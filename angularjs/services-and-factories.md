![Request](http://img.pandawhale.com/post-38727-NPH-I-request-the-highest-of-f-pZqj.gif)
# Services and Factories

Utilizing services and factories really allows you to build modular, composable, and pluggable web application. 
Factories are generally used basically for a lot of CRUD operations. Services is how you store and pass around the current state of app's information, such as user data.

You can inject services and factories where you need them!

The general communication between controllers, services, and factories should be:

> controllers --- ask ---> services --- ask ---> factories

So you should only inject factories into services and you should only inject services into controllers.

The common scenario is that a controller needs some information, say.. the current user data. The controller would ask the service for this information. If the service does not already have the current user data, it would then ask the factory to fetch that data from your database. Once the factory returns the user data, the service would save this data and then return to the controller.

Let's take a look at a sample pair of services and factories:

```js
// service.js

angular
  .module('app')
  .factory('userService', ['userFactory', function(userFactory){
    function fetchUser () {
      return userFactory.getUser();
    }
    
    return {
      user: fetchUser
    };
  }]);
```

```js
// factory.js

angular
  .module('app')
  .factory('userFactory', ['$http', function($http){
    function getUser() {
      // make ajax call to DB
    }
    
    return {
      getUser: getUser
    };
  }]);
```


________________________________

Prev: [Controllers](./controllers.md) | Next: [Directives](./directives.md) |
Home: [Lecture Outline](../README.md)
