## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
A tool that helps show the state of your html requests.

* What’s the difference between a session and a cookie?
A session is like a cookie however it adds an extra layer of security to the cookie so a user can't tamper with the information in your cookie.

* What’s a flash and when do you want to use flashes?
A flash is a message sent to the user/visitor/admin (whoever's on the page) regarding an error, update or anything that the developer needs to communicate with the user.

* Why do people say “HTTP is stateless”?
It doesn't hold any state just the behavior of how the code is rendered to the screen. 

* What’s authentication? Explain.
Authentication is rails identifying that the person logging in is really who they say there are.

* What’s the difference between authentication and authorization?
Authorization takes authentication a step further by saying "ok this is who you are, and this is what you have access to view based on who you are"

* What’s a before filter?
A before filter is a helper method that will run before your actions in that controller. You can keep a before_action in your base controller if you want to use that helper method across multiple controllers.

* How do we keep track of a user once they’ve logged in?
Sessions act has a hash in rails and you can store any information you want in them as a key value pair. So you could store their user_id, admin_id when they log in, and then when they log out, you clear that session.

* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two 
approaches?
You want to namespace a resource when you want to restrict/permit certain access to views in your application. You nest a resource when you have a database relationship(belongs_to, has_many, many_to_many). The difference is a a namespaced resource may will have different access than a non namespaced resource, however it can still works the same db relationships. 

* At a high level, what tools can you use to implement authorization? How would you use them?
OAuth will have you log in through a social account. This helps because then you're application doesn't store passwords at all, it takes your password by a token given from your account that is holding your password.

* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

An enum will help you define roles for your users in your application. You need to define role in your migration, and you would declare an enum in your user model.

* What are some strategies you can use to keep your views DRY?
You could user a presenter class for your models and keep your logic there.
