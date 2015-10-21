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

________________________________
Prev: [Lecture Outline](../README.md) | Next: [Express vs. Koa](./express-vs-koa.md)
