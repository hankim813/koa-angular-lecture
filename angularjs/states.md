![]()
# States

Since every different route is still technically the same page, most of the Angular community like to think of the routes as "states".
We're going to be using [`ngRoute`](https://docs.angularjs.org/api/ngRoute). 

Let's define a simple state:

```js
.config(['$stateProvider', '$urlRouterProvider', function ($stateProvider, $urlRouterProvider){

		// Redirect all invalid routes to 
		$urlRouterProvider.otherwise('/');

		// Define states
		$stateProvider

			.state('sample', {
				url: '/',
				templateUrl: '../components/sample/index.html',
				controller: 'sampleController',
				controllerAs: 'sample'
			});
	}]);
```

`.state()` function takes the name of the state and an object with a few more advanced configurations.

## Nested Views
