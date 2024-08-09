### Immediately Invoked Function Expression (IIFE)();
1. These are functions that are immediately invoked as soon as they are initialized.
2. These functions are useful when we want to declare a variable scope and avoid hoisting.
```
(function(){
  var b = 20;
  console.log("I am inside function");
})();
console.log("I am outside function");
```