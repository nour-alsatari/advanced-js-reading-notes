# advanced-js-reading-notes
Event loop:

The event loop has to wait until the stack is clear before it pushes the call back into the stack. it compares both
looks at the stack and looks at the task queue, if the stack is empty it takes the first thing in the queue and push it to the stack 

callback can be anyfunction that a function calls or they can be more explicitly be asynchronous callbacks as in one that will get pushed back to the call back queue in the future


Callback functions:

function is being called after something happened. we callback the callback func right after something has happened or some task is completed
we also use callback functions for event declarations

promises:
Promises are the ideal choice for handling asynchronous operations

A promise can be created using Promise constructor.
Syntax
var promise = new Promise(function(resolve, reject){
     //do something
});

Promise Consumers
Promises can be consumed by registering functions using .then and .catch methods.

Async/Await is the extension of promises
Async functions will always return a value. It makes sure that a promise is returned

Await function is used to wait for the promise. It could be used within the async block only. It makes the code wait until the promise returns a result. It only makes the async block wait.

Test-Driven Development:
There are two main types of automated tests: Unit and End-to-End (E2E)

Test-driven development is the act of first deciding what you want your program to do (the specifications), then writing the code to make that test pass
Jest is looking for a file name with some specific characteristics such as a .spec or .test contained within the file name.
Tests are just functions that receive a couple of arguments. We can call our test with either it() or test().
There is another way we could organize our code. We could wrap each test in a describe function.