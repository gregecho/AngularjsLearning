## Context ##
> #### What is $http ####
> #### What is $resource ####
> #### $http VS $resource ####
> #### Way to create AngularJS Service ####


## Content ##
### 1. What is $http ###
AngularJS **$http** service allows us to communicate asynchronously with server endpoints using XHR [browser's XMLHttpRequest Object] API. $http is designed for general purpose AJAX calls that can deal with both RESTful & Non-RESTful API on your server. $http can be treated somewhat equivalent to jQuery.ajax.

The $http API is based on the deferred/promise APIs exposed by the $q service which is an implmentation **Promise** interface.

The Promise API comes with following flow:
>+ Each asynchronous task will return a promise object.
>+ Each promise object will have a **then** function that can take two arguments, a **success handler** and an **error handler**.
>+ Then success or the error handler in the then function will be called only once, after the asynchronous task finish.
>+ The then function will also return a promise, to allow chaining multiple calls.
>+ Each handler (success or error) can return a value, which will be passed to the next function in the chain of promises.
>+ If a handler returns a promise(make another asynchronous request), then the next handler(success or error) will be called only after that request is finished.

````javascript
// Simple GET request example :
$http.get('/someUrl').
  then(function(response) {
    // this callback will be called asynchronously when the response is available
  }, function(response) {
    // this callback will be called asynchronously if an error occurs or server returns response with an error status.
  });
````



### 2. What is $resource ###
AngularJS **ngResource** module provide built-in support for interacting with RESTful services asynchronously, via **$resource**. $resource is a high-level abstraction on low-level $http service used for asynchronous server communication.



### 3.$http VS $resource ###
>+ Everything that can be done by $resource can be done by direction using $http.
>+ $http is designed for general purpose AJAX calls that can deal with both RESTful & Non-RESTful API on your server. 
>+ $resource is designed special to work with RESTful API.

> Note: $resource call can take several parameters. Full syntax of $resource invocation is as follows:
$resource(url, [paramDefaults], [actions], options);

A resource object with methods for the default set of resource actions optionally extended with custom actions. The default set contains these actions:
````json
{ 
  'get':    {method:'GET'},
  'save':   {method:'POST'},
  'query':  {method:'GET', isArray:true},
  'remove': {method:'DELETE'},
  'delete': {method:'DELETE'} 
  };
````


**$resource** code snippet:
````javascript
var User = $resource('/user/:userId', {userId:'@id'});
var user = User.get({userId:123}, function() {
  user.abc = true;
  user.$save();
});
````

**$http** code sinppet:
```javascript
$http.post('http://localhost:8080/SpringMVC4RestAPI/user/', user)
            .then(
                    function(response){
                        return response.data;
                    }, 
                    function(errResponse){
                        console.error('Error while creating user');
                        return $q.reject(errResponse);
                    }
            );
```

You can also access the raw $http promise via the $promise property on the object returned:
````javascript
var User = $resource('/user/:userId', {userId:'@id'});
User.get({userId:123})
    .$promise.then(function(user) {
      $scope.user = user;
    });
````

Demo:

> [ AngularJS $http service example-server communication][1]

[1]: https://github.com/gregecho/Spring4MVCHelloworldDemo/tree/Spring4Mvc-Angularjs-Communicate-using-service/src/main/webapp/static/js


----
### References
* [AngularJS $resource](https://docs.angularjs.org/api/ngResource/service/$resource)



-----
### TODO

* [ ] Read following artical ["AngularJS Dependency Injection"](https://docs.angularjs.org/guide/di).

* [ ] ["jQuery.Deferred对象"](http://javascript.ruanyifeng.com/jquery/deferred.html)

* [ ] 基于Deferred实现的弹出窗口
