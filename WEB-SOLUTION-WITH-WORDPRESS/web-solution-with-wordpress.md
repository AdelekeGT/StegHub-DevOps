# Project Documentation

## Create a new RedHat OS EC2 Instance which will be the Web Server

![Screenshot 486](<img/Screenshot (486).png>)

## Add 3 new EBS volumes of 10GiB each

![Screenshot 487](<img/Screenshot (487).png>)

## RedHat web server running successfully

![Screenshot 488](<img/Screenshot (488).png>)

## Grant necessary permission to server ssh private key

## ssh into web server

## Use `lsblk` command to inspect what block devices are attached to the server

```bash
lsblk
```

## Inspect with `ls /dev/` to see all 3 newly created block devices

```bash
ls /dev/
```

![Screenshot 490](<img/Screenshot (490).png>)

## Use `df -h` to see all mounts and free space on the server

```bash
df -h
```

![Screenshot 491](<img/Screenshot (491).png>)

## Use `gdisk` utility to create a single partition on each of the 3 disks

- `gdisk` on xvdb

```bash
gdisk /dev/xvdb
```

![Screenshot 492](<img/Screenshot (492).png>)

- `gdisk` on xvdc

```bash
gdisk /dev/xvdc
```

![Screenshot 493](<img/Screenshot (493).png>)

- `gdisk` on xvdbd

```bash
gdisk /dev/xvdbd
```

![Screenshot 494](<img/Screenshot (494).png>)

- Use `lsblk` to view the newly configured partitions on the 3 disks

![Screenshot 500](<img/Screenshot (500).png>)

## Install `lvm2` package

```bash
sudo yum install lvm2
```

- lvm2 installation started

![Screenshot 495](<img/Screenshot (495).png>)

- lvm2 installation concluded

![Screenshot 496](<img/Screenshot (496).png>)

## Use `pvcreate` utility to mark each of the 3 disks as physical voluemes (PVs) to be used by LVM

```bash
sudo pvcreate /dev/<volume>
```

- Verify that Physical Volume has been created successfully

```bash
sudo pvs
```

- Use `vgcreate` utility to add all 3 PVs to a volume group (VG) named `webdata-vg`

```bash
sudo vgcreate webdata-vg /dev/xvdb1 /dev/xvdc1 /dev/svdbd1
```

- Verify that Volume Group (VG) has been successfully created

```bash
sudo vgs
```

- Use `lvcreate` utility to create 2 logical volumes: apps-lv and logs-lv

```bash
sudo lvcreate -n apps-lv -L 14G webdata-vg && sudo lvcreate -n logs-lv -L 14G webdata-vg
```

- Verify that Logical Volume (Lv) hs been successfully created

```bash
sudo lvs
```

![Screenshot 502](<img/Screenshot (502).png>)

## Verify the entire setup

```bash
sudo vgdisplay -v #view complete setup - VG, PV, and LV
```

- vgdisplay started

![Screenshot 503](<img/Screenshot (503).png>)

- vgdisplay concluded

![Screenshot 504](<img/Screenshot (504).png>)

```bash
sudo lsblk
```

![Screenshot 505](<img/Screenshot (505).png>)

## Use `mkfs.ext4` to format the logical volumes with **ext4** filesystem

```bash
sudo mkfs -t ext4 /dev/webdata-vg/apps-lv
sudo mkfs -t ext4 /dev/webdata-vg/logs-lv
```

![Screenshot 506](<img/Screenshot (506).png>)

## Website files and logs

- Create `/var/www/html` directory to store website files

```bash
sudo mkdir -p /var/www/html
```

- Create `/home/recovery/logs` to store backup of log data

```bash
sudo mkdir -p /home/recovery/logs
```

- Mount `/var/www/html` on `apps-lv` logical volume

```bash
sudo mount /dev/webdata-vg/apps-lv /var/www/html/
```

- Use `rsync` utility to backup all the files in `/var/log` into `/home/recovery/logs`

```bash
sudo rsync -av /var/log/ /home/recovery/logs/
```

- Mount `/var/log` on `logs-lv` logical volume

```bash
sudo mount /dev/webdata-vg/logs-lv /var/log
```

![Screenshot 507](<img/Screenshot (507).png>)

- Restore log files back into `/var/log` directory

```bash
sudo rsync -av /home/recovery/logs/ /var/log
```

![Screenshot 508](<img/Screenshot (508).png>)

## Update `/etc/fstab` file so that the mount configuration will persist after restart of the server

- Check the UUID of the devices

```bash
sudo blkid
```

![Screenshot 509](<img/Screenshot (509).png>)

- Update `/etc/fstab` usinf the UUID and remove the leading and ending quotes

```bash
sudo vi /etc/fstab
```

![Screenshot 512](<img/Screenshot (512).png>)

## Test the configuration, reload the daemon, and verify setup

```bash
sudo mount -a
sudo systemctl daemon-reload
df -h
```

![Screenshot 513](<img/Screenshot (513).png>)

## Prepare the Database Server

