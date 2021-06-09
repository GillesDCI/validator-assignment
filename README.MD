# Use Express-Validator 

In this project we will be using express-validator to validate incoming data in our post requests. 

## What you will be doing

This project will allow you to practise:

> - Use of express-validator 
> - Writing middleware functions


This project assumes you've already had experience with:

> - Middleware functions
> - ExpressJs Routing


## Task 1 - Getting ready

1. Initialise npm into your project
   `npm init -y`
2. Install the express.js npm package
   `npm i express`
3. Install the express-validator npm package
   `npm i express-validator`
4. Create a file for your server (`server.js`)


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


## Task 4 - Create validateUser route handler
  1. Create a POST route handler `/validation/validateUser` which allows you to add a new user using the following JSON body :
 ```json
{
  "firstName" : "steve",
  "lastName" : "stevenson",
  "age": "129",
  "fbw": "36",
  "profession" : "Musician",
  "email" : "steve@steve.com"
}
```
For the  `/validation/validateUser` endpoint: 

- Create a middleware method that will make sure the object received contains `firstName`, `lastName`, `age`, `fbw` and `email`.
- Create a middleware method that will check if the user is above 18 years old
- Create a middleware method that checks whether the e-mail address is valid.
- If all the above is true, then you should send a response with a success message
- If any of the middleware fails, you should send a response with an error message that says why the user is not valid.




## Task 5 - Create sanitizeUser route handler
  1. Create a POST route handler `/validation/sanitizeUser` which allows you to add a new user using the following JSON body :
 ```json
{
  "firstName" : "steve",
  "lastName" : "stevenson",
  "age": "129",
  "fbw": "36",
  "profession" : "Musician",
  "email" : "steve@steve.com"
}
```

For the  `/validation/sanitizeUser` endpoint: 

 - Create a middleware that normalizes the `email`.
- Create a middleware that makes the `firstName` and `lastName` start with a capital letter
 - Create a middleware that will turn `age` and `fbw` to numbers


## Resources
-  https://github.com/validatorjs/validator.js#validators
-  https://github.com/validatorjs/validator.js#sanitizers
-  https://express-validator.github.io/docs/

