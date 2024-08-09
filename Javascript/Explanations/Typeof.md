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