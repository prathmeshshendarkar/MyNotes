### Variable Shadowing
1. When a inner scope or block scoped variable has the same name as global scope variable. Then if we try to print the value of the variable inside the inner scope, we will get the value of inner scope variable.
2. This is call variable shadowing, where in this case, the inner scope variable is shadowing the outer scope variable.
3. We can shadow the var variable by a let variable but the vice versa will throw error.
```
var a = 100;

(function greetings(){
  let a = 200;
  console.log(a); // 200
})();

console.log(a); // 100
```

