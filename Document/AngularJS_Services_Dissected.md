## Context ##
> #### What is AngularJS Service ####
> #### Way to create AngularJS Service ####


## Content ##
### 1. What is AngularJS Service ###
AngularJS services are functions or objects that can hold behavior or state throughout application. They are used to implement shared behavior/reusable logic which can be used by other components in your AngularJS application.

AngularJS services are **singletons**, means each service is instantiated only once, so each part of our application gets access to the same instance of the AngularJS service. AngularJS services are **lazily instantiated**, means Angular only instantiates a service when an application component who depends on it, gets loaded.

Do note that AngularJS services are different than AngularJS controllers. Controllers are created and destroyed several times while navigating to different views, but services are instantiated only once and then reused everywhere in application.

**Common use of Services**: Communicating with Server, Repeated behavior, Reusable business logic, application-level stores, shared state, etc.

### 2. AngularJS Service & Dependency Management ###
The whole AngularJS service concept is driven by [AngularJS Dependency Injection system](https://github.com/gregecho/AngularjsLearning/blob/master/Document/AngularJS_Dependency_Injection.md). Any service can be injected into another service, controller or directive, by just declaring it as a dependency, and AngularJS will do the rest.

### 3. Ways to create custom AngularJS Service ###
$log, $window, $location, $http are few examples of built-in services. A built-in AngularJS service name starts with $.

An AngularJS service can be implemented as a factory, service, or provider.

#### 3.1 Factory ####
A Factory is created using **module.factory** function. It is useful if you follow a functional style of programming and you prefer to return functions and objects.

> [ Create Service via Factory][1]

[1]: https://github.com/gregecho/AngularjsLearning/tree/master/AngularjsDemo1/Service_Factory.html

#### 3.2 Service ####
A Service is created using **module.service** function.It is useful if you follow a Class/OO style of programming, where we define classes and types instead of functions and objects. With service, the function definition is actually a class/type, and **AngularJS calls new on it to create an instance of it**.

In this case, our service definition function is now a JavaScript function. It doesn't return anything. AngularJS will perform **new GreetingService()** (iva DI), cache it , and then return that instance to all components that depends on GreetingService.

> [ Create Service via Service][2]

[2]: https://github.com/gregecho/AngularjsLearning/tree/master/AngularjsDemo1/Service_Service.html

### 4. Constant & Value ###
Angular provides us ways to define data that remains globally avaiable while not really polluting the global namespace. Constant and Values are our options to define globally available data, which can be injected as a dependency into other service or controller.

Difference between Constant & Value:
>+ A constant can be injected everywhere. The value of a constant is not meant to be changed, and should never be changed.
>+ A Value can be changed. A value can not be injected into config phase of application.

```javascript
var app = angular.module('myApp', []);
app.constant('PI', 3.14);
app.value('loggedinUser', 'SAM');

app.controller('AppController',['PI', 'loggedinUser', function(PI,loggedinUser){
    var self = this;
    self.r = 2;
    self.getArea = function(){
        return PI * r * r;
    };

    self.printMessage = function(){
        return 'Welcome' + loggedinUser;
    }
}]);
```



-----
### TODO

* [ ] Read following artical ["AngularJS Dependency Injection"](https://docs.angularjs.org/guide/di).
