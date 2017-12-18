## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. At a high level, what is Node?
run-time environment for executing JavaScript code server-side.

2. What is Express? Why is Express similar to in the Ruby world?
web application framework for Node.js
Sinatra

3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.
```
const express = require('express')
const app = express()

app.get('/api/v1/model/:id', jsController.action)
```
4. What do we use Knex for?
To build SQL queries in JS

5. How could you organize your code to follow the MVC design pattern in your Quantified Self project?
You could put your routes in the server.js file. request/response handling in controllers. knex SQL queries and other logic in the models.

6. How do you execute raw SQL in node?
`.raw()` method through Knex

7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?
Two advantages I can think of are modularity and reuasability. If you have your application logic (backend) completely seperated from your application user interface (frontend), you will have a slightly more modular web application. This will aid in a number of things (testing, readability, and maintainability). With a separate backend, your API can be reused with a number of applications and not just the one you originally created.

A disadvantage is that you're building two seperate applications so that will take more time. And testing can become more complicated and expensive.
#### Review  

8. Describe DNS.
Short for Domain Name System (or Service or Server), an Internet service that translates domain names into IP addresses.

9. What does writing clean code mean to you?
It means being able to write code that follows the 4 pillars of object oriented programming so that any developer at anytime can read your code and understand what is going on and how the application was built.

10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality?
class Room - would be responible for handling what goes on in that that, say changing the sheets, or calling down to the lobby
class Conceirge(sp?) - would handle guest relations like booking family trips or ordering late night pizza delivery
class Elevator- would handle getting the guest or employee to to the correct room
class Employee - would handle all thing help the guests like checking in and checking out and baggage service
class Guest - would handle the guest experience like paying for the room and using a phone to call an employee
