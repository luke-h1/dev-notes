## Class + prototypal inheritance 

  * In javascript, All functions by default get a public property on them called prototype. 

  ```
  function Foo() {
    // .... 
  }

  Foo.prototype;  
  ``` 


 * constructors 
```
  function Foo(){
    console.log('hello'); 
  }
  let a = new Foo(); // hello; 

``` 
 * Foo is just a normal function, but when called with new, it constructs an object which is then assigned to the variable a. The call was a constructor call, but Foo is not a constructor. Functions aren't constructors but function calls are "constructor calls" if the new keyword is used 
