## Assignment

### Brief

In this assignment, we will perform group research on:

1. The difference between Asynchronous Programming and Multithreaded Programming
1. The various approach to run `CompletableFuture` that is used for asynchronous programming

> Note: No coding assignment

### Async vs Multithreaded Programming

In your group, research and discuss the difference between Asynchronous Programming and Multithreaded Programming.

Q1: What is asynchronous programming?

```
Asynchronous programming involves executing tasks without blocking the main program flow, allowing the program to continue running while waiting for asynchronous operations to complete. It can be single threaded, as seen in Javascript using even loop or multi threaded in Java using CompletableFuture.
```

Q2: What is multithreaded programming?

```
Multithreaded programming involves the creation and management of multiple threads within a program that executes task concurrently. The treads may run using time slicing on a single core or in parallel on multiple cores, depending on the OS and CPU capabilities.
```

Q3: What are the similaries and differences between them?

```
Differences
1. Asynchronous programming can be either single or multi threaded while multi threaded programming can only be multithreaded

2. Asynchronous programming manages asyncronous task by using event loops or CompletableFuture while multi threaded program manages it using the CPU cores.

Similarities
1. Both Asynchronous and multi treaded program does not block the main program's code by allowing other task to be performed while waiting for long-running operations to complete

```

### Understanding `CompletableFuture`

Q1: What is the difference between `supplyAsync` and `runAsync` in `CompletableFuture`?

```
supplyAsync: Used if the method returns a value

runAsync: Used if the method does not returns a value

CompletableFuture: Similar to a promise in javascript, it holds the return value of the method which can be access with the .join() method
```

Q2: What is the difference between `thenAccept`, `thenRun`, and `thenApply` in `CompletableFuture`?

```
thenAccept: It consumes the result of a CompletableFuture without returning a value. It performs an action using the result but does not transform it or return a new CompletableFuture with a different result.

ThenApply: It consumes the results of a CompletableFuture, transforms it and return a new CompletableFuture with transformed value. The value can be access with .join() method.

ThenRun: Runs a task after the CompletableFuture completes without using its result. It accepts a Runnable and does not consume the value of the CompletableFuture.

```

### Submission

- Submit the URL of the GitHub Repository that contains your work to NTU black board.
- Should you reference the work of your classmate(s) or online resources, give them credit by adding either the name of your classmate or URL.

### References

_Example of Referencing Classmate_

Referenced the code block below from Terence.

```js
function printMe() {
  console.log("I am a reference example");
}
```

_Example of Referencing Online Resources_

- https://developer.mozilla.org/en-US/
- https://www.w3schools.com/html/
- https://stackoverflow.com/questions/14494747/how-to-add-images-to-readme-md-on-github
