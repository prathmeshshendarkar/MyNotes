### Functions

1. There are different ways to define a function

```
	1. function add(a,b){
		   return a+b;
	   }
	2. let xd = function(a,b){
		   return a+b
	   }
```

2. Now first way is the normal way to create a function.
3. Second one is call function express, where we assign the function to a variable and then call that function
4. The important difference here is that, first function is hoisted, we can call the function before declaration, **_However the function expression is not hoisted._**
5. Now If we try to call `xd()` Before we declare a function express, this will throw reference error.