## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?

rails new project_name -T -d postgresql --skip-spring --skip-turbolinks

2. What do Models generally inherit from in rails?

Application Record

3. What do Controllers generally inherit from in a rails project?

Application Controller

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

resources :horse, only: [:show]

5. What rake task is useful when looking at routes, and what information does it give you?

rake routes-shows you the HTTP Verb, Path, & Controller#Action based on your routes.rb file

6. What is an example of a route helper? When would you use them?

horse_path(horse) You would use this in a view to help routes pages correctly, in this case, to a show a specific horse.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

A _url will be what's shown in the browser, _wile path will be a helper in your page views to help route pages together.

8. What are strong params and why are the necessary?

THey set the parameters on which attributes need to be present/required to update data for that model.

9. What role does `form_for` play in helping us create our forms?

form_for is a form helper rails that renders a form in html in your brower view

10. How does `form_for` know where to submit the user's input?

When form_for is used, the HTML rendered shows the verb, action and path where that data will be submitted.

11. Create a form using a `form_for` helper to create a new `Horse`. 

<h1>New Horse:</h1>

<%= form_for @horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  
  <%= f.label :breed %>
  <%= f.text_field :breed %>
  
  <%= f.label :notes %>
  <%= f.text_area :notes %>
  
  <%= f.submit %>
<% end %>


12. Why do we want to validate our models?

When a user wants to upload data about an object, its best practice to validate attributes that would be required for data analysis. Some attributes of a model don't need to be validated but probably won't be used for data analysis.
