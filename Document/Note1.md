## Context ##
> #### What is AngularJS and Advantages ####
> #### Bootstrap AngularJS ####
> #### Data binding ####
> #### AngularJs Modules ####
> #### AngularJS Controllers ####
> #### A quick summary on scope ####

## Content ##
### 1. What is AngularJS and Advantages ###
AngularJS is a client side MVC framework, which 
+ Provides a framework and api to develop modular applications.
+ Provides well defined structure to your applications.
+ Separation of concerns. Each functionality of project belongs to a specific concern(data, view, business logic).
Advantage:
+ Separation of concerns(Benefit by MVC)
+ Fewer lines of code
+ Pure HTML templates(Benefit by Model-View-Controller)
+ Testability(Benefit by MVC)
+ Smooth Integration with 3rd party libraries

### 2. Bootstrap AngularJS ###
An AngularJS application is bootstrapped using ng-app directive.It refers to the part of your HTML which will be controlled/managed by AngularJS.

### 3. Data binding ###
The ng-model directive is used with input fields to get access to the user input inot JavaScript variables.
ng-bind and the double-curly notation{{}} are almost same and can be used interchangeable. ng-bind & {{variable }} notation are used to get the value from the variable referred by ng-model and display that value in the tag ng-bind is applied on [or on the place {{ variable }} is used], and keeping the value up to date if it changes.

### 4. AngularJs Modules ###
A module in AngularJS can be thought of as packages in Java.It's the container for the different parts of an application-controller, services, filters, directives, etc.
+ A module can define it's own controllers, services, filter, directives, etc which will be accessible throughout the module.
+ A module can depend on other modules.
+ A module can be used by AngularJS to bootstrap an application. By passing the module name to ng-app directive, we can tell AngularJS to load this module as the main entry point for the application.

#### 4.1 Define a Module with no dependencies ####
In angularJS, amodule is defined or called using **angular.module** function.

    angular.module('myapp', []);

The first argument is the module name, 'myApp'. The second argument is an array of module names that this module depends on.

#### 4.2 Define a Module with dependencies ####

    angular.module('myApp', ['ui.bootstrap', 'ngResource']);

It means all the functionalities available in 'ui.bootstrap' & 'ngResource', will be accessible throughout module 'myApp'.

#### 4.3 Load an existing Module ####
If we just want to load an existing module defined elsewhere, call module function with only one parameter which is name of module.

    angular.module('myApp');

### 5. AngularJS Controllers ###
AngularJS controllers can be considered as the driver for Model and View changes. Their core responsibilities includes:
+ Providing Data to UI.
+ Managing presentation logic, such as which element to show/hide, what style to apply on them, etc.
+ Handling user input, such as what happens when a user clicks something or how a text input should be validated.
+ Processing data from user input to be sent to server.

#### 5.1 Basic Syntax ####
+ Controllers are created as part of a module.
+ Once we have a module, we can create a controller using the **controller** function on the module.
+ controller function takes two arguments. First is the name of Controller, and the second argument is controller definition function which contains the actual logic of controller.

    angular.module('myApp',[])
    .controller('AppController', [function(){
        var self = this;
        self.name = 'test';
    }]);

Or if the module is defined elsewhere:

    var App = angular.module('myApp', ['ui.bootstrap', 'ngResource']); // in some file
    App.controller('AppController', [function(){
        var self = this;
        self.name = 'test';
    }]);

#### 5.2 Controller with Dependencies ####
In below example, our controller depends on few built-in AngularJS services.
+ First we need to add the dependencies as strings in th array (this is known as 'safe style of Dependency Injection').
+ Then we will inject them as variables(we can give it any name) into the function that is passed as the last argument in the array.

AngularJS will pick up the individual strings in the array, look up the services internally, and inject them into the function in the order in which we have defined the strings. Once the services are injected, we can use them within our controller.

      var App = angular.module('myApp', ['ui.bootstrap', 'ngResource']); // in some file
      App.controller('AppController', ['$log', '$location', function($log, $location){
            var self = this;
            self.sayHello = function(){alert('say hello');}
            $log.log('I am starting');
            $location.path("/newpath");
      }]);

#### 5.3 How to use a controller in UI? ####
Using **ng-controller** directive.

    <body ng-controller="AppController as ctrl">
    <label>Name :</label><input type="text" ng-model="ctrl.name" placeholder="Enter your name"/><br/><br/>  
    <span ng-bind="ctrl.name"></span><br/><br/> 
    <button ng-click="ctrl.sayHello()"> Hello </button>
    .....
    </body>

**ng-controller** directive is primarily used to associate an instance of a controller with a UI element.

With ng-controller, we have provided a name to this particular instance of AppController. Using controllerAs syntax, we can give each instance of the controller a name in order to recognize its usage in the HTML. Note that we can even have different instance of the controller used in different place in UI.

### 6. A quick summary on scope ###
One of the best explanation available on AngularJS scope can be found at [This link](https://github.com/angular/angular.js/wiki/Understanding-Scopes), which will answer all your scope related questions. Below is a quick summary on scope.

+ Every Angular application has a single root scope that can be accessed using **$rootScope**. Application may have serveral other scopes[child scopes]. All other scopes are descendant scopes of the root scope.
+ A Scope in general is an object that refers to the application model. It acts as a context for an element in your HTML DOM. Each & every element in your HTML lives under a scope, whether it is it's own scope or a parent scope. If the element has not defined it's own scope, it is using scope from it's parent.
+ Scopes are arranged in hierarchical structure which mimic the DOM structure of the application.
+ You may also treat the scope as a bridge between model & view.
+ Scope are attached to the DOM as $scope data property.
+ Scopes provide APIs($watch) to observe model changes.
+ Scopes provide APIs($apply) to propagate any model changes through the system into the view from outside of the "Angular realm"
+ Scopes can propagate events in similar fashion to DOM events.The event can be broadcasted to the scope children or emitted to scope parents.

### 7. Controller demo ###
示例代码：
> [AngularJS controller basic demo][1]    
> [AngularJS Nested Controller Demo][3]    

[1]: https://github.com/gregecho/AngularjsLearning/tree/master/AngularjsDemo1/AngularJSControllerDemo.html
[3]: https://github.com/gregecho/AngularjsLearning/tree/master/AngularjsDemo1/NestedControllerDemo.html


-----
### TODO

* [ ] Read following artical ["Understanding Scopes"](https://github.com/angular/angular.js/wiki/Understanding-Scopes).

---
**Reference**
> [AngularJS Tutorial][2]

[2]:http://websystique.com/angularjs-tutorial/