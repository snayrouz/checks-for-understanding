## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?
Unit testing in JavaScript. I believe that testing at the unit level, at the very least, should always help drive development.

2. What are some tools to help debug JavaScript code?
Debugger, Inspector-> dev console, pryjs

3. What are some tools you need in order to unit test your JavaScript?
Mocha/Chai

4. What is the syntax for invoking a function?
 const someFunc = () => {
    // do something
  }
  someFunc()
  
  
5. What is CORS?
(Looked this up)
Mechanism that uses additional HTTP headers to let a user agent gain permission to access selected resources from a server on a different origin (domain) than the site currently in use. A user agent makes a cross-origin HTTP request when it requests a resource from a different domain, protocol, or port than the one from which the current document originated.

6. How do we enable CORS?

    Open Internet Information Service (IIS) Manager.
    Right click the site you want to enable CORS for and go to Properties.
    Change to the HTTP Headers tab.
    In the Custom HTTP headers section, click Add.
    Enter Access-Control-Allow-Origin as the header name.
    Enter * as the header value.
    Click Ok twice.
    
7. What's `this` in JavaScript?
Refers to the parent object

8. What is Webpack and why is it useful?
Build tool that puts all of your assets, including Javascript, images, fonts, and CSS, in a dependency graph. It's useful if
your application has a complex front end and a lot of content.

9. When/why do you want to use event delegation?
(Looked this up for a proper definition)
Event delegation allows us to attach a single event listener, to a parent element, that will fire for all descendants matching a selector, whether those descendants exist now or are added in the future.

11. What's `npm` and what do we use it for?
npm is a package manager for the JavaScript programming language. npm can manage packages that are local dependencies of a particular project.

#### Review  
12. What's the MVC design pattern? Describe each part of MVC.
MVC stands for Model View Controller, and is a web-app design architecture.
Model-where we keep all the logic for the application
View- where we handle the rendering of our site
Controller- where we handle the routing/actions of our application

13. What are a few ways to optimize a Rails application?
Caching, shorter DB queries, indexing, background workers

14. What's a background worker? When would we want to use a background worker?
Background workers are a way to execute regular jobs that might otherwise compromise site performance or hamper scalability. For example, we can use a background worker to send emails out to users, or we can use a background worker to perform an API call to update the DB every night.

