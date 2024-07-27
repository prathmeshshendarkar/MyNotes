## More About Functions
- Functions are called first class objects, which means they also have properties just like objects.
### Passing argument to function in javascript
1. Arguments in javascript is either passed as by value or by reference
2. We we pass primitive values such as strings, numbers, or booleans we are passing the arguments as value. So any modification of that value inside the function will not affect the original variable.
3. Whereas when we pass the non primitive values such as arrays, objects ... We are passing it as reference, which means any modification to the values inside the function will modify the original variable as well.

### Higher Order Functions
1. When we pass any function as an argument to a function and that function returns the function as well, these are called higher order functions.
```
		// We are defining our handler function
		function add(x, y){
		    return x + y;
		}
		
		// We are defining our main function
		function operatononnums(operatorfunc, x, y){
		    // We are returning the handler function return value
		    return operatorfunc(x, y);
		}
		
		console.log(operatononnums(add, 2, 3));
```

### CallBack function
1. [[Callbacks]]


### Constructor Function
1. When we create a constructor function, pass on the argument to the function we we initialize the function using new keyword.
2. Whatever arguments we pass during initialization, in order for the new object to use that argument, we need to define that inside of this keyword.

### Static Properties
1. Static properties are something that you can access without creating an instance of the class. On the other hand, the instance will not have access to the static properties of a class.

### Call, Apply, Bind and this keyword
1. [[this Keyword in javascript]]

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

### Closures
1. Closures are functions that can access the variables or functions in the scope it was defined, even though the scope is executed.

### Variable Shadowing
1. 