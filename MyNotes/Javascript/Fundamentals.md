
## ECMAScript , Javascript , NodeJS, Bun

```
ECMAScript

    Specification for Writing JavaScript: ECMAScript is a standard specification that serves as the foundation for writing JavaScript.

JavaScript

    Language Based on ECMAScript: JavaScript is a programming language built on top of ECMAScript specifications.
    JavaScript Compilation: To compile JavaScript, Chrome developed the V8 Engine, which is designed to compile and execute JavaScript.
    Browser Execution: Initially, the only way to run JavaScript was through a browser.
    Web APIs: Functions like setTimeout and fetch are provided by the browser and are called Web APIs. They are not part of the ECMAScript specifications.

Node.js

    JavaScript Outside the Browser: Node.js was developed to allow JavaScript to run outside the browser, making it possible to use JavaScript as a backend language.
    Built on V8 Engine: Node.js includes features such as HTTP, file I/O, and others, built on top of the V8 engine, enabling JavaScript to run on the server side.

Bun

    Node.js Competitor: Bun is another runtime that can execute JavaScript.
    Built with Zig: Unlike Node.js, which is built on top of C or C++, Bun is built using the Zig programming language.


```

### Var , Let and Const variables

* Check this article: \[\[Why should we use const instead of let and var]] Available in Explanations Tab!

### Typeof

```
		console.log(typeof 1); // 'number'
		console.log(typeof 'hello'); // 'string'
		console.log(typeof true); // 'boolean'
		console.log(typeof {}); // 'object'
		console.log(typeof []); // 'object'
		console.log(typeof function() {}); // 'function'
		console.log(typeof null); // 'object'
		console.log(typeof undefined); // 'undefined'
```

* Important ones: typeof `{} - Object, [] - Object , null - Object , undefined - undefined`
* When checking the typeof values of variables that are not initalised will give undefined.

```
	let x;
	console.log(typeof(x)); // Undefined
```

### Type Conversions

1. When we are adding any 2 types of distinct data in javascript, if one of the data is string then other data whatever maybe will convert to string
   1. Ex: 10 + "20" - 1020 ; true + "20" - true20
2. Whereas when we are doing any other mathematical operations on distinct data, then string is converted to number and then operations are performed.
   1. Ex: 10 - "20" -> -10 ; true - "20" -> -19
   2. Ex: 10 \* "20\* -> 200
   3. Ex: 20 / "10" -> 2
   4. Ex: 20 % "10" -> 0
3. Boolean values are converted everytime, with strings and with numbers. True : 1 and False : 0
   1. True + "10" - 11
   2. False - 10 -> -10
4. Also there are two types of conversions: Implicit Type/Automatic Type, Explicit Type

### Equal(`==`) and Strict Equal Operators (\`===)

1. Equal operator will check both the operators and will provide a boolean result and also will convert one data type to another.
   1. For ex: 10 == "10" => returns true
2. Strict equal operator will provide a boolean result with strict actions, and will not convert any data types
   1. For ex: 10 === "10" => returns false

### Truthy and Falsy values

1. Below values are false values

```
		 false
		 0 or -0 or 0n
		 ""
		 null
		 undefined
		 NaN
```

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
4. The important difference here is that, first function is hoisted, we can call the function before declaration, _However the function expression is not hoisted._
5. Now If we try to call `xd()` Before we declare a function express, this will throw reference error.
6. **Arrow Functions**

```
	const add = (a, b) => {
		return a + b;
	}
	const add = (a,b) => a+b
	The second arrow function does not have any return statement
	It is by implicit so we don't need to specify return.
```

7. Anonymous Function

```
		The anonymous function is declared without any name
		they can be declared using both function and arrow functions
		1. setTimeOut(function(){
		}, 1000)
		2. setTimeOut(() => {
		}, 1000)
```

8. Functions can be passed as argument to another function and they can be returned as anonymous function from a function.
9. **Arguments Object**
   1. In javascript functions, (Not Arrow functions) the arguments which are passed to the functions can be accessed via arguments object. Ex:
   2. Note: They are not arrays … So you cannot perform push, pull and other array operations on them.

```
		function a(x, y, z){
		    console.log(arguments);
		}
		a(1,2,3); //[Arguments] { '0': 1, '1': 2, '2': 3 } 
		The above is not available for arrow functions.
		In ES6 , we can use rest operator easily to access the arguments
```
