![Power Rangers](http://30.media.tumblr.com/38512230168dfe85a34042a7c60b5f37/tumblr_n5aaqxKSQ51r0j0yso4_400.gif)
# Controllers

Here's where things get fun. Controllers are how we connect the model and the view. Here's a sample controller:

```js
angular
  .module('app')
  .controller('someController', ['someDependency', function(someDependency){
    var vm = this;
  }]);
```

## Two Way Data Binding

This is probably the coolest thing about Angular as well as why I really like the MV* structure. Your view is always in sync with the data in
your controller!


```js
// state.js

.state('sample', {
		url: '/',
		templateUrl: 'view.html',
		controller: 'someController',
		controllerAs: 'dbc'
});
```


```js
// controller.js

.controller('someController', ['someDependency', function(someDependency){
    var vm = this;
    
    vm.data = 1;
    vm.addOne = addOne();
    
    function addOne(){
      ++vm.data;
    }
}]);
```


```html
<!-- view.html -->
<div>
  {{ dbc.data }}
  
  <button ng-click="dbc.addOne()">Add 1!</button>
</div>

```
____________________
Prev: [States](./states.md) | Next: [Services & Factories](./services-and-factories.md) |
Home: [Lecture Outline](../README.md)
