# Express REST API

## ES6 Classes

Classes are in fact "special functions", and just as you can define function expressions and function declarations, in other words, they are templates for objects

#### Class expressions:

It is another way to define a class.

## Using Express Routing

Routing refers to how an application’s endpoints (URIs) respond to client requests.

### Route methods:

GET, POST(add), PUT(update), DELETE, ALL(for all HTTP request methods on the same path).
We can use them like: `app.get('path',handlePathFun);`.

## Express Routing

Router is like a mini-Express application.
Router doesn’t bring in views or settings but provides us with the routing APIs like:

- `.use`
- `.get`
- `.params`
- `.route`

### With Express Router we can:

- Use `express.Router()` multiple times to define groups of routes.
- Apply the `express.Router()` to a section of our site using `app.use()`.
- Use route middleware to process requests.
- Use route middleware to validate parameters using `.param()`.
- Use `app.route()` as a shortcut to the Router to define multiple requests on a route.
