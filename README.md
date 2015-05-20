#Angular
## Folder structure
### What
Make a folder for every abstract state.  
eg) for;
```js
  .state('init', {
    abstract: true,
    url: '/init',
    templateUrl: "states/init/init.html",
  })
  .state('init.login', {
    url: '/login',
    templateUrl: "states/init/init-login.html"
  })
    .state('init.anotherAbs', {
      abstract: true,
      url: '/anotherAbs',
      templateUrl: "states/init/anotherAbs/anotherAbs.html"
    })
```
Note we have folder named `init` which is the same name as state `init`.


## File and variable naming.
### What
Name folders with lower camelcase for abstract states.
eg)
for `.state('init',{abstract: true, ...})`

Name HTML file names, css class/id names using snakecase according to state name.
eg)
for `.state('main.sub1', ...)`, name files: `main-sub1.html`, name id attribute: `id="main-sub1"`  
Note if `.state('mainCamel.sub1', ...)` then `mainCamel-sub1.html`, `id="mainCamel-sub1"`  
snakes for dots

Name Controllers using dot notation in same format and according to state name.  
eg)
for `.state('main.sub2.sub3', ...)`, name controller: `.controller('main.sub2.sub3', ...)`  

Name JS variable names using lower camelcase.  
eg)
`var thisIsAnotherVariable = 1223132;`  

Name Service/Factory/Directive names using proper camelcase.  
eg)
`.factory('MyAwesomeUtilityFunctions', ...)`  

Make state Data service with properties that reflect to a state it is used in.
eg) 
```js
.factory(Data, function (){
  var Data = {
    rootVariable1: 'Note this is root state like index.html',
    rootVariable2: 'used like $scope.data = Data',
    main: {
      mainRootVariable1: 'This is main abstract state data',
      mainRootVariable2: 'used like `$scope.dataMain = Data.main`',
      nested1: {
        mainNestedStateVar1: 'this is data for nested state of main',
        mainNestedStateVar1: '$scope.dataMainNested1 = Data.main.nested1'
      }
    }
  }
});
```
### Why
For more consistent, more logical, MOREEEEE state driven development.


