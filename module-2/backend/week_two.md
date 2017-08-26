## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

ActiveRecord is an object relational mapper(ORM). It allows Ruby objects to map to a database(postgresql in our case). The attributes of that Ruby object become the columns of that specific table in the database.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
.all
.find()
.where()
.first
.last

You have access to them because the Team class is inheriting from the ActiveRecord::Base class.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

Team.find(4).name
Team.where(owner_id: 4)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

@team.owners.where(owner_id: 4)

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

Teacher has_many students
Student belongs_to a Teacher

Teacher              Student
id----------         id
name       |         name 
department _________ teacher_id

6. Define foreign key, primary key, and schema.

- Primary Key is a unique identifier for a given table.
- Foreign Key is an attribute that sits on a second table to create the relationship to the first table's primary key.
- A schema is a layout of the attributes(columns) associated to a given table and their values(string,text,integer,date). Can be found in your database folder of your project directory.

7. Describe the relationship between a foreign key on one table and a primary key on another table.

I believe this answer is similiar to the previous one-> a foriegn key sits on a second table and is the unique id of the first table. That's how the relationship is created.

8. What are the parts of an HTTP response?

- A status line 
- A status code (100-informational, 200-success, 300-redirection, 400-client error, 500-server error)
- Header

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
.has_attribute?(attribute_name) = returns true if the attribute exists, false if it does not
.to_param = generates a clean url with the id and attribute name
.not(argument) = selects from table using WHERE + NOT
.reflect_on_all_associations = returns an array of all associations. You can specify if you want to reflect on :has_many,                                    :belongs_to, etc.
.has_secure_token(token) = generates a unique 24 character token

2. Name your three favorite ActiveRecord rake tasks and describe what they do.

rake notes = will search through code for comments beginning with FIXME, OPTIMIZE or TODO.
rake routes = shows all of the defined routes
rake doc:rails = will generate API docs in your application 

3. What two columns does `t.timestamps null: false` create in our database? 

created_at
updated_at

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
A School has_many teachers
A Teacher belongs_to a school

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
A primary key and foreign key

School         Teacher
id -----       id
name   |       name
city   |       grade
state  |______ school_id


6. Give an example of when you might want to store information besides ids on a join table.

To be honest, I don't have one. I thought the purpose of a join table was to normalize and keep the schema and db well designed.

7. Describe and diagram the relationship between patients and doctors.

Doctor has_many patients
Patient belongs_to a doctor

8. Describe and diagram the relationship between museums and original_paintings.

Museum has_many original_paintings
Original_paintings belong_to a musuem

9. What could you see in your code that would make you think you might want to create a partial?

Repetition in the views folder across different models. An example would be a form partial, where you're using a form template in your 'show' and 'new' html.erb files.
