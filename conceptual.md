### Conceptual Exercise

Answer the following questions below:

- What are some ways of managing asynchronous code in JavaScript?

The best way is to use async await callback functions

- What is a Promise?

A Promise is an object that may produce a single value sometime in the futre: it will either be resolved value or a reason its not resolved.
A Promise may be in of 3 possible states: fullfilled, rejected, pending.

- What are the differences between an async function and a regular function?

Async funtions return a promise. You can use await to get the value. Async and Await is used with Promises to make the code look synchronous. A regular function executes i the order it was called.

- What is the difference between Node.js and Express.js?

Node.js is a run-time environment for building server-side event driven i/o application using Javascript

Express.js is a framework based on node.js for building web-applications using principles and approaches of node.js

- What is the error-first callback pattern?

Error-first Callback in Node.js is a function which either returns an error object or any successful data returned by the function.

1. The first argument of the callback is reserved for an error object. 
If an error ocurred, it will be returned by the first err argument.

2. The second argument of the callback is reserved for any successful response data. If no error occured, err will be set to null and any successful data will be returned in the second argument.


- What is middleware?

Middleware is code that runs inbetween of a request and response cycle

- What does the `next` function do?

next is the callback argument to the middleware function, called 'next' by convention. It is used to control the next middleware function--othersiwe the request will be left open.

- What are some issues with the following code? (consider all aspects: performance, structure, naming, etc)

The code is written in sequential order, and will have to execute three differnt responses. You can use async/await allows the calls to be made simultaneously and processed once received. 


```js
async function getUsers () {
  const elie = await $.getJSON('https://api.github.com/users/elie')
  const joel = await $.getJSON('https://api.github.com/users/joelburton')
  const matt = await $.getJSON('https://api.github.com/users/mmmaaatttttt')

  return [elie, matt, joel]
}
```
