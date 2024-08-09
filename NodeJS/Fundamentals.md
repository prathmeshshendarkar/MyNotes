1. NodeJS is a Javascript Runtime environment. So basically any javascript code can be executed using NodeJS.
2. Just like we compile c++ code because we have g++ or gnu , similary to execute a javascript code, we require NodeJS or atleast some sort of javascript engine.
3. NodeJS also has V8 Javascript Engine that they have build inorder to execute javascript, this engine is used by chrome team for execution of our javascript codes.
4. Similary, Firefox uses Spider Monkey Engine. We can use these independent engines and still execute our javascript code outside of browser. How?
5. Well think about how desktop based applications and server side scripting works. They all uses a javascript engine.

## To Understand Event Loops and how nodeJS can handle multiple requests 
- [Event Loop](https://dev.to/trunghieu99tt/how-does-nodejs-handle-thousands-of-requests-while-its-single-thread-dcp)
- [Another Article](https://polcode.com/resources/blog/how-to-handle-thousands-of-requests-efficiently-node-js-secrets-uncovered/)
- [StackOverFlow Article](https://stackoverflow.com/questions/34855352/how-in-general-does-node-js-handle-10-000-concurrent-requests)
### With the above point, how can we handle multiple requests using workers?
- [Workers](https://www.geeksforgeeks.org/how-to-run-many-parallel-http-requests-using-node-js/)



