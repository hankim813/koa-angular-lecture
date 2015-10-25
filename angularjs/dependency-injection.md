![I need you](http://media.giphy.com/media/k9H5YJMoFF0tO/giphy.gif)
# Dependency Injection

One key aspect of Angular as a framework is how it relies on dependency injection. There are few places you need to "inject" dependencies:

The `index.html`:

```html
<!-- Angular Packages -->
<script src="vendors/angular-ui-router.min.js"></script>
<script src="vendors/ngStorage.min.js"></script>
<script src="vendors/angular-cookies.min.js"></script>
```

The Angular Module:

```js
angular
    .module('app', [
        'ui.router',
        'ngStorage',
        'ngCookies'
    ])
```

Functions of the module:

```js
.config(['$stateProvider', '$urlRouterProvider', function ($stateProvider, $urlRouterProvider){ }]);
```

*Note*: that the order of your dependecy injections must be the same as the order of the function parameters! :boom:

Dependency injection allows Angular to be modular and makes your code cleaner and pluggable :)
________________________________

Prev: [Directory Structure](./directory-structure.md) | Next: [States](./states.md) |
Home: [Lecture Outline](../README.md)
