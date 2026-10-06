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

     var is function-scoped and can be redeclared and reassigned. let and const are block-scoped; let can be reassigned, while const cannot. let and const are also subject to the Temporal Dead Zone.

15. What is a closure, and when would you use it?

    A closure is when a function retains access to variables from its lexical scope even after the outer function has finished executing. Closures are useful for creating private state, maintaining state between function calls, callbacks, event handlers, and asynchronous operations.
     
16. What is the difference between == and ===?

    == performs loose equality and can perform type coercion before comparing values. === performs strict equality and checks both the value and the type without coercion.

17. What is the difference between null and undefined?

    undefined generally means that a value hasn’t been assigned or doesn’t exist, while null is an intentional assignment representing the absence of a value. undefined is commonly produced automatically by JavaScript, whereas null is usually assigned explicitly by the developer.

18. What is the difference between primitive and reference types?

    Primitive values are copied by value, so assigning one primitive variable to another creates an independent value. Objects, arrays, and functions are reference values, so assigning them to another variable copies the reference to the same underlying object. Therefore, modifying the object through one reference can affect the other.

19. What is the difference between shallow copy and deep copy?

    A shallow copy creates a new top-level object but keeps references to nested objects, so changes to nested data can affect the original. A deep copy recursively creates independent copies of nested objects, so changes to the copy don’t affect the original.

20. How does the this keyword work in JavaScript?

    this is determined primarily by how a function is called. In a method call, it usually refers to the object before the dot. Regular functions get this from their invocation context, while arrow functions don’t have their own this and inherit it from the surrounding scope. call, apply, and bind can explicitly control this for regular functions.

21. What is the difference between arrow functions and regular functions?

    Arrow functions differ from regular functions mainly in how they handle this. Regular functions have their own this, which is determined by how they’re called, while arrow functions don’t have their own this and inherit it from the surrounding scope. Arrow functions also don’t have their own arguments object and cannot be used as constructors with new. They are especially useful for callbacks because they preserve the surrounding this.

22. What is the difference between microtasks and macrotasks?

    Microtasks and macrotasks are different queues used by JavaScript’s event loop. Promise callbacks and queueMicrotask are microtasks, while setTimeout, setInterval, and many DOM events are macrotasks. After the current synchronous task finishes, the event loop drains all available microtasks before starting the next macrotask. That’s why Promise callbacks usually execute before a setTimeout callback, even when the timeout is set to zero. 

23. What is the difference between async/await and Promises?

    async/await is syntactic sugar built on top of Promises. Promises are handled using methods such as .then(), .catch(), and .finally(), while async/await allows asynchronous code to be written in a more synchronous-looking style. An async function always returns a Promise, and await pauses that async function until the Promise settles without blocking the JavaScript thread.

24. What is the difference between Promise.all(), Promise.race(), and Promise.allSettled()?

    Promise.all() waits for all promises and rejects as soon as one rejects, so it’s useful when every operation is required. Promise.race() settles as soon as the first promise settles, whether fulfilled or rejected. Promise.allSettled() waits for every promise to settle and returns the status and result of each one, making it useful when individual failures shouldn’t stop us from receiving the other results.

25. How does JavaScript handle asynchronous operations?

    JavaScript is single-threaded, so it uses the event loop to handle asynchronous operations without blocking the main thread. Asynchronous work is handled by the JavaScript runtime, such as Web APIs in a browser or Node.js APIs. Once the operation is ready, its callback or Promise continuation is placed into a task queue. The event loop moves it to the call stack when the stack is empty, with microtasks such as Promise callbacks being processed before the next macrotask.

26. What is callback hell, and how can you avoid it?

    Callback hell occurs when multiple asynchronous operations are nested inside each other’s callbacks, making the code difficult to read, maintain, and handle errors in. It can be avoided by using Promises with chaining, async/await with try/catch, and by breaking complex callback logic into separate functions.

27. What is the difference between map(), filter(), and reduce()?

    map() transforms every element and returns a new array with the same length. filter() returns a new array containing only elements that satisfy a condition. reduce() processes the array and accumulates the elements into a single result, which can be a number, object, array, or another data structure.

28. What is the difference between forEach() and map()?

    forEach() is mainly used for performing side effects on each array element and returns undefined, while map() transforms each element and returns a new array containing the results. I use map() when I need the transformed data and forEach() when I simply need to perform an action for each item.

29. How does the sort() method work?

    sort() sorts the elements of an array and mutates the original array. By default, it converts elements to strings and sorts them lexicographically, so for numbers I usually provide a comparator such as (a, b) => a - b. If I don’t want to mutate the original array, I can use toSorted() or create a copy before sorting.

30. How do you remove duplicate elements from an array?

    The simplest way to remove duplicates from an array is to use a Set, because a Set only stores unique values. For example, [...new Set(array)]. If I’m dealing with objects, I would usually use a Map or filter() based on a unique property such as an id.

31. How do you flatten a nested array?

    I would normally use flat() to flatten a nested array. By default, it flattens one level, but I can specify a depth such as flat(2) or use flat(Infinity) to flatten all levels. If I need to implement it myself, I can use reduce(

    ~~~js
    function flatten(array) {
      return array.reduce((result, item) => {
         if (Array.isArray(item)) {
         return result.concat(flatten(item));
        }

        return result.concat(item);
       }, []);
     }
     ~~~

32. How do you group an array of objects by a property?

    I can group an array of objects by a property using reduce(). I use the property value as a key in the accumulator, create an array if that group doesn’t exist, and then push the object into it. In modern JavaScript, I can also use Object.groupBy(), which provides a more concise built-in solution.

33. What is a prototype in JavaScript?

    A prototype is an object that JavaScript objects can inherit properties and methods from. When a property or method isn’t found directly on an object, JavaScript searches its prototype and continues up the prototype chain. JavaScript uses prototype-based inheritance, and even ES6 classes use prototypes behind the scenes.

34. What is the difference between call(), apply(), and bind()?


35. What is memoization, and how would you implement it?

    Memoization is an optimization technique where we cache the result of a function based on its input. When the function is called again with the same input, we return the cached result instead of recalculating it. I would typically implement it using a closure and a Map to store the arguments and results. It’s most useful for expensive, pure functions, but it increases memory usage because of the cache.

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
