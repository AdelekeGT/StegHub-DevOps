# PROJECT DOCUMENTATION

## Create two EC2 instances: mysql-server and mysql-client

![Screenshot 397](<img/Screenshot (397).png>)

## Change the permission for their SSH public keys

- These keys will allow connection to the servers

![Screenshot 398](<img/Screenshot (398).png>)

## Connect to mysql server EC2 Instance

![Screenshot 399](<img/Screenshot (399).png>)

## Update server components of mysql server EC2 Instance(sudo apt update)

![Screenshot 400](<img/Screenshot (400).png>)

## Update server components of mysql server EC2 Instance (concluded)

![Screenshot 401](<img/Screenshot (401).png>)

## Install mysql-server on the mysql server EC2 Instance

![Screenshot 402](<img/Screenshot (402).png>)

## Install mysql-server on the mysql server EC2 Instance (concluded)

![Screenshot 403](<img/Screenshot (403).png>)

## Start mysql_secure_installation

![Screenshot 404](<img/Screenshot (404).png>)

## mysql_secure_installation (concluded)

![Screenshot 405](<img/Screenshot (405).png>)

## Start mysql

- Check mysql status to be sure it is running

![Screenshot 406](<img/Screenshot (406).png>)

## Now, login to mysql client EC2 Instance

![Screenshot 407](<img/Screenshot (407).png>)

## Update server components of mysql client EC2 Instance

![Screenshot 408](<img/Screenshot (408).png>)

## Install mysql-client on mysql client EC2 Instance

![Screenshot 409](<img/Screenshot (409).png>)

## Check mysql version to confirm it is installed

![Screenshot 410](<img/Screenshot (410).png>)

## On AWS, edit mysql server Inbound Rule, add rule to open MySQL TCP port 3306

![Screenshot 411](<img/Screenshot (411).png>)

## Configure the Inbound Rule to allow traffic/connection from mysql client EC2 Instance's IP private IPv4 address

![Screenshot 412](<img/Screenshot (412).png>)

## Displays all mysql server Inbound Rules

![Screenshot 413](<img/Screenshot (413).png>)

## On mysql server EC2 Instance, open mysql configuration file

![Screenshot 414](<img/Screenshot (414).png>)

## Change 'bind-address' parameter to 0.0.0.0 (any IP address allowed)

![Screenshot 415](<img/Screenshot (415).png>)

## Make sure to restart MySQL after this change to effect the changes

- Check status to be sure mysql-server is running

![Screenshot 416](<img/Screenshot (416).png>)

## Go to mysql client EC2 Instance, and connect to mysql client's mysql-server using the client already installed

![Screenshot 417](<img/Screenshot (417).png>)

## Use the SHOW databases command to show databases on mysql server that has been successfully connected with

![Screenshot 418](<img/Screenshot (418).png>)
