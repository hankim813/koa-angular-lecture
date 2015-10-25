![Party](http://i.imgur.com/e1GzZ.gif)
# Set Up Mongo Database

Let's quickly set up a DB to save users! Mongo is a no-sql database that is super easy to use since you can basically dump anything into a database. I encourage you to learn more about it!

## Installation

Download [MongoDB](https://www.mongodb.org/downloads#production).

We'll need to use `monk`, `co-monk`, and `password-hash` as well:

```
$ npm install --save monk
$ npm install --save co-monk
$ npm install --save password-hash
```

`monk` lets you easily interact with a mongo DB. `co-monk` is a wrapper that basically makes all the functions in `monk` return generator functions so that we can use `yield`! `password-hash` will be used to hash passwords of course.

database.js:

```js
/**
 * Module dependencies
 */

var db = process.env.MONGOLAB_URI || 'mongodb://localhost/api';
var monk = require('monk');

/**
 * Expose db
 */

module.exports = monk(db);
```

user.js:

```js
/**
 * Module dependencies
 */

var db = require('lib/db/database');
var wrap = require('co-monk');
var User = wrap(db.get('user'));
var passwordHash = require('password-hash');

/**
 * Expose `User`
 */

module.exports = User;
```
________________________________

Prev: [Routes](./routes.md) | Next: [Angular Intro](../angular/intro.md) | Home: [Lecture Outline](../README.md)
