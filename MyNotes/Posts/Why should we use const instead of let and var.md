# Function scope and Block scope
1. Function scope: When a variable is declared inside a function using `var`, it is only accessible within that function.
2. Block scope: Variables declared within a block (i.e., inside `{}`) using `let` or `const` are only accessible within that block.

# Difference between var , let and const
1. var:
	1. Variables declared with `var` within a function are only accessible within that function.
    2. Variables declared with `var` are accessible before initialization, but their value is `undefined`. These variables are hoisted to the top of the function scope.
    3. These variables can be re-declared and updated after initialization.
```
		var x = 10;
		x = 20;
		console.log(x); // 20
		
		function myApp(){
		    console.log(a); // undefined
		    var a = "I am inside function";
		    console.log(a);
		}
		myApp();
```
2. let:
	1. Variables declared with `let` within a block of code (such as `if/else` statements, loops, or any `{}`) are only accessible within that block.
    2. If you try to access a `let` variable before initialization, JavaScript will throw a `ReferenceError`.
    3. These variables can be re-declared in the same scope, they can be updated as well within the same scope.
```
	    let x = 10;
		x = 20;
		console.log(x); // 20
		
		function myApp(){
		    console.log(a); // Reference Error
		    let a = "I am inside function";
		    console.log(a);
		}
		myApp();
		console.log(x);
```
3. const:
	1. Variables declared with `const` cannot be re-declared and cannot be updated after initialization.
    2. However, you can update the properties and elements of `const` variables, such as objects and arrays.
    3. `const` variables will also throw an error if accessed before initialization.
    4. `const` variables are also block-scoped.
```
	    const x = 10;
		x = 20;
		console.log(x); // TypeError
		
		function myApp(){
		    console.log(a); // Reference Error
		    const a = "I am inside function";
		    console.log(a);
		}
		myApp();
```

In Summary:
- `var` variables are function-scoped, meaning they are accessible throughout the function even if declared inside a block.
- `let` and `const` variables are block-scoped, meaning they are only accessible within the block where they are declared.
- Always try to use `const` variables first if you do not intend to change their values.
- If you need to reassign values, use `let` variables instead of `var`.