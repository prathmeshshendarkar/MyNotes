Before Learning promises checkout this link about callbacks: [[Callbacks]]

## What is a Promise?
1. Well a promise is a standarized way of handling asynchronous operations instead of entering into a callback hell.
2. To use promise, we instantiate a new promise object with the new keyword and Promise constructor function. This function will accept a callback function as the only single argument. This callback function is also called executor.
```
const urlName = 'https://swapi.dev/api/people/';

console.log("Hello World");

// Lets start with Normal promise to fetch the data
// Fetch also has in built promise method, so we actually don't need to create our own promise.
const Promise1 = new Promise((res, rej) => {
  console.log("Hello Promise")
  fetch(urlName)
    .then((resp) => resp.json())
    .then((data) => res(data))
    .catch(err => rej(err));
})

Promise1
  .then((data) => console.log(data))
  .catch(err => console.log(err));
// Promise is either fulfilled or rejected 
```

## Promise.all
1. We can use Promise.all method in order to check if all the promises are fulfilled or not.
2. Even if there is one rejected promise from the array, it will still throw error. The function will overlook the resolved promises. Check below code
```
// Lets use multiple promises
let p1 = new Promise((res, rej) => {
  console.log("I am inside P1");
  setTimeout(() => {
    // console.log("I am inside first P1 Timer");
    res("I am inside first P1 Resolution");
  }, 1000);
})

let p2 = new Promise((res, rej) => {
  console.log("I am inside P2");
  setTimeout(() => {
    // console.log("I am inside second P2 Timer");
    rej("Error I am inside second P2 Resolution");
  }, 1000)
})

let p3 = new Promise((res, rej) => {
  console.log("I am inside P3");
  setTimeout(() => {
    // console.log("I am inside second P2 Timer");
    res("I am inside second P3 Resolution");
  }, 1000)
})

// Lets use Promise.all to fulfill all the promises
Promise.all([p1, p2, p3])
  .then((results) => {
    console.log(results);
  })
  .catch((err) => {
    console.log(err);
  })

// Output
I am inside P1
I am inside P2
I am inside P3
Error I am inside second P2 Resolution
```
3. Whereas, if all the promises will give me correct result then I will get the output correct
```
// Lets use multiple promises
let p1 = new Promise((res, rej) => {
  console.log("I am inside P1");
  setTimeout(() => {
    // console.log("I am inside first P1 Timer");
    res("I am inside first P1 Resolution");
  }, 1000);
})

let p2 = new Promise((res, rej) => {
  console.log("I am inside P2");
  setTimeout(() => {
    // console.log("I am inside second P2 Timer");
    res("I am inside second P2 Resolution");
  }, 1000)
})

let p3 = new Promise((res, rej) => {
  console.log("I am inside P3");
  setTimeout(() => {
    // console.log("I am inside second P2 Timer");
    res("I am inside second P3 Resolution");
  }, 1000)
})

// Lets use Promise.all to fulfill all the promises
Promise.all([p1, p2, p3])
  .then((results) => {
    console.log(results);
  })
  .catch((err) => {
    console.log(err);
  })

// Output
// I am inside P1
// I am inside P2
// I am inside P3
// (3) ['I am inside first P1 Resolution', 'I am inside second P2 Resolution', 'I am inside second P3 Resolution']
```

## Different API's that we can use that has in-built promise functions.
1. Fetch
```
// Lets work with fetch which is inbuilt promise
const urlName = 'https://swapi.dev/api/people/';

console.log("Hello World");

fetch(urlName)
  .then((resp) => resp.json())
  .then((data) => console.log(data))
  .catch(err => console.log(err));

// Output
// Hello World
// {count: 82, next: 'https://swapi.dev/api/people/?page=2', previous: null, results: Array(10)}
```

2. Async /Await functions
	1. When we use async in front of any function, it automatically returns a promise even if we don't specify it.
	2. Below is the code which returns a promise and is handled by async and await functions.
```
	// Async Await Functions
	const fetchData = async () => {
	  await fetch(urlName)
	    .then((resp) => resp.json())
	    .then((data) => console.log(data))
	    .catch((err) => console.log(err));
	
	  return null;
	}
	
	fetchData();
	//Output
	// Hello World
	// {count: 82, next: 'https://swapi.dev/api/people/?page=2', previous: null, results: Array(10)}

	// A good way to execute async and await function
	const fetchData = async () => {
	  const resp = await fetch(urlName);
	  if (!resp) {
	    console.log("Error Occured while fetching the data");
	  }
	  const data = await resp.json();
	  return data;
	}
	
	const newData = async () => {
	  const data = await fetchData();
	  console.log(data);
	}
	
	newData();
	//Output
	// Hello World
	// {count: 82, next: 'https://swapi.dev/api/people/?page=2', previous: null, results: Array(10)}
```
