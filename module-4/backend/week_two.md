## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's one difference between ES5 and ES6?
in ES6 you have you have scoping uses classes.

2. What's the difference between asynchronous and synchronous JavaScript? 
Synchronous loading occurs when the browser must halt the rendering of the page in order to complete the execution of JavaScript code.
Asynchronousis when JavaScript code is processed in parallel to the rest of the page content. 

3. What are the four pillars of Object Oriented programming?
Abstraction. 
Encapsulation.
Inheritance. 
Polymorphism.

4. What are some tools available in JavaScript to help you write object oriented code?
Refactoring?? not sure i understand

5. What are some key concepts to be aware of when refactoring your JavaScript?
Look for functions larger than 10 lines of code, look for long conditionals, look for makint things into functions to be used later

6. What's a callback function and what are some reasons when we use/need callback functions?
A callback function is a function that is passed to another function as a parameter, and the callback function is called inside the other function. Youw really want to avoid using callbacks and use promises instead.

7. What's the scope of variables in Javascript?
JavaScript has two scopes – global and local. Any variable declared outside of a function belongs to the global scope, and is therefore accessible from anywhere in your code. Each function has its own scope, and any variable declared within that function is only accessible from that function and any nested functions.

8. What's the difference between `==` and `===` in JavaScript?
The double equal (==) is an auto type converting equality and three equals (===) isa strict equality operator, i.e., it will not covert values automatically.

9. Why do front end frameworks exist?
Frameworks make your life easier by simplifying complex problems so you can focus on finishing your project. 
Keep state out of the DOM
Higher-level abstractions
Code organization
Common concepts that can be shared between apps and developers
Large communities, shared knowledge, documentation, bug fixes
Better app structure through tools and guidelines

#### Review  

10. Why do people say "HTTP is stateless"?
HTTP is a stateless protocol, which means that the connection between the browser and the server is lost once the transaction ends.

11. Describe a RESTful API.
REST is an architectural style, and RESTful is the interpretation of it. That is, if your back-end server has REST API and you make client-side requests (from a website/application) to this API, then your client is RESTful. Follows convention of PUT POST DELETE GET.

12. What are some main characteristics of a team following an agile workflow?
Sprints (evey 2 weeks for example), having a stand up at the beginning of the spring and retro at the end of the sprint, having a team lead or scrum master to faciliate the sprints.

13. What are some advantages **and** disadvantages to using OAuth to authenticate a user?
Pros
all OAuth data transfers must take place on SSL (Secure Sockets Layer) to ensure the most trusted cryptography industry protocols are being used to keep data as safe as possible.

Not only does OAuth give users the power to allow sites limited access to their data, but it even allows users to control when that timeframe window is up. It’s comforting that users can choose when authorization tokens expire

Cons
Needing to make anonymous alternate accounts can be just as annoying as having to toggle dozens of site privacy settings each month.
You choose to use a central hub to connect to all your other favorite sites, and the central account becomes hacked, or you simply choose to close the account, then the serious repercussions are felt across several sites instead of just one.
