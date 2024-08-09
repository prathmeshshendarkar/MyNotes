1. Closures are functions that have access to variables in the scope in which it was defined even after that scope was executed.
```
let a = 10;
function printHello(){
  let b = 20;
  return function(){ // Closure function
    let c = 30;
    return function(){ // This funnction is closure
      console.log(a);
    }
  }
}

let outputFun = printHello();
outputFun();

let newFun = outputFun();
newFun();
```

2. Above closure functions can access the variables that were declared in that scope. If we tried accessing a particular variable outside of that scope, it won't happen.