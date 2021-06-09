# Use Express-Validator 

In this project we will be using express-validator to validate incoming data in our post requests. 

## What you will be doing

This project will allow you to practise:

> Use of express-validator 
> Writing middleware functions


This project assumes you've already had experience with:

> - Middleware functions
> - ExpressJs Routing


## Task 1 - Getting ready

1. Initialise npm into your project
   `npm init -y`
2. Install the express.js npm package
   `npm i express`
3. Create a file for your server (`server.js`)


## Task 2 - Set up your server

##### starter code
```javascript
const express = require('express');
const app = express();

app.use(express.urlencoded({extended:true}));
app.use(express.json());

app.listen(3001, () => {
   console.log("The server is listening to requests") 
});
```

## Task 3 - Setting up routes 

  1. Create a folder /routes 
  2. Create a validationRoutes.js file 
  3. Import the route applications into your `server.js` file.
  4. Assign the route application to their respective route. `/validation`


## Task 4 - Create route handlers in postsRoutes.js
  1. Create a POST route handler `/validation/validateUser` which allows you to add a new user using the following JSON body :
 ```json
{
  "firstName" : "steve",
  "lastName" : "stevenson",
  "age": "129",
  "fbw": "36"
  "profession" : "Musician",
  "favoriteBands" : ["Radiohead", "Motorhead", "Machinehead", "The talking heads" ],
  "email" : "steve@steve.com"
}
```







