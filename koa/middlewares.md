![YES](http://i.imgur.com/LbRrr.gif)
# Middlewares

Koa is essentially just an object containing an array of middleware generator functions. Middlewares is how you can really customize your Koa apps. Very pluggable since it works in a stack-like manner. It makes architecting your backend super fun!

![Middlewares](https://cloudup.com/crYO7MLyWKA+)

You can inject middlewares by simply using `.use()`. Remember that Koa works in a stack-like manner so the order of where you put the middleware in your code matters!

![Middleware order matters](https://cloudup.com/c217s4KwN_z+)

#### Resource

Check out some cool middlewares for Koa [here](https://github.com/koajs/koa/wiki).

________________________________

Prev: [Directory Structure](./directory-structure.md) | Next: [Set Up Mongo Database](./set-up-mongo-database.md) |
Home: [Lecture Outline](../README.md)
