## Week One - Module 4 Recap

Fork this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. What's the most useful thing you learned from completing the intermission week work?

  The most useful thing I learned was how to approach learning a new language. I found it valuable to try to draw significant parallels between JavaScript and Ruby, and then learn the differences after I had established some common ground.

2. What are some tools to help debug JavaScript code?

  I mainly use pry, but there is also the native node debugger tool, along with google chrome's dev tools. Console logging also helps (although it's not as robust).

3. What are some tools you need in order to unit test your JavaScript?

  The tools I use are Mocha and Chai. Mocha allows your tests to be run inside of Node (and Node in turn allows you to run JavaScript outside of the browser), and Chai is an assertion library that allows for better unit testing assertions.

4. What is the syntax for invoking a function?

  In order to invoke a function, you must include parentheses after the function name like this: `someFunction();`.

5. What's the difference between `==` and `===` in JavaScript?

  The double equals sign can compare equivalent values that can be different data types, so this will return true: `3 == '3'`. The triple equals sign means that the values AND data types have to be the same, so this will return false: `3 === '3'`.

6. What's the difference between asynchronous and synchronous JavaScript?

  Asynchronous means that other functions can be executed while another function is waiting for a response. Synchronous is what we are used to in ruby, where functions must end before moving on to the next operation (or function call).

7. How do we setup a route when creating an API with Node and Express?

  Inside of `server.js` (which is comparable to a routes file in Rails or Sinatra) we can setup our routes for our app. The route for a get request to the root path would be written like so:

  ```javascript
  app.get('/', function(request, response) {
    // Code goes here...
  })
  ```
  In the above example, "app" is an instance of express and the "get" method can be used to create our get request. The path is specified by the first argument in the function, and the callback function passes in two variables (request and response) that can be used inside of the code block.


8. What do we use Knex for?

  Knex adds a layer of abstraction over our database. It includes built-in methods that allow for easier database interaction and queries.

9. What's `npm` and what do we use it for?

  Node Package Manager (abbreviated "`npm`") is used to download modules which allows us to incorporate different JavaScript libraries into our Node app.


#### Review  
10. What's the MVC design pattern? Describe each part of MVC?

  MVC stands for "Model, View, Controller." It's a design architecture that allows for single responsibility inside of a web application. When a user makes a request to our app, their request gets routed to the correct Controller (via some sort of routing file), which handles all requests with a similar function. The Controller then accesses the Model layer, which includes all methods associated with a particular object in our app, such as a users table. The Model also interacts with the database, usually via some sort of ORM (depending on the type of database the app is running on). The Model then returns its data to the Controller, and the Controller sends the data off to the View layer. The View is responsible for the front-end of the app and displays the information that we wish to display to the user, and that the user had hoped to access via their initial HTTP request. Sometimes the back-end can be extracted out into an internal API that we create, and the front-end can then consume these endpoints in order to display information in the browser.

11. What is AJAX? What are some benefits of using AJAX?

  AJAX stands for "Asynchronous JavaScript And XML." It allows for client-side requests to be made to the back-end without having to refresh the page. This allows for processes to occur in the background which might otherwise stall the user while navigating a website, and/or avoid lengthy page reloads every time the user interacts with a website in any way.

12. What's a background worker? When would we want to use a background worker?

  A background worker is any sort of operation that is running behind the scenes while a user is interacting with a website. It doesn't affect the performance of a webpage or the user's experience by forcing them to wait until the operation is completed. By utilizing a background worker, the user can continue to click and navigate around the website like normal, without having to wait on the operation to finish before they can continue.
