
### Implicit Bindings of this keyword

1. this keyword in javascript refers to the context to which function is bind to. 
2. For ex, if this keyword is called inside a standalone function, then it is bind to the global context. However, if it is called from an object context, it will bind to that object.
3. Examples
	1. ![[Pasted image 20240715145139.png]]
	2. Same, if we use a variable that is defined outside of object maybe in global context, still it won't work.
	3. ![[Pasted image 20240715145337.png]]
	4. Lets look at same concept of binding this to a object, but with nested objects for better understanding.
	5. ![[Pasted image 20240715145743.png]]
	6. The above output is: Alice Bob

### Explicit binding of this keyword
#### Using call method in javascript
1. When we want to bind this value to a function we use call method. The second and third arguments of call function are the parameters that we pass to the function. Below is the implementation for that.
```
		// call method
		// function sayHello(){
		//   console.log(this.name);
		// }
		
		// const obj = {
		//   name: 'Alice'
		// }
		
		// const obj2 = {
		//   name: 'Bob'
		// }
		
		// sayHello.call(obj); // The first argument is this value. 
		// sayHello.call(obj2);
		// console.log(obj.sayHello); // undefined

```
#### Using constructor to bind function to a object.
1. We can use new keyword and constructor functions to bind the functions to object as well.
```
		// this using constructor
		function sayHello(name){
		  this.name = name;
		  console.log(`I am inside function ${name}`)
		}
		
		const obj = new sayHello('Alice');
		console.log(obj.name);
```

## Understanding Bind, Apply and Call
1. This was really hard for me to understand, I know it should be very basic. But seriously it was hell.
2. Ok, First of all Standalone functions have this undefined or global contexts.
3. Second, If a function is called from object, then that functions this is Object.
	1. However, if we call that function as a callback function in any asynchronous task, then this will be again undefined or global context. Because we are passing it as a standalone funciton. Below example
```
	let person = {
	    name: 'John Doe',
	    getName: function() {
	        console.log(this.name);
	    }
	};
	
	person.getName();
	setTimeout(person.getName, 1000); // Undefined because now this is referred to global context
```
4. Ok third, If we really want to access name from a certain object/component, then we need to use either bind/call/apply function.
5. Reason? Because the standalone function does not have access to parent's properties.
6. If we want to access those properties, we need to bind parent object to the standalone function.
```
let xd = 1;
let person = {
    name: 'John Doe',
    getName: function() {
        console.log(this.name);
    }
};

person.getName();
setTimeout(person.getName.bind(person), 1000);
```
7. In above example, we are binding a standalone function to person object. Now this refers to person object. Which is why the callback function will be executed correctly with this.name.

Refer below diagram for reactjs use case, when we are increasing the count value from a child component to a parent's count value.
![[IMG_20240724_133909.jpg]]