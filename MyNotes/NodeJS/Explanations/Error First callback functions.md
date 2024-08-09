##  Who handles the asynchronous callback functions calls in nodeJs?
- Well, Event loop handles all async calls except for file i/o operations.
- This operations are handled by libuv library and is maintained in it's own thread pool.
- Libuv Library has it's own thread pool, once the file i/o operation is completed the callback is placed in the callback queue after that.

## Error first callback functions
- The error first callback functions are a way to handle the asynchronous calls.
- This is a standard approach provided by Ryan from the start.
- How to use error first callback function?
```
const urlName = 'https://swapi.dev/api/people/';

const dataFetched = (callbackFunc) => {
  const outputResult = fetch(urlName)
    .then((res) => res.json())
    .then((data) => callbackFunc(null, data))
    .catch((err) => callbackFunc(new Error('Error Fetching the data'), null));
  // console.log(outputResult); This will be a promise
  return outputResult;
}

const callbackFunc = (err, res) => {
  // console.log("Hello");
  if (err) {
    console.error(err.message);
    return;
  }
  console.log(res);
}

const outputData = dataFetched(callbackFunc);

------------------------------------------------------------------

const fs = require("fs");

// Declare the callback function first
const callbackFunc = (err, data) => {
  if (err) {
    console.error(err.message);
    return;
  }
  console.log(data);
  fs.writeFile("./sample2.txt", data, "utf8", callbackFunc);
};

// Call fs.readFile with the correct syntax
fs.readFile("./sample.txt", { encoding: "utf8" }, callbackFunc);

fs.writeFile("./sample3.txt", "Hey Man", "utf8", (err) => {
  if (err) {
    console.error(err.message);
    return;
  }
  console.log("File Entry added!!!");
});

```
