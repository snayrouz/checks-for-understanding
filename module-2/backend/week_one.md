## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
GET - used to grab an object from the database
POST- used to post an object to the database
UPDATE- update attributes 
PATCH -update attributes
DELETE- delete an object

2. What is Sinatra?
DSL for Ruby web applications

4. What is MVC?
Models, Views, Controllers -> helps implement a user interface on a web application

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
(Guess) If anyone were to look at our code and want to understand how the MVC works, it's best to follow convention so that they can understand the application.

6. What types of variables are accessible in our view templates without explicitly passing them?
Instance variables

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    erb :index
  end
  ```
@count = 1
???? not too sure

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

name = Mr. Ed
erb :index(name: name)

9. What's the purpose of ERB?
It allows us to run Ruby methods on our html pages.

10. Why do I need a development AND test database?
You need a test database to create a small data set (usually 2-3 objects) to test functionallity of your code. You need a development database

11. What's responsive design?
Code that is designed to fit on to smart phones, tablets and desktops. It will also respond to the size of your browser and move the html/css around so that it fits to screen.

12. What is CRUD and why is it important?
CRUD stems from 4 sql commands, Create, Read, Update, Delete. It's important because it tells an application how to behave when opening files on the web.

13. What does HTTP stand for? 
Hypertext Transfer Protocol

14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<%= RUBY MAGIC %>
<h1> Ruby #{@magic.id} </h1>

15. What's an ORM?
Object Relational Map

16. What's the most commonly used ORM in ruby (Sinatra & Rails)?
Activerecord
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

get '/restaurants' (shows all restaurants)
post '/restaurants' (save to the database and renders to a 'show' or 'index')
get '/restaurants/:id (shows just one restaurant)
get '/restaurants/:id/new'(shows a new form to enter restaurant data)
get '/restaurants/:id/edit (shows one restaurant in an edit form)


18. What's a migration? 
Migration prepares your data base tables and produces your schema.

19. When you create a migration, does it automatically modify your database?
There are more steps. First you have to create the migration, then migrate the db, then seed the database so it normalizes your tables.

20. How does a model relate to a database?
The model holds the query to talk to the database directly

21. What's the difference between agile workflow and waterfall method?
Agile breaks up your workflow into pieces that allow you to write code, test, and

22. What is the difference between `#new` and `#create`?
'new' creates a new object while 'create' makes a new object and saves it to the DB

