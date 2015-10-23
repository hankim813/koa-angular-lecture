![YES](http://i.imgur.com/LbRrr.gif)
# Middlewares

Koa is essentially just an object containing an array of middleware generator functions. Middlewares is how you can really customize your Koa apps. Very pluggable since it works in a stack-like manner. It makes architecting your backend super fun!

You can inject middlewares by simply using `.use()`. 

![Middlewares](https://cloudup.com/cgwVFsPkmec+)

Remember that Koa works in a stack-like manner so the order of where you put the middleware in your code matters!

![Middleware order matters](https://cloudup.com/c217s4KwN_z+)

You can move onto the next middleware in line by:

```js
yield next;
```

You can see the cascading effect of how Koa's middlewares goes downstream then back upstream:

![Koa Cascading](https://cloudup.com/cEv9rbmqLjd+)
![Terminal Output](https://cloudup.com/cG_udanh4_Y+)

#### Resource

Check out some cool middlewares for Koa [here](https://github.com/koajs/koa/wiki).

________________________________

Prev: [Directory Structure](./directory-structure.md) | Next: [Routes](./routes.md) | Home: [Lecture Outline](../README.md)
