### interview questions

## JavaScript

1. What is a higher order function
   
     A higher-order function is a function that either accepts another function as an argument, returns a function as its result, or both. This concept is a core part of JavaScript's functional programming capabilities and is widely used for creating modular, reusable, and expressive code.

2. What is the Temporal Dead Zone

   The Temporal Dead Zone (TDZ) refers to the period between the start of a block and the point where a variable declared with let or const is initialized. During this time, the variable exists in scope but cannot be accessed, and attempting to do so results in a ``ReferenceError``.

3. What is the currying function

     Currying is the process of transforming a function with multiple arguments into a sequence of nested functions, each accepting only one argument at a time.
   
4. What is Hoisting
    Hoisting is JavaScript's default behavior where variable and function declarations are moved to the top of their scope before code execution. This means you can access certain variables and functions even before they are defined in the code.

5. What is a promise
 
    A Promise is a JavaScript object that represents the eventual completion (or failure) of an asynchronous operation and its resulting value. It acts as a placeholder for a value that may not be available yet but will be resolved in the future.

   - ``pending``: This is an initial state of the Promise before an operation begins
   - ``fulfilled``: This state indicates that the specified operation was completed.
   - ``rejected``: This state indicates that the operation did not complete. In this case an error value will be thrown

6. What is a callback function

     A callback function is a function passed into another function as an argument. This function is invoked inside the outer function to complete an action. Let's take a simple example of how to use callback function

7. What is event bubbling

    Event bubbling is a type of event propagation in which an event first triggers on the innermost target element (the one the user interacted with), and then bubbles up through its ancestors in the DOM hierarchy — eventually reaching the outermost elements, like the document or window.

   ``js
  // Bubbling phase (default)
  parent.addEventListener("click", function () {
    console.log("Parent");
  });
   ``

8. 








## TypeScript

## React

## Node

## Git
