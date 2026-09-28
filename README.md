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

6. What is a promise
 
    A Promise is a JavaScript object that represents the eventual completion (or failure) of an asynchronous operation and its resulting value. It acts as a placeholder for a value that may not be available yet but will be resolved in the future.

   - ``pending``: This is an initial state of the Promise before an operation begins
   - ``fulfilled``: This state indicates that the specified operation was completed.
   - ``rejected``: This state indicates that the operation did not complete. In this case an error value will be thrown

7. What is a callback function

     A callback function is a function passed into another function as an argument. This function is invoked inside the outer function to complete an action. Let's take a simple example of how to use callback function

8. What is event bubbling

    Event bubbling is a type of event propagation in which an event first triggers on the innermost target element (the one the user interacted with), and then bubbles up through its ancestors in the DOM hierarchy — eventually reaching the outermost elements, like the document or window.

   ```js
     // Bubbling phase (default)
     parent.addEventListener("click", function () {
       console.log("Parent");
     });
   ```

9. What is event capturing

      Event capturing is a phase of event propagation in which an event is first intercepted by the outermost ancestor element, then travels downward through the DOM hierarchy until it reaches the target (innermost) element.

    ```js
    // Capturing phase: parent listener (runs first)
   parent.addEventListener("click", function () {
     console.log("Parent (capturing)");
   }, true); // `true` enables capturing
    // in Function

    function firstFunc(event) {
     alert("DIV 1");
     event.stopPropagation();
   }
    ```
    
10. What are JS data types

      1. string
      2. number
      3. boolean
      4. object
      5. null
      6. undefiend
      7. bigint
      8. symbol

11. What is the event loop

       The event loop is a process that continuously monitors both the call stack and the event queue and checks whether or not the call stack is empty. If the call stack is empty and there are pending events in the event queue, the event loop dequeues the event from the event queue and pushes it to the call stack. The call stack executes the event, and any additional events generated during the execution are added to the end of the event queue.

12. What is the call stack

    Call Stack is a data structure for javascript interpreters to keep track of function calls(creates execution context) in the program. It has two major actions,

    - Whenever you call a function for its execution, you are pushing it to the stack.
    - Whenever the execution is completed, the function is popped out of the stack.

13. What is heap

      Heap(Or memory heap) is the memory location where objects are stored when we define variables. i.e, This is the place where all the memory allocations and de-allocation take place. Both heap and call-stack are two containers of JS runtime. Whenever runtime comes across variables and function declarations in the code it stores them in the Heap.
         
14. What is the difference between var, let, and const?
15. What is hoisting in JavaScript?
16. What is a closure, and when would you use it?
17. What is the difference between == and ===?
18. What is the difference between null and undefined?
19. What is the difference between primitive and reference types?
20. What is the difference between shallow copy and deep copy?
21. How does the this keyword work in JavaScript?
22. What is the difference between arrow functions and regular functions?
23. What is the difference between microtasks and macrotasks?
24. What is the difference between async/await and Promises?
25. What is the difference between Promise.all(), Promise.race(), and Promise.allSettled()?
26. How does JavaScript handle asynchronous operations?
27. What is callback hell, and how can you avoid it?
28. What is the difference between map(), filter(), and reduce()?
29. What is the difference between forEach() and map()?
30. How does the sort() method work?
31. How do you remove duplicate elements from an array?
32. How do you flatten a nested array?
33. How do you group an array of objects by a property?
34. What is a prototype in JavaScript?
35. What is the difference between call(), apply(), and bind()?
36. What is memoization, and how would you implement it?

## TypeScript

## React

   1. What is the Virtual DOM?
   2. What is the difference between useState and useReducer?
   3. What is the difference between useMemo and useCallback?

## Node

1. What is Node.js and why is it used?
   
      Node.js is an open-source, cross-platform JavaScript runtime environment that executes code outside of a web browser. It is built on V8, the same JavaScript engine within Chrome, and optimized for high performance. This environment, coupled with an event-driven, non-blocking I/O framework, is tailored for server-side web development and more.
   
3. How does Node.js handle child threads?
4. Describe the event-driven programming in Node.js.
5. What is the event loop in Node.js?
6. What is the difference between Node.js and traditional web server technologies?
7. Explain what "non-blocking" means in Node.js.
8. What is "npm" and what is it used for?



## Git
