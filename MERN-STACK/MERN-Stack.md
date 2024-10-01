# Project Documentation

## Create a new EC2 Instance for the MERN stack project and start the instance on AWS

![Screenshot 221](<img/Screenshot (221).png>)

## Login to the server on Windows Terminal

![Screenshot 222](<img/Screenshot (222).png>)

## Update server components (sudo apt update)

![Screenshot 223](<img/Screenshot (223).png>)

## Download node

- Node dowloading

![Screenshot 224](<img/Screenshot (224).png>)

- Node download concluded

![Screenshot 225](<img/Screenshot (225).png>)

## Install nodejs

![Screenshot 226](<img/Screenshot (226).png>)

## Check to be certain nodejs had been installed

## Check to be certain node package manager (npm) has been installed

## Create Todo directory and 'cd' into it

![Screenshot 228](<img/Screenshot (228).png>)

## Create a node project using 'npm init'

![Screenshot 230](<img/Screenshot (230).png>)

## Install expressjs

![Screenshot 231](<img/Screenshot (231).png>)

## Create index.js file

![Screenshot 232](<img/Screenshot (232).png>)

## Contents of index.js file

![Screenshot 233](<img/Screenshot (233).png>)

## Run index.js using node (server should be running)

![Screenshot 234](<img/Screenshot (234).png>)

## Edit EC2 Instance inbound rules

- Open TCP port 5000 and Allow request from anywhere to connect

![Screenshot 235](<img/Screenshot (235).png>)

## Acess server IP address from a browser and get a welcome response

![Screenshot 236](<img/Screenshot (236).png>)

## Create 'routes' directory and 'cd' into it

## Create file api.js

![Screenshot 237](<img/Screenshot (237).png>)

## Contents of api.js file

![Screenshot 238](<img/Screenshot (238).png>)

## Back to home, install mongoose

![Screenshot 239](<img/Screenshot (239).png>)

## Create models directory and 'cd' into it

## Create todo.js file and open it using vi editor

![Screenshot 240](<img/Screenshot (240).png>)

## Contents of todo.js file

![Screenshot 241](<img/Screenshot (241).png>)

## Get back inside the routes directly and edit the api.js file

![Screenshot 242](<img/Screenshot (242).png>)

## Edit to the api.js file

![Screenshot 243](<img/Screenshot (243).png>)

## Create a Cluster on mongodb.com

![Screenshot 249](<img/Screenshot (249).png>)

## 'cd' into Todo directory and create .env file

![Screenshot 250](<img/Screenshot (250).png>)

## Content of .env file - contains the connect string to the mongo database created on mongodb.com

![Screenshot 251](<img/Screenshot (251).png>)

## Now edit index.js to connect to the created database

![Screenshot 252](<img/Screenshot (252).png>)

## New contents of index.js file

![Screenshot 253](<img/Screenshot (253).png>)

## Cluster on mongodb, other network access parameters configured

![Screenshot 269](<img/Screenshot (269).png>)

## Create a POST request to /api/todos on Postman

## Edit the Headers section to include the 'Content-Type' header with the value 'application/json'

![Screenshot 270](<img/Screenshot (270).png>)

## Edit the Body section to include to todo to post

![Screenshot 271](<img/Screenshot (271).png>)

## In the Todo diretory, create a react app

![Screenshot 272](<img/Screenshot (272).png>)

## Install 'concurrently' as a dependency

## Install 'nodemon' as a dependency

![Screenshot 273](<img/Screenshot (273).png>)

## Open pacakge.json and made edits to the script key

- Script to include 'nodemon' and 'concurrently' workiing at the start of the server app

![Screenshot 275](<img/Screenshot (275).png>)

## cd into client directory and open package.json file

![Screenshot 302](<img/Screenshot (302).png>)

## Add 'proxy' key to package.json file

![Screenshot 303](<img/Screenshot (303).png>)

## Create src directory and 'cd' into it

## Create components directory and 'cd' into it

## create Input.js, Todo.js and ListTodo.js files

![Screenshot 304](<img/Screenshot (304).png>)

## Contents of Input.js file

![Screenshot 305](<img/Screenshot (305).png>)

## Back to client directory, install axios

## 'cd' into src/components directory and open ListTodo.js file

![Screenshot 306](<img/Screenshot (306).png>)

## Contents of LisTodo.js

![Screenshot 307](<img/Screenshot (307).png>)

## Open Todo.js file

![Screenshot 308](<img/Screenshot (308).png>)

## Contents of Todo.js

![Screenshot 309](<img/Screenshot (309).png>)

## Back a step to src directory, create App.js file

![Screenshot 310](<img/Screenshot (310).png>)

## Contents of App.js file

![Screenshot 311](<img/Screenshot (311).png>)

## In src directory, create App.css file

![Screenshot 312](<img/Screenshot (312).png>)

## Contents of App.css file (image A)

![Screenshot 313](<img/Screenshot (313).png>)

## Contents of App.css file (image B)

![Screenshot 314](<img/Screenshot (314).png>)

## Create index.css file

![Screenshot 315](<img/Screenshot (315).png>)

## Contents of index.css file

![Screenshot 316](<img/Screenshot (316).png>)

## Back to Todo directory, run 'npm run dev'

![Screenshot 317](<img/Screenshot (317).png>)

## Access localhost from a browser

- Todo app is displayed
- Add todo and see activities displayed in Todolist

![Screenshot 318](<img/Screenshot (318).png>)

## Add more activities to test Todolist

![Screenshot 319](<img/Screenshot (319).png>)
