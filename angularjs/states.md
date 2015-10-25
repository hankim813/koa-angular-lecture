![Big Deal](https://s-media-cache-ak0.pinimg.com/originals/7e/a6/fb/7ea6fbd43cad1f8f376bc982b9bae5a2.gif)
# States

Since every different route is still technically the same page, most of the Angular community like to think of the routes as "states". Today, we'll be using the fan favorite, [`ui-router`](https://github.com/angular-ui/ui-router), to configure our states.

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

`url`: The address you'll see for that state in the browser.
`templateUrl`: Define the HTML template you want to render for this state.
`controller`: Define the name of the controller that will be in charge of the state.
`controllerAs`: An alias for the controller within your view. 

## Nested Views

You can have parent and children views by nesting the states:

```js
.state('parent', {
	url: '/parent'
})

	.state('parent.child', {
		url: '/child' // this will render as 'parent/child'
	})
```

The `url` of the parent state will always prepend the `url` of the child states. In the HTML of the parent state, you must have `ui-vew` element to render it's child states:

```html
<div ui-view></div>
```

## Challenge

Let's build a parent state for the navbar. 

________________________________

Prev: [Dependency Injection](./dependency-injection.md) | Next: [Controllers](./controllers.md) |
Home: [Lecture Outline](../README.md)
