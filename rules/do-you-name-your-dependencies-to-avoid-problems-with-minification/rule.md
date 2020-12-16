---
type: rule
archivedreason: 
title: Do you name your dependencies to avoid problems with minification?
guid: a234f979-bc20-4415-8e9a-caf2b9cfc4fc
uri: do-you-name-your-dependencies-to-avoid-problems-with-minification
created: 2014-10-07T14:42:09.0000000Z
authors:
- id: 37
  title: Ben Cull
related:
- do-you-know-the-common-design-patterns-part-2---example

---

Angular uses parameter names to determine which dependencies to inject. When you minify your angular code, the parameter names are changed, so you must name your dependencies to ensure they work correctly. 
<!--endintro-->


The standard way to inject your dependencies looks a little like the following. We're defining a controller in this case.


```
phonecatApp.controller('PhoneListCtrl', function ($scope, $http) {...}
```



::: bad
Bad Example: This code will break when minified
:::






When this code is minified the parameters are renamed. This means that the dependency injector no longer knows which services to inject.




You can fix this in two ways. The first one uses the $inject property to identify the name of the parameters in order:



```
function PhoneListCtrl($scope, $http) {...}
PhoneListCtrl.$inject = ['$scope', '$http'];
phonecatApp.controller('PhoneListCtrl', PhoneListCtrl);
```



::: good
Good Example: This code names the parameters using the $inject property
:::






The second and preferred option is to pass an array containing the names, followed by the function itself. Take a look:



```
phonecatApp.controller('PhoneListCtrl', ['$scope', '$http', function($scope, $http) {...}]);
```



::: good
Better Example: This code names the parameters inline which is a little cleaner

:::






Using this method will ensure you don't run into problems with minification. If you'd like to read more, check out the [Angular tutorial for Dependency Injection](https&#58;//docs.angularjs.org/tutorial/step_05).