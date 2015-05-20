#Angular
## File naming and variable names.
### What
Name HTML file names, css class/id names using snakecase according to state name.
eg) for `.state(main.sub1)`, name files: `main-sub1.html`, name id attribute: `id="main-sub1"`
Name Controllers using dot notation in same format and according to state name.
eg) for `.state(main.sub2.sub3)`, name controller: `.controller('main.sub2.sub3', ...)`
Name JS variable names using lower camelcase.
eg) `var thisIsAnotherVariable = 1223132;`
Name Service/Factory/Directive names using proper camelcase.
eg) `.factory(MyAwesomeUtilityFunctions, ...)`
### Why
For consistent, more logical state driven development.


