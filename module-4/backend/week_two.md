## Week Two - Module 4 Recap

Fork this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. What is Webpack and why is it useful?

  Webpack is a build tool or package manager that takes all of our files, runs them through pre-processors, and makes our human-readable code more efficient and readable for the browser in production.

2. When do you want to use event delegation?

  Event delegation is useful when we want to add things to the DOM that were not there on page load. Since the browser won't know if these newly-added elements, we delegate the events to their parent node, which WERE created when the page loaded.

3. What's one difference between ES5 and ES6?

  ES6 has two new ways to declare variables--`const` and `let`--which essentially replace `var`. The former is useful when you do not expect the variable to change, and the latter is used when you do.

4. How are you using the MVC design pattern in your Quantified Self project?

  Right now we separated out our routes to different Express routers. We currently do not have controllers set up, but we're aware that they would be useful in imitating the MVC structure of a Rails app, for example. We are utilizing models, however, and created separate files for Food, Meal, and MealFood. Obviously these files include our link to the Postgres database, which we coordinate through knex. Finally, the views portion of the MVC structure is handled through our front-end, which uses HTML, CSS, and JavaScript, and communicates to our back-end via AJAX calls and DOM events.

5. How do you execute raw SQL in node?

  We are currently using knex to handle our raw SQL queries. Inside of our models, we have various functions that make queries to our database using the database.raw function included in knex.

6. What's a callback function and what are some reasons when we use/need callback functions?

  Callback functions are functions that are executed inside of another function, and do not have to be invoked immediately. Often when passing functions as arguments, it allows for our code to become DRYer and more modular in that we can separate out smaller operations into separate bits of code that execute only one task.

7. What is CORS?

  CORS stands for Cross Origin Resource Sharing, and is used to make requests and responses to external resources. Typically a website does not allow just anyone to access their resources on their site due to security reasons, but they can choose to allow certain requests as they see fit via CORS.

8. What are some steps to avoid CORS?

  On the back-end, you can set the headers so that the API endpoints can be consumed from other origins. Inside of your server file, you can set the header to "Access-Control-Allow-Origin" using express functions.


#### Review  

9. Why do people say "HTTP is stateless"?

  The HTTP request/response cycle is stateless because data does not persist between the client and the server after the connection has been closed. It's as if--upon back-to-back requests--the client and server are unaware that they've ever communicated to each other previously. There are ways however to maintain this connection and keep it open so that data can be transferred back and forth multiple times. The WebSockets protocol is one such way, and allows the connection between client and server to be left open. Chat rooms can be built via WebSockets, for example.

10. What is a RESTful API?

  A RESTful API is a service that provides access to its content via a set of agreed-upon standards and methods (in this case GET, POST, PUT, and DELETE HTTP methods). We can think of an API as a black box where external users of the service do not have access or knowledge of what's going on internally, but are given standard, expected ways of interacting with the black box in the form of HTTP paths and verbs.

11. What are some main characteristics of a team following an agile workflow?

  A team following an agile workflow aims to implement features in an iterative manner. They are open to change, willing and able to adapt to a client's requirements because they are constantly getting feedback from them and using that to reorient their design process. Communication, collaboration, and delivering a working product are paramount in an agile environment.

12. What are some advantages/disadvantages to using OAuth to authenticate a user?

  Using OAuth is advantageous because it makes logging into a site easier--you only have to store your user information on one site that can then be accessed by others. It's also better for security--if you trust the website where your information is stored then you can feel more confident about browsing other sites because they don't have access to your personal/financial data. However, the websites that you use OAuth for now have access to some of your social media information such as profile info, friends, and photos, so you have to choose what information you want to share with them. Finally, if your account that you use for OAuth gets hacked, all the other sites you have linked to that account are potentially vulnerable as well.
