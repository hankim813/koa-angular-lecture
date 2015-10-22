![Cute Fight](http://ak-hdl.buzzfed.com/static/2013-10/enhanced/webdr06/14/10/anigif_enhanced-buzz-1726-1381761781-16.gif)
# Express vs. Koa

Philosophically, Koa aims to "fix and replace node", whereas Express "augments node". Koa uses co to rid apps of callback hell and simplify error handling. 

Koa exposes its own this.request and this.response objects instead of node's `req` and `res` objects.

Express, on the other hand, augments node's `req` and `res` objects with additional properties and methods and includes many other "framework" features, such as routing and templating, which Koa does not.

Thus, Koa can be viewed as an *abstraction* of node.js's `http` modules, where as Express is an application *framework* for node.js.

| Feature           | Koa | Express |
|------------------:|-----|---------|
| Middleware Kernel | ✓   | ✓       |
| Routing           |     | ✓       |
| Templating        |     | ✓       |
| Sending Files     |     | ✓       |
| JSONP             |     | ✓       |

## TLDR -- How is Koa different?

#### Generated-based control flow

- No callback hell.
- Better error handling through try/catch.
- No need for domains.

#### Koa is barebones

- Koa does not include any middleware.
- Routing is not provided.
- Many convenience utilities are not provided. For example, sending files.
- Koa is more modular.

#### Koa abstracts node's request/response

- Less hackery.
- Better user experience.
- Proper stream handling.

#### Source: http://koajs.com/
________________________________

Prev: [Express vs. Koa](./express-vs-koa.md) | Next: [Boot it up](./boot-it-up.md)
Home: [Lecture Outline](../README.md)
