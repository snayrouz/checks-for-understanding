1. How do we make flash messages display on a page?
In your application.html.erb file:
     <% flash.each do |name, msg| %>
      <div class="alert alert-success" role="alert">
        <%= content_tag :div, raw(msg), class: name %>
      </div>
    <% end %>
Then in your controller, specify a flash alert with flash[:alert] = "Message" in the controller action you'd like the a message. Typically destroy, update, create ,new.

2. Where is cart information/temporary information usually stored?
In a session

3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?

You wouldn't want the cart to persist to the database for the integrity of the data in the database. Meaning, people can leave items in their cart for a long period of time and they can expire. You wouldn't want bad data in your database.

If you were doing analytics on a particular item, it could be valuable to see how long an item was in a cart, or often a user puts a certain item in their cart. This could help with suggested items to the user in the future.

4. What is the purpose of the asset pipeline?

To store css,images, js for a project. If you worked at a large company, they could have an asset folder pertaining to their standards or their customer standards so you can work with that.

5. Why do we precompile our assets?

To streamline the request response cycle. 

6. What do each of the following tags do?

<%= stylesheet_link_tag "application" %>    this will look for a stylesheet to style your entire application
<%= javascript_include_tag "application" %> this will look for the JS that will be applied to your entire application
<%= image_tag "rails.png" %> . this will give your image a tag for accessibility. Similiar to img src

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

Table of Contents
What your project does
How to install it
Example usage
How to set up the dev environment
How to ship a change
Change log
Contributors

8. What are the top four accessibility issues that we as developers should be aware of?
Visual
Mobility
Cognition
Hearing

8. before_save is an example of a what? Where in our Rails application would we find a before_save?

callback
most likely in our application controller 

10. Given the following object, how would we create a scope for all users who are active?

User.create(name: "Happy", active: true)

class User < ActiveRecord
  scope :active, {where(active:true)}
end

11. What is the difference between a scope and a class method?
Scopes can be chained, class methods can be chained only if they return an object that can be chained
Scopes automatically work on has_many relationships
You can set up a default scope
