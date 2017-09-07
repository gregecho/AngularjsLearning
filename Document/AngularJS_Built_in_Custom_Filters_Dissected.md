## Context ##
> #### What is Filters ####
> #### Commonly used built-in filters ####
> #### Way to use filters ####
> #### Way to create AngularJS Service ####


## Content ##
### 1. What is Filters ###
AngularJS **Filters** are mainly used to transform the data from the data to a human-readable format. Filters **DO NOT MODIFY ** the data they applied upon, but provides on the fly conversion of that data into required format.


### 2. Commonly used built-in filters ###
Following are the commonly used built-in filters.

|            Filter             |                Description                 |
| ----------------------------- | ------------------------------------------ |
| lowercase | lowercase filter            |
| uppercase | uppercase filter   |
| currency | currency filter |
| number | number filter |
| date | date filter |
| json | json filter |
| limitTo | limitTo filter |
| orderBy | ordeBy filter |
| filter | filter filter |

### 3.Way to use filters ###
Filters can be applied on View Templates and on data in Controllers/Services/Directives.

####3.1 Filters On View Templates ####
On view level, filters are applied on expressions separated with PIPE.
````javascript
{{ expression | filter }}
````
Filter can be chained:
````javascript
{{ expression | filter1 | filter2 | ... }}
````
Filter can accept arguments:
````javascript
{{ expression | filter:argument1:arguments:... }}
````

[AngularJS built-in filters](https://github.com/gregecho/AngularjsLearning/tree/master/AngularjsDemo1/AngularJS_Built_In_Filters.html)
