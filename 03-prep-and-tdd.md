# Read03
* Answer the question.
* Review: ES6 Classes.
* Using Express Routing.
* Express Routing.

### *Answer the question*
- Q1 : 1) In one scenario you can identify the currently logged in user, so using the custom middleware fetches the user through a set of authentication steps.
2) A second example is changing the functionality on your response object, such as creating a new header. I could foresee a company doing that to advertise a sale of a product.
3) Building on the fact that a user logs in, the custom middleware can be uses to also validate a users data. The users information and credentials could be stored in a database to verify the information is correct.
- Q2 : True
- Q3 : Middleware could be built as so when a set of parameters are requested within a webpage it bypasses a response cycle and overlay’s a set of data.
- Q4 : Middleware is usually injected during a req and before a response cycle, this means that middleware is a dependency and the req and res cycle depend on the middleware to take place.
- Q5 : If a return statement is used in a function body, the execution of the function is stopped. “What happens in the function,Using Express Routing stays in the function”.

### *Review: ES6 Classes*

Classes are a template for creating objects.Classes in JS are built on prototypes but also have
some syntax and semantics that are not shared with ES5 class-like semantics.

For more details see [Review: ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes).

### *Using Express Routing*
Routing refers to how an application’s endpoints (URIs) respond to client requests. For an introduction to routing.

You define routing using methods of the Express app object that correspond to HTTP methods:
- app.get() to handle GET requests 
- app.post to handle POST requests.
- use app.all() to handle all HTTP methods 
- app.use() to specify middleware as the callback function.

For more details see [Using Express Routing](https://expressjs.com/en/guide/routing.html).

### *Express Routing*
It is a mini express application without all the bells and whistles of an express application, just the routing stuff. Let’s take a look at exactly what this means. We’ll go through each section of our site and use different features of the Router.

- Use express.Router() multiple times to define groups of routes
- Apply the express.Router() to a section of our site using app.use()
- Use route middleware to process requests
- Use route middleware to validate parameters using .param()
- Use app.route() as a shortcut to the Router to define multiple requests on a route

For more details see [Express Routing](https://www.digitalocean.com/community/tutorials/learn-to-use-the-new-router-in-expressjs-4).

