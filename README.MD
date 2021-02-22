Create a server.js file, this is a creation of the server

http is already embedded in the node modules, just bring it in as a const, no need to use the cli command
Use postman a headless browser without the gui.
After console.log add
`Res.end`

Will automatically give a 200 response.
The response so far is:

`Url:”/“,
Method: “GET”`

Control +C quit the server and re-run in postman

`const {headers, url, method }= req;
console.log(headers, url, method);`

Run this through postman at http:localhost:5000
 Fig postman3.png

’npm install —save—dev nodemon’

This also installs (node_modules)

The dev is for the development environment which is will change in prod env.

Check the devDependencies in package.json to see that nodemon has been correctly installed

“start” : “nodemon server.js”

Then  ‘npm start’ will get what you have got already on port 5000.

const PORT= 5000 was in the server.js file.

______


Now in the console, start on the major project
`npm init` install node_modules

`npm i express dotenv`

`npm install —save—dev nodemon`




