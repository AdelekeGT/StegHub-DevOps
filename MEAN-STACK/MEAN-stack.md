# Project Documentation

## Create a new EC2 Instance for the MEAN stack project and start the instance on AWS

![Screenshot 340](<img/Screenshot (340).png>)

## Login to the server on Windows Terminal

![Screenshot 341](<img/Screenshot (341).png>)

## Update server components (sudo apt update)

![Screenshot 342](<img/Screenshot (342).png>)

## Upgrade server (sudo apt upgrade)

![Screenshot 343](<img/Screenshot (343).png>)

## Install certificates

![Screenshot 344](<img/Screenshot (344).png>)

## Download and Install npm

![Screenshot 345](<img/Screenshot (345).png>)

## Install nodejs

![Screenshot 346](<img/Screenshot (346).png>)

## Install curl tool

![Screenshot 347](<img/Screenshot (347).png>)

## Installing MongoDB

- Import the MongoDB public GPG Key

- Create a list file for MongoDB

- Update the package database (sudo apt update)

- Install MongoDB

- Start MongoDB (sudo systemctl start mongod)

- Check MongoDB status (sudo systemctl status mongod)

- Enable MongoDB to run on boot (sudo systemctl enable mongod)

![Screenshot 350](<img/Screenshot (350).png>)

## Install body-parser using npm

## Create Books directory and cd into it

## Create node package using 'npm init'

![Screenshot 352](<img/Screenshot (352).png>)

## Node package creation (concluded)

![Screenshot 353](<img/Screenshot (353).png>)

## In Books directory, open create server.js file

![Screenshot 354](<img/Screenshot (354).png>)

## Contents of server.js file

![Screenshot 355](<img/Screenshot (355).png>)

## Back to home, Install express and mongoose globally

## cd into Books directory, create apps directory and cd into it

## Create routes.js file

![Screenshot 356](<img/Screenshot (356).png>)

## Contents of routes.js file

![Screenshot 357](<img/Screenshot (357).png>)

## In app directory, create models directory and cd into it

## Create book.js file

![Screenshot 358](<img/Screenshot (358).png>)

## Contents of book.js file

![Screenshot 359](<img/Screenshot (359).png>)

## Back to Book directory, create 'public' directory and cd into it

## Create script.js file

![Screenshot 360](<img/Screenshot (360).png>)

## Contents of script.js file

![Screenshot 361](<img/Screenshot (361).png>)

## Still inside 'public' directory, create index.html file

![Screenshot 362](<img/Screenshot (362).png>)

## Contents of index.html file

![Screenshot 363](<img/Screenshot (363).png>)

## Contents of index.html file (concluded)

![Screenshot 364](<img/Screenshot (364).png>)

## Back to Book directory, run the server.js file

![Screenshot 365](<img/Screenshot (365).png>)

## Curl the server localhost to see html file displayed in CL

![Screenshot 366](<img/Screenshot (366).png>)

## To be able to access the server from browser, edit inbound rules of server to open TCP port 3300 and allow connection from anywhere

- 3300 is the port at which our express server is running

![Screenshot 367](<img/Screenshot (367).png>)

## See new rule allowing traffic to TCP Port 3300

![Screenshot 369](<img/Screenshot (369).png>)

## Access the servers public IP address from browser, and see Book Management app displayed

![Screenshot 370](<img/Screenshot (370).png>)
