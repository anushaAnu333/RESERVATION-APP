Backend

npm init -y
main-index-->server.js
mkdir frontend backend  --to create folder

npm i express mongoose dotenv

install 2 dev dependencies 
concurrently-allows us to run script -backend and frontend at the same time

npm i --save-dev nodemon concurrently

cd frontend

npx create-react-app .

in backend create file server.js
inside

Entry point of the server

create an xpress application 
 const express=require("express")------

 Initiate express function in app variable
 const app=express()

create server at port 3000

app.listen(3000,function()=>{
    console.log("server running")
})


create 2 file .env and .gitignore

inside 

.env
PORT=5000
MONGO_URL=


server.js
we need to bring .env in the server
require('dotenv').config()

run the server
in the terminal---node backend/server.js