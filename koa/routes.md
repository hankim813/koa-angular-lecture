![Parks and Rec](https://i.imgur.com/BTdpA9d.gif)
# Routes

Let's talk about some routes! :boom:

We're going to use `koa-route`, which is a dead simple router.

## Installation & Usage

```
$ npm install --save koa-route
```

```js
var router = require('koa-route');

app.use(router.get('/', function *(next){
    this.request; // this is koa request
    this.response; // this is koa response
}));
```

Koa's `request` and `response` objects are abstractions on top of node's vanilla request/reponse object, providing additional functionality that is useful for every day HTTP server development.

## Challenge

Build a RESTful `POST` route for `/users` that accepts user registration data.

________________________________

Prev: [Middlewares](./middlewares.md) | Next: [Set Up A Mongo Database](./set-up-a-mongo-database.md) | Home: [Lecture Outline](../README.md)
