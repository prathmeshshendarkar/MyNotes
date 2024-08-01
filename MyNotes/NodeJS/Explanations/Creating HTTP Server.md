## Creating a server will only NodeJS
```
// 1. First I would require HTTP Module for initalizing a listener
// This listener will listen to any incoming requests
// And based on that will fire the response
const http = require('http');

// Before we start creating a function, we need to define
// a server, because just the http module won't be suffice
// A web server will act for fetching requests and will require a callback function that needs to be called for the server
const myServer = http.createServer(requestListener);

// Now, we need to listen to incoming requests
// However, first we need define a port that will be used
myServer.listen((3000), () => {
    console.log("Server is running");
});

function requestListener(req, res){
    if(req.url === '/'){
        res.end("Hello World");
    }

    if(req.url === '/name'){
        res.end("Hello John");
    }
}
```

Creating Web server using express
1. Now, we can create web server using http module of nodejs then why express? Well express is a framework built on top of http module. Express provides easy use of request handling and use of middleware functions. 
```
	// Use of express
	// import express from 'express';
	const express = require('express');
	
	const app = express();
	
	app.get('/', (req, res) => {
	    res.status(200).send("Hello World");
	})
	
	app.listen('3000', () => {
	    console.log("Yes express is running");
	})
```

