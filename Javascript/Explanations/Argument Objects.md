### Argument Objects
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
