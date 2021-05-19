# node-prep

##### Q: How many threads does Node have
> 1 thread (thread = an operation that is happening in the same time with another one)

##### Q: Is Node primarily a sync or async programming language
> In is asynchronous because the programmer should initiate a callback routine (https://github.com/mariusbanea/web-developers-toolkit/blob/master/js/functions/callback-function-example.html). This means he tells Node.js, “Hey Node. Guess what? Call me back if an error has occurred. If not give me the results and move on as fast as possible.” This is great if you are working with two or maybe three events one after the other. 

##### Q: Difference between the callback, closure, and recursive functions
> * callback function (function which has another function as parameter used to control the order in which functions get executed): https://github.com/mariusbanea/web-developers-toolkit/blob/master/js/functions/callback-function-example.html
> * closure function (function inside another function with the scope of protecting the scope of the inner function; used to handle sensitive data): https://github.com/mariusbanea/web-developers-toolkit/blob/master/js/functions/closure-example.js
> * recursive-function (function calling itself repeatedly; make sure to have some conditional to stop the recursion in order to avoid infinite loop): https://github.com/mariusbanea/web-developers-toolkit/blob/master/js/functions/recursive-function-example.js

##### Q: What is “callback hell”
> * If you are working with a large number of events, then initiating callbacks, with the proper error-trapping routines causes what has become known as “callback hell”. Simply put, the code, the programmer and the actual program, require an incredible amount of error checking to make sure everything is working correctly. (In coding language – you will overflow the stack.) 

##### Q: Difference between a SQL database and a NoSQL database
> * SQL stands for Structured Query Language, and is not a database in itself but rather a language for interacting with relational databases. 
> * https://github.com/mariusbanea/web-developers-toolkit/blob/master/databases/sql-vs-nosql-pros-and-cons.jpg

##### Q: What are the projects suitable for node
> Single thread websites with SQL DBs and API support

##### Q: What happens type a URL into your browser and hit enter
> Create the DOM which is copy of the code from the server is not the code of the server (cross browser, device and OS optimisation)
> * connect to the external server where the website is (ex: yahoo.com)
> * download all the files related to the website (html, css, images, fonts, javascript, etc.)
> * structure the files folder * file tree (check in web development tools → source tab)
> * read the code in order to display it as web design
https://medium.com/@maneesha.wijesinghe1/what-happens-when-you-type-an-url-in-the-browser-and-press-enter-bb0aa2449c1a and http://www.w3schools.com/js/js_htmldom.asp

##### Q: What are the parts of this url https://github.com/username/repository-name/folder-name/file-name?key=value&anotherKey=differentValue
> * http / https ===> the access protocol
> * github.com ===> domain name
> * username/reposiotry-name/folder-name/file-name ===> are parameters  / routes that we get to send to the domain name (the user sends only the values for each parameters and the key is preset)
> * /?key=value&anotherKey=differentValue ===> are usually query that we get to send to the domain name  (the user sends both the key and values for each query)
> * URLs structure: PROTOCOL + DOMAIN NAME + PARAMETERS + QUERIES

##### Q: What is the Express router?
> * Routing refers to determining how an application responds to a client request to a particular endpoint, which is a URI (or path) and a specific HTTP request method (GET, POST, and so on).
> * Each route can have one or more handler functions, which are executed when the route is matched. The Router objects keeps the application organized, with service objects being written for specific routes

##### Q: What is JavaScript object destructuring?
> * The destructuring assignment syntax is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables.
> * https://github.com/mariusbanea/web-developers-toolkit/blob/master/js/objects/destructuring-objects.js

##### Q: What are service objects used for?
> * Service object are useful for organizing your code
> * We can wrap related functions such as for a specific table in a database, a directory in the file system or related API calls
> * A service object helps us adhere to software development good practices such as SOC, DRY and encapsulation

##### Q: Describe MVC in NODE
> * Model is the Database. View is the Express server application, because it's what we directly interact with. Controller is Node itself, because it is managing the communication between Express and the Environment/Database.
> * https://github.com/mariusbanea/web-developers-toolkit/blob/master/node/node-mvc.pdf

##### Q: What are RESTfull web services
> * REST is a uniform standard for building web APIs. It stands for Representational State Transfer, with the central idea being to provide a client with a Representation of the State of an application that lives in the server's environment, as well as methods to perform CRUD operations on that application's State.
> * https://github.com/mariusbanea/web-developers-toolkit/blob/master/api/http-methods-for-restful-services.pdf

##### Q: What is middleware
> * Any function which a request 'passes through' in the Express server. A Middleware gets the Request Object, performs its defined function, then passes the Request Object on to the next Middleware.
> * https://en.wikipedia.org/wiki/Middleware

##### Q: What are the most common NPM packages you are using
> * Express, Morgan, CORS, Helmet, DotENV, XSS, KNEX
> * More packages can be found here: https://colorlib.com/wp/npm-packages-node-js/

##### Q: How would you explain server-side programming to a new developer
> A server-side web app is simply a program whose purpose is to expose resources (data, files, etc.) to other applications. Server side programming focuses on data persistence, security, software testing, business logic and dev ops.

##### Q: What is the Response <—-> Request data cycle in Node
> * request data flow (REQ, SEND): api call from the Front-end -> server.js (Node) -> app.js (Node) -> router.js (Node) -> service.js (knex) -> PG Database (DBeaver)
> * response data flow (RES): api response to the Front-end <- server.js (Node) <- app.js (Node) <- router.js (Node) <- service.js (knex) <- Database (DBeaver)

##### Q: Walk me through your workflow for deploying an application to production. What precautions do you take?
> * Test all new code
> * Ensure tests don't affect production databases
> * Ensure all secrets (keys/tokens etc) are hidden
> * Remove any unnecessary logs
> * Remove sensitive server error messages
> * App uses the PORT from environment
> * Correct usage of versions
> * Audit for security vulnerabilities in packages

##### Q: What is the correspondence between API calls vs CRUD operations
> https://github.com/mariusbanea/web-developers-toolkit/blob/master/api/http-methods-for-restful-services.pdf

##### Q: What is the structure of the PostgreSQL DB
> PostgreSQL has a list of tables which have table head for the structure and rows with individual data

##### Q: HTTP status codes in the 200, 300, 400, and 500
> https://github.com/mariusbanea/web-developers-toolkit/blob/master/api/http-status-codes-sheat-sheet.pdf

##### Q: How do you handle logs for your server? Can you describe a time when you found logging valuable?
> Using Morgan to log the HTTP layer, which can be configured for different levels of detail. Logging is helpful when debugging, as you can see which methods are being sent by a client and what response the server is sending.

##### Q: Difference between unit and integration tests?
> * Unit tests (a type of testing to check if the small piece of code is doing what it is suppose to do.) and 
> * integration test (a type of testing to check if different pieces of the modules are working together). 

##### Q: What tools do you use when creating a persistence layer, and why is that layer important?
> * PostgreSQL (db software), Knex (npm package which helps creating SQL queries inside the service files), Postgrator (npm package which helps with DB migrations and seeding). 
> * The persistence layer maintains the state of data. Without it, apps are volatile, and the data resets whenever the server restarts. The persistence layer allows a user to access the same data repeatedly, across sessions in the app.

##### Q: What are the typical files (and their roles) of a Node project 
> Example code here: https://github.com/mariusbanea/thinkful-node-postgres-boilerplate-app
> * server.js * controller code for the server with the api endpoints
> * package.json * json file with all project related settings and node modules necessary for it
> * public folder to hold all the view related files (index.html, js, css, fonts and images files)
> * test folder to hold all the files related to automatic testing
> * models folder containing the mongoose schemas and models
> * node_modules folder where all the modules in the package.json are installed
> * config.js file (or .env file) to hold the parameters related to he project database connection, special ports or url used in the project as well as the auth tokens
> * readme.md file for the project documentation
> * .gitignore file to exclude the files we don’t want to send to the github repository
> * app.js is the starting pint for the routes
> * postragtor-config.js * config files related to the migrations
> * .env * has the sensitive data related to the db connection details or auth tokens
> * *router.js * has the api endpoints grouped by functionality (ex: client-router.js)
> * *sevice.js * has the db connection scripts necessary for each router

##### Q: What are the main parts of a server js file
> * import external resources
> * server start and stop functions
> * api end points (app.get)
> * app listen with the port settings (app.listen)

##### Q: What commands lines do you use to setup a new node project
> * npm init (initialize the project and create and empty package.json)
> * npm install packge-name (install the necessary packages)
> * npm start (run the server without monitoring it)
> * nodemon server.js (run the server and monitors it)

##### Q: What are the benefits of bcrypt compared to other approaches.
> * Bcrypt uses salts to randomize the hashes which makes them more secure than non-salted hashing algorithms and encryption which is designed to be decrypted. Bcrypt is designed to be slow which prevents rainbow-table attacks and slows brute-force dictionary attacks.
> * SHA-2 family of hashes was designed to be fast. BCrypt was designed to be slow. Both are considered robust. With enough rounds or work-factor, either one can take longer than the other, but I would lean towards the one that was designed to be slow. (if server load is an issue, the Work Factor is adjustable). 

##### Q: What is difference between Salt and Hash
> * Salt = is the rule base of which the password get encrypted; 
> * Hash = use the encryption key to generate a encrypted password 
> * Example: if the initial password is “ABC”; the SALT is the rule to convert the initial password to the encrypted form (ex: every letter from he alphabet becomes the number equivalent starting with a = 1); and the HASH is the encrypted password “123”

##### Q: How the JSON Web Tokens work?
> Once the user is logged in, each subsequent request will include the JWT (which is stored in the local storage), allowing the user to access routes, services, and resources that are permitted with that token
https://jwt.io/introduction/

##### Q: What is an XSS attack and do you know any steps to take to prevent them?
> * XSS (Cross-Site Scripting) attacks occur when an attacker uses a web application to send malicious code, generally in the form of a browser side script, to a different end-user.
> * Sanitize your input. (Capstone we used a module to filter input from users to prevent XSS attacks.)

##### Q: What are environmental variables and what might you put in them?
> Environmental variables are variables that are set on the environment file on the server (.env) and are stored in the scope of the current project. By adding them to .gitignore file the DATABASE_URL, JWT_SECRET, API KEY, etc. will be hidden from public.


##### ======== SQL drills =====
> https://github.com/mariusbanea/web-developers-toolkit/blob/master/databases/postgres-cheat-sheet.md

##### ======== Coding challenges =====
#
##### Challenge 1: 
> modules require and object destructuring
In the modules/calculator.js, export an object whose properties are the functions add, subtract, multiply, divide using ES6 Object initialize shorthand. In the app.js require the calculator module assign the properties to variables using ES6 Object descrtucturing syntax.

> * `Solution 1`: 
>   * https://github.com/mariusbanea/thinkful-node-modules-require-and-object-destructuring/blob/master/modules/calculator.js and 
>   * https://github.com/mariusbanea/thinkful-node-modules-require-and-object-destructuring/blob/master/app.js


#
##### Challenge 2: 
> give an example of a PostgreSQL service for a pancake management app with  GET, POST, PUT and DELETE endpoints and give an example of a Node migration file content inside it as well 

> * `Solution 2`:  
>   * https://github.com/mariusbanea/thinkful-node-postgres-boilerplate-app


#
##### Challenge 3: 
> Write an example function that takes a callback function as an argument. Inside the function, invoke the callback and pass in a locally assigned variable (any value). Finally, call the example function, with a callback that logs out the provided argument.

> * `Solution 3`: 
>   * https://github.com/mariusbanea/web-developers-toolkit/blob/master/js/functions/callback-function-example.html


##### ======== testing strategies ====
> You’re given the task of testing the LinkedIn URI `/contacts`. It’s used across the LinkedIn product to return all sorts of information about a user’s contacts, such as their name, profile photos, and locations, and it’s crucial that it always work. Discuss how you would approach testing it. What’s important to test and what kind of tests would you write.
> * test if the page is accessible (in this case: the user is logged in first)
> * test if the page is not empty (in this case: the user has at least one contact) 
> * test if the page has the right content (in this case: the contact belongs to that user) 
> * test that all the content elements in the page are present (in this case: the contact container has the included elements (photo, name, job title, etc) ) 
> * niche scenarios (for example: contacts of contacts or inter-related contacts)
