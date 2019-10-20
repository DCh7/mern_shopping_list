Getting started: mern_shopping_list

$npm init

entry point: server.js
license: MIT

$npm i express body-parser mongoose concurrently

Express.js : helps manages routes, handling requests and views.
Body-parser : extract entire body portion of an incoming request stream and exposes it on req.body

$npm i -D nodemon

Nodemon: will constantly watch backend and reload on save
-D will install on dev dependency, so it's ignored in production

"scripts": {
    "start": "node server.js"
}

Scripts will be executed when run on production

How to run scripts: npm run <scripts>

URI is stored in config/keys
API is stored in routes/api

$npm i bcryptjs



================= CLIENT ===================

Run $create-react-app

Since we will be using axios, in package.json add

"proxy": "http://localhost:5000"     //Same json level as private, dependencies, and scripts

Add new scripts for running both server and client

"client-install": "npm install --prefix client",
...
"client": "npm start --prefix client",
"dev": "concurrently \"npm run server\" \"npm run client\""

Add external packages in client
$npm i bootstrap reactstrap uuid react-transition-group

uuid generates unique id

$npm i redux react-redux redux-thunk

store.js : entry point for redux store

$npm i axios

Why postbuild prod config set to false: it's not gonna run build script if it in production