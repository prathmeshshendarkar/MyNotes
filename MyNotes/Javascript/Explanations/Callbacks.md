## CallBack Functions
1. Javascript has asynchronous tasks that are resolved after certain period of time.
2. Lets say after a certain period, those tasks gets resolved, and we need a notification. Like for ex, I have tweeted something which takes time, and after that I need a notification.
3. How will I know if the task is completed or not?? That's where callback functions come.
4. Callback functions are called inside any function, mostly in asynchronous functions. That is when a asynchronous task is completed, that callback function will be called notifying everyone that the task is completed.
```
let a = 10;
console.log(a);
setTimeout(() => {
  a = 20;
  console.log(a);
}, 4000);
```

### CallBack Hell
1. Now, lets say, we have a schedule ok. Once an asynchronous task is completed, proceed to another asynchronous task, once that is completed proceed to another asynchronous task. For ex below
```
let a = 10;
console.log("Before Timer");
setTimeout(() => {
  console.log(a);
  setTimeout(() => {
    a = 20;
    console.log(a);
    setTimeout(() => {
      a = 30;
      console.log(a);
    }, 1000)
    console.log(`I am inside second setTimeout ${a}`);
  }, 1000)
  console.log(`I am inside first setTimeout ${a}`);
}, 1000);
console.log("After Timer");

//Output
Before Timer
After Timer
10
I am inside first setTimeout 10
20
I am inside second setTimeout 20
30
```
2. The above code is what callback hell looks like. We cannot have this much callback functions inside another functions, that is not readable.