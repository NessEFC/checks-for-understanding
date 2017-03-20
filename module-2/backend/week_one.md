## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.

* GET - retrieves (read) data
* PUT - updates or edits data
* POST - creates new data
* DELETE - removes data
* ? - 

2. What is Sinatra?

Sinatra is a light-weight web development framework and domain-specific-language (DSL) developed for Ruby.

4. What is MVC?

MVC stands for model, view, controller, and is used to separate out specific tasks of a web app.

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

Sinatra is looking for specific syntax within each route, and following conventions also allows others to view and/or edit our code, providing some universality to our apps.

6. What types of variables are accessible in our view templates without explicitly passing them?

Instance variables created in each distinct route method.

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  
  ```ruby
  get '/horses' do
    name = 'Mr. Ed'
    erb :index, locals: {name: 'Mr. Ed'}
  end
  ```

9. What's the purpose of ERB?

ERB allows you to use Ruby code inside of a view alongside your HTML and CSS.

10. Why do I need a development AND test database?

A test database allows you to test light-weight, smaller scenarios to make sure your code works without having to use large datasets. Development databases allow you to mimic production scenarios with large datasets, but you know what to expect out of your data.

11. What's responsive design?

Responsive design deals with re-sizing of browser windows, or using different mobile devices, and making sure that the web-page stills behaves as you expect.

12. What is CRUD and why is it important?

CRUD stands for Create, Read, Update, and Delete, and represents the four major functions of a database app. It's important because if followed, it allows for full web app functionality.

13. What does HTTP stand for?

HTTP stands for HyperText Transfer Protocol.

14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

* <%= %>, inserts code
* <%  %>, does not insert code?...

15. What's an ORM?

ORM stands for Object-Relational-Mapping, and ActiveRecord is an ORM built in Ruby primarily for the Rails framework. It's used to handle database actions and functions.

16. What's the most commonly used ORM in ruby (Sinatra & Rails)?

ActiveRecord

17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

* get '/restaurants' - read all restaurants
* get '/restaurants/new' - read the page for adding a new restaurant
* post '/restaurants' - create the new restaurant
* get '/restaurants/:id/edit' - read the edit page of a single restaurant
* put '/restaurants/:id' - edit the page of a single restaurant
* get '/restaurants/:id' - read the page of a single restaurant
* delete '/restaurants/:id' - delete the page of a single restaurant

18. What's a migration?

A migration is needed every time there is a change to the database.

19. When you create a migration, does it automatically modify your database?

No, you have to run rake db:migrate.

20. How does a model relate to a database?

The model is the file that actually communicates with the database. It can perform functions on tables and retrieve information, delete information, etc.

21. What's the difference between agile workflow and waterfall method?

Agile workflow combines all aspects of the project into smaller iterations, working on each in parallel. Over time, these small iterations add up to a large working product. The waterfall method essentially tries to complete the entire project in one single iteration, from concept to finished product.

22. What is the difference between `#new` and `#create`?

New will make an instance in a table but not save it. Create combines the #new and #save method into one, allowing you to create and save an instance in a table in one method.
