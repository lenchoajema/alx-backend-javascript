#0x05. NodeJS Basic
#run javascript using NodeJS
#use NodeJS modules
#use specific Node JS module to read files
#use process to access command line arguments and the environment
#create a small HTTP server using Node JS
#create a small HTTP server using Express JS
#create advanced routes with Express JS
#use ES6 with Node JS with Babel-node
#use Nodemon to develop faster

# NodeJS and ExpressJS Project

## Introduction
Welcome to the **NodeJS and ExpressJS** project! This repository provides an overview of running JavaScript using NodeJS, utilizing NodeJS modules, reading files, accessing command line arguments and the environment, creating HTTP servers with NodeJS and ExpressJS, using ES6 with Babel-node, and improving development speed with Nodemon.

## Features
- Running JavaScript using NodeJS
- Using NodeJS modules
- Reading files with NodeJS
- Accessing command line arguments and environment variables
- Creating a small HTTP server using NodeJS
- Creating a small HTTP server using ExpressJS
- Creating advanced routes with ExpressJS
- Using ES6 with NodeJS via Babel-node
- Speeding up development with Nodemon

## Prerequisites
Before you begin, ensure you have the following installed:
- NodeJS
- npm (Node package manager)
- Nodemon
- Babel-node

## Installation
Follow these steps to set up and run the project:

1. **Clone the repository:**
   
   git clone https://github.com/your-username/nodejs-express-project.git
   cd nodejs-express-project
   

2. **Install the dependencies:**
   
   npm install
   

## Running JavaScript Using NodeJS
You can run a JavaScript file using NodeJS with the following command:

node your_script.js


## Using NodeJS Modules
NodeJS modules allow you to split your code into reusable pieces. Use the `require` function to import modules.
javascript
const fs = require('fs');
const http = require('http');


## Using Specific NodeJS Module to Read Files
NodeJS provides the `fs` module to interact with the file system.
javascript
const fs = require('fs');

fs.readFile('path/to/file.txt', 'utf8', (err, data) => {
  if (err) {
    console.error(err);
    return;
  }
  console.log(data);
});


## Using `process` to Access Command Line Arguments and the Environment
The `process` object in NodeJS provides information about the current NodeJS process.
javascript
// Access command line arguments
const args = process.argv.slice(2);
console.log(args);

// Access environment variables
console.log(process.env);


## Creating a Small HTTP Server Using NodeJS
NodeJS allows you to create a simple HTTP server using the `http` module.
javascript
const http = require('http');

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello, World!\n');
});

const PORT = 3000;
server.listen(PORT, () => {
  console.log(`Server running at http://localhost:${PORT}/`);
});


## Creating a Small HTTP Server Using ExpressJS
ExpressJS is a minimal and flexible NodeJS web application framework.
javascript
const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send('Hello, World!');
});

const PORT = 3000;
app.listen(PORT, () => {
  console.log(`Server running at http://localhost:${PORT}/`);
});


## Creating Advanced Routes with ExpressJS
ExpressJS makes it easy to define advanced routes.
javascript
const express = require('express');
const app = express();

app.get('/user/:id', (req, res) => {
  res.send(`User ID: ${req.params.id}`);
});

const PORT = 3000;
app.listen(PORT, () => {
  console.log(`Server running at http://localhost:${PORT}/`);
});


## Using ES6 with NodeJS via Babel-node
Babel-node allows you to use the latest JavaScript features with NodeJS.
1. **Install Babel dependencies:**
   
   npm install --save-dev @babel/core @babel/node @babel/preset-env
   

2. **Create a `.babelrc` file in the root directory:**
   json
   {
     "presets": ["@babel/preset-env"]
   }
   

3. **Run your ES6 code using Babel-node:**
   
   npx babel-node your_script.js
   

## Speeding Up Development with Nodemon
Nodemon automatically restarts your NodeJS application when file changes are detected.
1. **Install Nodemon globally:**
   
   npm install -g nodemon
   

2. **Use Nodemon to run your application:**
   
   nodemon your_script.js
   

## Conclusion
This project covers the essentials of using NodeJS and ExpressJS, including running JavaScript, using modules, reading files, creating HTTP servers, and improving development efficiency with ES6 and Nodemon. Explore the examples and documentation to deepen your understanding and mastery of these topics.

