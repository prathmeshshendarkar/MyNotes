## Event Emitter class
- Event emitter is a class of events module. Whenever a object or component will emit any events for example clicking a button or a data is fetched successfully then a listener will detect that event and will call the callback function.
- It is useful in asynchronous programming, decoupled modules i.e, a module which is independent of a different module, any particular task that we perform in a module the other module's behavior won't change.
- Is event emitter asynchronous tasks? No . It is a synchronous task, check below example, where, until and unless all the listeners jobs are completed, the further code is not executed. So it is a blocking code?
```
// import events from 'events';
const events = require('events');
// const eventEmitter = events.EventEmitter;

// console.log(eventEmitter);

const myEmitter = new events();

// Listen to a particular event
myEmitter.on('eventOne', () => {
    console.log("I am inside Event One");
    setTimeout(() => {
        console.log("Hello Event One");
    }, 1000)
    console.log("I am inside Event One after callback");
})

// Emit event one event
console.log("Hello World")
myEmitter.emit('eventOne');
console.log("End world");

Output
Hello World
I am inside Event One
I am inside Event One after callback        
End world
Hello Event One
```

- So basically, event Emitter is a synchronous tasks, so every listener will be called, however, the asynchronous tasks which are inside of listener will be called later.
- Another example of different listeners listening to a event, however still performing synchronous tasks.
```
// import events from 'events';
const events = require('events');
// const eventEmitter = events.EventEmitter;

// console.log(eventEmitter);

const myEmitter = new events();

// Listen to a particular event
myEmitter.on('eventOne', () => {
    console.log("I am inside Event One");
    setTimeout(() => {
        console.log("Hello Event One");
    }, 1000)
    console.log("I am inside Event One after callback");
})

myEmitter.on('eventOne', () => {
    console.log("Second listener");
    setTimeout(() => {
        console.log("Second Event One");
    }, 2000)
})

myEmitter.on('eventOne', (arg1) => {
    console.log(`Third listener ${arg1}`);
    setTimeout(() => {
        console.log("Third Event One");
    }, 1000)
})

// Emit event one event
console.log("Hello World")
myEmitter.emit('eventOne', "John");
console.log("End world");

Output
Hello World
I am inside Event One
I am inside Event One after callback        
Second listener
Third listener John
End world
Hello Event One
Third Event One
Second Event One
```

## Listening for a event only once!
- The listener will only listen to a particular event once after that even if the event is called multiple times it won't work.
```
// listening to a event once

myEmitter.once('eventTwo', () => {
    console.log("I am calling the event once");
    setTimeout(() => {
        console.log("Event once called");
    }, 1000)
})

myEmitter.emit('eventTwo');
myEmitter.emit('eventTwo');

Output
I am calling the event once
Event once called
```

## Calling prepend listener method for providing a precedence over a specific listener.
1. We can call the prepend listener method, if we want a specific listener to be called before all the listeners. Below is the example
```
// import events from 'events';
const events = require('events');
// const eventEmitter = events.EventEmitter;

// console.log(eventEmitter);

const myEmitter = new events();

// Listen to a particular event
myEmitter.on('eventOne', () => {
    console.log("I am inside Event One");
    setTimeout(() => {
        console.log("Hello Event One");
    }, 1000)
    console.log("I am inside Event One after callback");
})

myEmitter.on('eventOne', () => {
    console.log("Second listener");
    setTimeout(() => {
        console.log("Second Event One");
    }, 2000)
})

myEmitter.on('eventOne', (arg1) => {
    console.log(`Third listener ${arg1}`);
    setTimeout(() => {
        console.log("Third Event One");
    }, 1000)
})

myEmitter.off('eventOne', () => {
    console.log("Offline listener");
})

myEmitter.on('eventOne', () => {
    console.log(`Fourth listener`);
    setTimeout(() => {
        console.log("Fourth Event One");
    }, 1000)
})

myEmitter.prependListener('eventOne', () => {
    console.log(`Prepended Listener`);
    setTimeout(() => {
        console.log("Hello Prepend Listener");
    }, 1000)
})

myEmitter.prependListener('eventTwo', () => {
    console.log(`Prepended Listener Second Event`);
    setTimeout(() => {
        console.log("Hello Prepend Listener two");
    }, 1000)
})

// Emit event one event
console.log("Hello World")
myEmitter.emit('eventOne', "John");

myEmitter.emit('eventTwo');
console.log("End world");
console.log(myEmitter.listenerCount('eventOne'))

Output
Hello World
Prepended Listener
I am inside Event One
I am inside Event One after callback        
Second listener
Third listener John
Fourth listener
Prepended Listener Second Event
End world
5
Hello Prepend Listener
Hello Event One
Third Event One
Fourth Event One
Hello Prepend Listener two
Second Event One
```

## Other methods on eventEmitter
1. To remove a specific listener: removeListener
2. To remove all listeners for a specific event: removeAllListener
3. To set specific number of listeners for a particular event: setMaxListeners

 