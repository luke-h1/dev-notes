## VAR VS LET 

* the differnces between var and let have to do with scope 

* introduced in ES6, ```let``` allows you to declare a variable that is accesible only inside a specific block of code 


Example: 

```
function foo(){
  var a = 2; 

  if (a > 1){
    let b = 4;  

      while (b < 4){
        let c = a + b; 
        b++; 
      }
  }
}
```

In the above example, b can only be accessed in the if statemnt and not in the whole foo function. C can only be accessed inside the while loop