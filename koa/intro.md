![Koa Logo](https://cloudup.com/c6Rd4cuYxpR+)
# Intro

[Koa](http://koajs.com/) is a new web framework designed by the team behind Express, which aims to be a **smaller**, more **expressive**, and more **robust** foundation for web applications and APIs. Through leveraging generators Koa allows you to ditch callbacks and greatly increase error-handling. Koa does not bundle any middleware within core, and provides an elegant suite of methods that make writing servers fast and enjoyable.

## Dependencies

#### node 0.11.x or higher

Koa needs to be running `node 0.11.x` or higher so that we can use the `--harmony` flag. Would highly recommending using [n](https://github.com/visionmedia/n), a simple node version manager to quickly install the right `node` version.

```
$ npm install -g n
$ n 0.11
$ node --harmony my-koa-app.js
```

## What is it?

A Koa application is an object containing an array of middleware generator functions which are composed and executed in a stack-like manner upon request. Koa is similar to many other middleware systems that you may have encountered such as Ruby's Rack, Connect, and so on - however a key design decision was made to provide high level "sugar" at the otherwise low-level middleware layer. This improves **interoperability**, **robustness**, and makes writing middleware much more **enjoyable**.

This includes methods for common tasks like content-negotiation, cache freshness, proxy support, and redirection among others. Despite supplying a reasonably large number of helpful methods Koa maintains a small footprint, as no middleware are bundled.

Boot it up in six lines of code:

```js
var koa = require('koa');
var app = koa();

app.use(function *(){
  this.body = 'Hello World';
});

app.listen(3000);
```

#### Source: http://koajs.com/
________________________________

Prev: [Lecture Outline](../README.md) | Next: [Express vs. Koa](./express-vs-koa.md)