Now, we're ready to install and configure the MySQL server, which will act as the database for our website on the server instance. To accomplish this, we'll replicate the process we used for the server instance, including creating a RedHat EC2 instance, attaching the three EBS volumes, and SSHing into the instance to create partitions.

Create logical volumes using the same process as we did in the server instance. The logical volume should be named db-lv instead of apps-lv. Additionally, create another logical volume named logs-lv. Mount the db-lv to the /db/ directory.

## Install WordPress on Web Server

- Update the server repository

```bash
sudo yum -y update
```

![Screenshot 529](<img/Screenshot (529).png>)

![Screenshot 530](<img/Screenshot (530).png>)

- Install wget, Apache and its dependencies

```bash
sudo yum -y install wget httpd php php-mysqlnd php-fpm php-json
```

![Screenshot 531](<img/Screenshot (531).png>)
![Screenshot 532](<img/Screenshot (532).png>)

- Start Apache

```bash
sudo systemctl enable httpd && sudo systemctl start httpd
```

- Install PHP and its dependencies

```bash
sudo yum install https://dl.fedoraproject.org/pub/epel epel-release-latest-8.noarch.rpm
sudo yum install yum-utils http://rpms.remirepo.net/enterprise/remi-release-8.rpm
sudo yum module list php sudo yum module reset php
sudo yum module enable php:remi-7.4
sudo yum install php php-opcache php-gd php-curl php-mysqlnd
sudo systemctl start php-fpm
sudo systemctl enable php-fpm
setsebool -P httpd_execmem 1
```

- Restart Apache

```bash
sudo systemctl restart httpd
```

![Screenshot 533](<img/Screenshot (533).png>)
![Screenshot 534](<img/Screenshot (534).png>)
![Screenshot 535](<img/Screenshot (535).png>)
![Screenshot 536](<img/Screenshot (536).png>)
![Screenshot 537](<img/Screenshot (537).png>)

- Download wordpress and copy wordpress to `/var/www/html`

```bash
mkdir wordpress && cd wordpress
sudo wget http://wordpress.org/latest.tar.gz
sudo tar xzvf latest.tar.gz
sudo rm -rf latest.tar.gz
sudo cp wordpress/wp-config-sample.php wordpress/wp-config.php
cp -R wordpress /var/www/html/
```

![Screenshot 538](<img/Screenshot (538).png>)
![Screenshot 539](<img/Screenshot (539).png>)
![Screenshot 540](<img/Screenshot (540).png>)

- Configure SELinux Policies

```bash
sudo chown -R apache:apache /var/www/html/wordpress
sudo chcon -t httpd_sys_rw_content_t /var/www/html/wordpress -R
sudo setsebool -P httpd_can_network_connect=1
```

![Screenshot 541](<img/Screenshot (541).png>)

## Install MySQL on your DB Server EC2

- Update server repository and install `mysql-server`

```bash
sudo yum update
sudo yum install mysql-server
```

![Screenshot 542](<img/Screenshot (542).png>)
![Screenshot 543](<img/Screenshot (543).png>)
![Screenshot 544](<img/Screenshot (544).png>)
![Screenshot 545](<img/Screenshot (545).png>)

- Verify that mysql servise is up and running

```bash
sudo systemctl status mysqld
sudo systemctl restart mysqld
sudo systemctl enable mysqld
```

![Screenshot 546](<img/Screenshot (546).png>)

## Configure DB to work with WordPress

```bash
sudo mysql
```

```mysql
CREATE DATABASE wordpress;
CREATE USER 'myuser'@'web-server-ip-address' IDENTIFIED BY 'choose your password';
GRANT ALL ON wordpress.* TO 'myuser'@'web-server-ip-address';
FLUSH PRIVILEGES;
SHOW DATABASES;
exit
```

![Screenshot 547](<img/Screenshot (547).png>)

## Configure WordPress to connect to remote database

- Go to AWS, edit Inbound Rule on DB server by opening MySQL/Aurora port 3306 and allowing access to the DB ONLY from Web Server(WordPress) IP address.

![Screenshot 548](<img/Screenshot (548).png>)

- On Web Server, install MySQL client;

```bash
sudo yum install -y mysql-client
```

![Screenshot 549](<img/Screenshot (549).png>)

- Test that you can connect from Web Server to DB server by using `mysql-client`.
- Verify that you can successfully execute `SHOW DATABASES;` on MySQL

```bash
sudo mysql -u myuser -p -h <DB-server-ip-address>
```

![Screenshot 550](<img/Screenshot (550).png>)

- Remember to change Inbound Rules on Web Server; Enable TCP port 80 to allow access from everywhere 0.0.0.0/0

- Try to access from your browser the link to WordPress `http://<Web-Server-Public-IP-Address>/wordpress/`

![Screenshot 551](<img/Screenshot (551).png>)

- Fill out DB credentials

![Screenshot 552](<img/Screenshot (552).png>)

- Successful WordPress installation message on browser

![Screenshot 553](<img/Screenshot (553).png>)
