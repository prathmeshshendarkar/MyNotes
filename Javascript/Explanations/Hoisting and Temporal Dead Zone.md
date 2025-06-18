
### Hoisting
1. Hoisting is a concept where the declared functions, variables or class are hoisted or raised to the top of the scope they were defined in.
```
	printHello();
	
	function printHello(){
	  console.log("Hello");
	}
```
2. The below code will throw error, because the printJello function is initiated within global scope. This function is also hoisted, but it is hoisted in printHello's scope(Local scope)
```
	printHello();
	printJello(); // Not defined
	function printHello(){
	  console.log("Hello");
	  function printJello(){
	    console.log("Jello");
	  }
	}
```
3. Let's try to modify the code and then we will show the output
```
	printHello();
	
	function printHello(){
	  console.log("Hello");
	  printJello(); // Jello
	  function printJello(){
	    console.log("Jello");
	  }
	}
```

### Hoisting in var, let and const
1. With var declarations, same happens. They are also hoisted to the top of there scope.
```
	print();
	
	console.log(name); // name is not defined
	function print(){
	  var name = "Hello";
	}
```
2. Why name is not defined? Well, it's because hoisting happens to the top of there scope they were defined in. In this case, the name is hoisted to the top of print function's scope. Below is the modified code.
```
	print();
	
	function print(){
	  console.log(name); // Hello
	
	  var name = "Hello";
	}
```


# Temporal Dead Zone
1. A temporal dead zone is a area of block where a variable is in accessible until computer fully initializes it with a value.
2. 