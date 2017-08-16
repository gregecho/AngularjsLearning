

## Content ##
### 1. Basic Form ###

> [ Basic Form demo][1]

[1]: https://github.com/gregecho/AngularjsLearning/tree/master/AngularjsDemo1/Basic_Form.html

+ With **ng-model**, AngularJS automatically creates the objects and it's properties on the fly if it does not exist.

### 2. Form with Error Handling ###
+ We can use name attribute on that field and on form. When we add a name to any input field, it creates a model on the form for that particular input, with the error state.
+ Each of the validators exposes a key on the $error object, so that we can pick it up and display the error message for that particular error to the user.
+ If a certain validator failed, then AngualrJS marks that field as invalid [myForm.email.$invalid], which can again be used with ng-show to display further error to user.

#### 2.1 Different Form states in AngularJS ####
>+ **$invalid** : AngularJS sets this state when any of the validations (required, ng-minlength, and others) mark any of the fields within the form as invalid.
>+ **$valid** : The inverse of the previous state, which states that all the validations in the form are currently evaluating to correct.
>+ **$pristine** : All forms in AngularJS start with this state. This allows you to figure out if a user has started typing in and modifying any of the form elements. Possible usage: disabling the reset button if a form is pristine.
>+ **$dirty** : The inverse of $pristine, which states that the user made some changes (he can revert it, but the $dirty bit is set).
>+ **$error** : This field on the form houses all the individual fields and the errors on each form element.


> [ Form with Error Handling][2]

[2]: https://github.com/gregecho/AngularjsLearning/tree/master/AngularjsDemo1/Form_with_Error_Handling.html

### 3. Form with Bootstrap ###



> [ Form_with_Bootstrap][3]

[3]: https://github.com/gregecho/AngularjsLearning/tree/master/AngularjsDemo1/Form_with_Bootstrap.html

-----
### TODO

* [ ] Read following artical ["Understanding Scopes"](https://github.com/angular/angular.js/wiki/Understanding-Scopes).