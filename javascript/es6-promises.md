## ES6 promises 


* Promises are part of the es6 standard and are an alternative to callbacks. They are an alternative way of handling asynchronous operations. 


* They are called promises because while they are handling asynchronous operations, they can promise to do something when that operation is finished. You handle a promise response with a .then. Some function .then and inside there you will specify what happens when the promise is complete. 

* Resolve is what you want to call when what you’re done with what you’re doing 

* Reject is what you want to call if there is some kind of error that you want to throw. 

Example: 
```
function createPost(post) { 
   return new Promise(function(resolve, reject){
     setTimeout(function () {
       posts.push(post);
       resolve();
      
   }, 2000);
   });
}

createPost({title: 'post three', body: 'this is post three'}).then(getPosts);

``` 


Handling errors with ES6 promises: 
```
 
function createPost(post) { 
   return new Promise(function(resolve, reject){
     setTimeout(function () {
       posts.push(post);
       const error = true;
       if(! error){
         resolve();
 
       }else {
         reject('Error: Something went wrong')
       }
      
   }, 2000);
   });
}

createPost({title: 'post three', body: 'this is post three'}).then(getPosts).catch(function(error){
 console.log(error)
})


``` 