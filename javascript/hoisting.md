## HOISTING 

* Variable and function devclarations are put into memory during the compile phase but stay where you type them in your app. 

* One advantage of Javascript putting function declarations into memory before executing any code segment is the ability to use a function before it has been initialized in your code 




i.e.: 
``` 

foo('Luke'); 

function foo(name){
  console.log(`Hello ${name} !`) 
}
``` 

Works the same as way as doing : 

``` 
function foo(){
  console.log(`Hello ${name} !`) 
}
foo() 
```

 * In ES6 this is not a recommended practice. The first function works and prints the string      'hello' and the name passed in. The variable foo is declared after it is used but still works. When your Javascript code is being processed, in the first iteration, before actually executing it line by line, all the variable and function declarations are detected. Then they are created in memory and space is allocated for them. Only after that, the code is executed line by line. 

 * This behaves exactly the same as if the declarations were moved to the top of the scope (the function body). This means that your code behaves as if the declaration of the variables and functions were first and then the rest of your code. 

 * it is always a good idea to always declare first before using a variable or a function and to group all of the declarations on the top of the scope they apply to. It is much easier to see what variables are being used for in a given scope and easier to find a variable declaration when looking for it. It is also much more natural to define the function / variable before using it and not doing it the other way round. Such code is much easier to read, understand & reason. 


## BLOCK SCOPE: 

```
for (var i = 0; i < 10; i++) { 
  // do something 
}
console.log(i) // results in 10 
``` 

 * variables declared using the 'var' keyword do not respsect block scope. That means you would expect the variable i from the above for loop to be only accesible inside the loop. Wrong... . 
 Because var does not respect block level scope it will be globally accesible in your app. That means the variable i is now declared also as a property of the window ( window.i ) . 

 *  variables declared using var can be accessed in the whole scope. You can access them before they are declared. This is considered bad practice, as only declarations and not initializations are hoised. 

 ## LET 
  * let behavies differently. You can only access it only after it was declared. Until then the variable is considered to be in the 'temporal dead zone'


  Example: 

  ```
  var foo = 32; 
  console.log(window.foo) // 32 
  ``` 

  * when using let or const this does not happen 

  ``` 
  let foo = 42; 
  console.log(window.foo) // undefined 
  console.log(foo) // 42 
  ```
