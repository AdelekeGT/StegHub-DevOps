# Project Documentation

## Login to EC2 Instance using Gitbash

![Screenshot 149](<img/Screenshot (149).png>)

## apt update

![Screenshot 151](<img/Screenshot (151).png>)

## Nginx Installation A

![Screenshot 152](<img/Screenshot (152).png>)

## Nginx Installation B

![Screenshot 153](<img/Screenshot (153).png>)

## Check Nginx status

![Screenshot 154](<img/Screenshot (154).png>)

## Use 'curl' to test IP Address

- ### Check Nginx Server to see if it can be accessed locally

![Screenshot 155](<img/Screenshot (155).png>)

## Test IP Address from a browser

- ### Nginx default page

![Screenshot 156](<img/Screenshot (156).png>)

## Install mysql-server

![Screenshot 157](<img/Screenshot (157).png>)

## Login to mysql

![Screenshot 158](<img/Screenshot (158).png>)

## Alter User to access mysql using mysql_native_password

![Screenshot 159](<img/Screenshot (159).png>)

## Execute mysql_secure_installation

![Screenshot 164](<img/Screenshot (164).png>)

## Login to mysql with new altered password

![Screenshot 165](<img/Screenshot (165).png>)

## Exit mysql

![Screenshot 166](<img/Screenshot (166).png>)

## Install 'php-fpm' and 'php-mysql'

![Screenshot 167](<img/Screenshot (167).png>)

## Configure nginx to serve a custom website

- ### Create custom web directory in /var/www/

- ### Grant permissions to user on the created web directory

- ### Create new configuration in /etc/nginx/sites-available/

![Screenshot 168](<img/Screenshot (168).png>)

## Content of new config file in /etc/nginx/sites-available/

![Screenshot 169](<img/Screenshot (169).png>)

## Create symbolic link to new config file in /etc/nginx/sites-enabled/

![Screenshot 170](<img/Screenshot (170).png>)

## Check nginx configuration to make sure it is Ok

![Screenshot 171](<img/Screenshot (171).png>)

## Unlink default config in /etc/nginx/sites-enabled/

![Screenshot 172](<img/Screenshot (172).png>)

## Restart nginx

![Screenshot 173](<img/Screenshot (173).png>)

## Create an index.html file in /var/www/'project-directory'/ to be served as default for custom site

![Screenshot 174](<img/Screenshot (174).png>)

## In stead of index.html, create info.php file in /var/www/'project-directory'/ to be served as default

![Screenshot 175](<img/Screenshot (175).png>)

## Content of info.php file

![Screenshot 176](<img/Screenshot (176).png>)

## info.php file rendered on browser when Nginx server is hit

![Screenshot 177](<img/Screenshot (177).png>)

## Create new mysql database

![Screenshot 178](<img/Screenshot (178).png>)

## Create new mysql user

- ### Grant all privileges to user only on the new database created

![Screenshot 179](<img/Screenshot (179).png>)

## Login using new created user credentials

- ### SHOW DATABASES

- ### USE 'created' DATABASE

- ### CREATE TABLE

- ### INSERT INTO TABLE

- ### SELECT \* FROM TABLE - to show all contents of table

![Screenshot 180](<img/Screenshot (180).png>)

## Create another todo_list.php file to get info from database and render on browser

![Screenshot 181](<img/Screenshot (181).png>)

## Content of todo_list.php

![Screenshot 183](<img/Screenshot (183).png>)

## Todo list rendered on browser through todo_list.php

![Screenshot 184](<img/Screenshot (184).png>)
