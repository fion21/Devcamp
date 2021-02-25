## Replica Education Course Directory
#### API, Auth, GPPD/CRUD, NoSQL or any data source
##### Project run through gist
The project aims to have various pieces of code which can be re-used for
basic or high-level projects from this stage. The data source could be using
a mock api to simulate a project in it's early stages of mvp (minimal viable product) of greater monetary value prior to stakeholders' approval.
Notes:
Create a `server.js` file, this is a creation of the server
http is already embedded in the node modules, just bring it in as a const, no need to use the cli command
Use `postman` a headless browser without the gui.
After console.log add
`Res.end` Will automatically give a 200 response.
The response so far is:
`Url:”/“, Method: “GET”`

Control +C quit the server and re-run in postman
______

`const {headers, url, method }= req;
console.log(headers, url, method);`

Run this through postman at `http:localhost:5000`
 
 ![](https://github.com/fion21/Devcamp/blob/main/src/postman3.png?raw=true)
 

’npm install —save—dev nodemon’

This also installs (node_modules)

The dev is for the development environment which is will change in prod env.

Check the devDependencies in package.json to see that nodemon has been correctly installed

“start” : “nodemon server.js”

Then  ‘npm start’ will get what you have got already on port 5000.

const PORT= 5000 was in the server.js file.

 ![](https://github.com/fion21/Devcamp/blob/main/src/postman4.png?raw=true)

______


Now in the console, start on the major project
`npm init` install node_modules

`npm i express dotenv`

`npm install —save—dev nodemon`

## Routes set-up

Express has been brought in, the basic links are being derived.

const express = require('express');
const router = express.Router();

app.get('api/v1/bootcamps', (req, res) => {
    res.status(200)
    .json({success: true, msg: 'Show all bootcamps'});
    });
______

## Fixed Error
// Load env vars
//dotenv.config({ path: './config/config.env' });
const path = require('path')
require('dotenv').config({ path: path.resolve(__dirname, './config/config.env') })

______
## Security, database, colours

abstraction layer for nosql and security
added mongoose

`npm i colors`
added colors to the output of text
${conn.connection.host}`.cyan.underline.bold);` so that it is really easy to read in the console.
