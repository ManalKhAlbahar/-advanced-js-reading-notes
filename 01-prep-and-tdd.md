# Read01 - TDD
1.Event Loop.
2.JS callback functions.
*3-JS Promises.
4-JS Async/Await.
5-Test-Driven Development.
###*Event Loop*
An event loop is something that pulls stuff out of the queue and places it onto the function execution stack 
whenever the function stack becomes empty.

For more details see [Event Loop](https://www.youtube.com/watch?v=8aGhZQkoFbQ).

### *JS callback functions*
Asynchronous programming:JS runs code sequentially in top-down order. However, 
there are some cases that code runs (or must run) after something else happens and also not sequentially.
The way to create a callback function is to pass it as a parameter to another function, and then to call it 
back right after something has happened or some task is completed. 
We can use a built-in method in JS called “setTimeout”, which calls a function or evaluates an expression 
after a given period of time (in ms). 
We can define a function directly inside another function, instead of calling it,also we can write the same callback
function as an arrow function,and we can use it with  event declarations.
 
 For more details see [JS callback functions](https://www.freecodecamp.org/news/JS-callback-functions-what-are-callbacks-in-js-and-how-to-use-them/).

### *JS Promises*
Promises are used to handle asynchronous operations in JS.

-Benefits of Promises 
 1-Improves Code Readability.
 2-Better handling of asynchronous operations.
 3-Better flow of control definition in asynchronous logic.
 4-Better Error Handling.

-A Promise has four states: 
 1-fulfilled: Action related to the promise succeeded
 2-rejected: Action related to the promise failed
 3-pending: Promise is still pending i.e. not fulfilled or rejected yet
 4-settled: Promise has fulfilled or rejected

Promises can be consumed by registering functions using .then and .catch methods.

For more details see [JS Promises](https://www.geeksforgeeks.org/javascript-promises/).

### *JS Async/Await*
Async:
It simply allows us to write promises based code as if it was synchronous and it checks that we are not breaking 
the execution thread.
Await:
Await function is used to wait for the promise. It could be used within the async block only. It makes the code
wait until the promise returns a result. It only makes the async block wait.
Promises can be consumed by registering functions using .then and .catch methods.

For more details see [JS Async/Await](https://www.geeksforgeeks.org/async-await-function-in-javascript/).

### *Test-Driven Development*
Testing is the process of ensuring a program receives the correct input and generates the correct output and intended 
side-effects.
1-Testing is verifying our application does what it should.
2-There are two types of tests: manual and automated
3-Tests assert that your program will behave a certain way. Then the test itself proves or disproves that assertion.
Test-Driven Development(TDD) is the act of first deciding what you want your program to do (the specifications),
formulating a failing test, then writing the code to make that test pass. It is most often associated with automated 
testing. Although you could apply the principals to manual testing as well.

For more details see [TDD](https://www.freecodecamp.org/news/an-introduction-to-test-driven-development-c4de6dce5c/).
