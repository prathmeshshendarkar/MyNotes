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