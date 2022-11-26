Backend

npm init -y
main-index-->server.js
mkdir frontend backend --to create folder

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

create server at port 5000

app.listen(5000,function()=>{
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
in the terminal---node backend/server.js -------shows server running on 5000

copy paste gitingore in frontend to gitingore outside

node_modules
node_modules/ give like this it will block node in src

in frontend terminal run the command

rm -rf .git
ls -a----------shows git is not here
delete gitignore in frontend

c.. to come out of folder

git init

add .env in gitignore

package.json
inside script

'start':"node backend/server.js"
"server":"nodemon backened/server.js"
"client":"npm start --prefix frontent"
"dev":"concurrently \"npm run server\"\"npm run client\""
