# Top JavaScript Interview Questions & Answers

> A comprehensive guide covering the most important JavaScript concepts asked in interviews — from basics to advanced.

---

## 1. What is the difference between `var`, `let`, and `const`?

`var` is function-scoped, can be redeclared and updated, and is hoisted with an undefined value. `let` is block-scoped, can be updated but not redeclared. `const` is block-scoped and cannot be updated or redeclared. Always prefer `const` by default, use `let` when you need to reassign, and avoid `var` in modern JavaScript.

| Feature | `var` | `let` | `const` |
|---|---|---|---|
| Scope | Function | Block | Block |
| Redeclare | ✅ | ❌ | ❌ |
| Reassign | ✅ | ✅ | ❌ |
| Hoisted | ✅ (undefined) | ✅ (TDZ) | ✅ (TDZ) |

---

## 2. What is Hoisting?

Hoisting is JavaScript's behavior of moving declarations to the top of their scope before execution. `var` declarations are hoisted and initialized as `undefined`. Function declarations are fully hoisted. `let` and `const` are hoisted but not initialized — accessing them before declaration throws a `ReferenceError`. This is called the **Temporal Dead Zone**.

---

## 3. What is a Closure?

A closure is when a function remembers and accesses variables from its outer scope even after that outer function has finished executing.

```javascript
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}
const counter = outer();
counter(); // 1
counter(); // 2
```

> Closures are used in data privacy, factory functions, and callbacks.

---

## 4. What is the difference between `==` and `===`?

`==` is loose equality — it compares values after type coercion. `===` is strict equality — it compares both value and type without coercion. Always use `===` to avoid unexpected bugs.

```javascript
0 == "0"   // true  (type coercion)
0 === "0"  // false (different types)
```

---

## 5. What is Event Delegation?

Event delegation is attaching a single event listener to a parent element instead of adding listeners to every child. It works because of **event bubbling** — events propagate up from child to parent. This improves performance and works for dynamically added elements.

```javascript
document.getElementById("list").addEventListener("click", function(e) {
  if (e.target.tagName === "LI") {
    console.log(e.target.innerText);
  }
});
```

---

## 6. What is Event Bubbling and Event Capturing?

Event **bubbling** means an event starts from the target element and bubbles up to the root. Event **capturing** means the event starts from the root and goes down to the target. By default, event listeners use bubbling. You can stop bubbling using `e.stopPropagation()`.

---

## 7. What is the difference between `null` and `undefined`?

`undefined` means a variable has been declared but not assigned a value. `null` is an intentional empty value assigned by the developer.

```javascript
typeof undefined  // "undefined"
typeof null       // "object" ← known JavaScript bug
```

---

## 8. What is the `this` Keyword?

`this` refers to the object that is currently executing the function. Its value depends on how the function is called:

- In a **method** → refers to the object
- In a **regular function** → refers to global object (or `undefined` in strict mode)
- In an **arrow function** → inherits `this` from its surrounding lexical scope

---

## 9. What is the difference between Regular Functions and Arrow Functions?

Arrow functions don't have their own `this` — they inherit it from the surrounding scope. They also cannot be used as constructors and don't have the `arguments` object. Regular functions have their own `this` and `arguments`. Arrow functions are ideal for callbacks and situations where you want to preserve the outer `this`.

---

## 10. What is a Promise and what are its states?

A Promise is an object representing the eventual completion or failure of an asynchronous operation. It has three states:

- **Pending** — initial state
- **Fulfilled** — operation succeeded
- **Rejected** — operation failed

You handle results using `.then()`, `.catch()`, and `.finally()`.

---

## 11. What is the difference between Promise methods?

| Method | Behavior |
|---|---|
| `Promise.all` | Waits for all to resolve. Rejects if any one rejects |
| `Promise.allSettled` | Waits for all to finish regardless of success or failure |
| `Promise.race` | Resolves/rejects as soon as the first promise settles |
| `Promise.any` | Resolves as soon as the first promise fulfills |

---

## 12. What is async/await?

`async/await` is syntactic sugar over Promises that makes asynchronous code look synchronous. An `async` function always returns a Promise. `await` pauses execution until the Promise resolves.

```javascript
async function fetchData() {
  try {
    const response = await fetch(url);
    const data = await response.json();
    return data;
  } catch (error) {
    console.log(error);
  }
}
```

---

## 13. What is the Event Loop?

The event loop allows JavaScript to be non-blocking despite being single-threaded. It continuously checks the call stack — if it's empty, it picks tasks from:

- **Microtask queue** → Promise callbacks (higher priority)
- **Macrotask queue** → setTimeout, setInterval, DOM events

> Microtasks always run before macrotasks.

---

## 14. What is the difference between Microtasks and Macrotasks?

```javascript
console.log("start");
setTimeout(() => console.log("setTimeout"), 0);
Promise.resolve().then(() => console.log("promise"));
console.log("end");

// Output: start → end → promise → setTimeout
```

- **Microtasks**: Promise callbacks, `queueMicrotask`
- **Macrotasks**: `setTimeout`, `setInterval`, DOM events

---

## 15. What is Debouncing and Throttling?

**Debouncing** delays the execution of a function until after a specified time has passed since the last call. Used for search input.

**Throttling** ensures a function is called at most once in a specified time interval. Used for scroll or resize events.

---

## 16. What is Prototype and Prototypal Inheritance?

Every JavaScript object has a hidden `__proto__` property pointing to its prototype. When you access a property, JavaScript looks on the object first, then its prototype, then up the chain — this is called the **prototype chain**. This is how JavaScript implements inheritance.

---

## 17. What is the difference between `call`, `apply`, and `bind`?

All three explicitly set the value of `this` for a function.

| Method | Invokes Immediately | Arguments |
|---|---|---|
| `call` | ✅ | Passed individually |
| `apply` | ✅ | Passed as an array |
| `bind` | ❌ | Returns new bound function |

---

## 18. What is Memoization?

Memoization is an optimization technique where you cache the result of a function call based on its inputs so that repeated calls with the same inputs return the cached result instead of recomputing. Useful for expensive pure functions.

---

## 19. What is the difference between Deep Copy and Shallow Copy?

A **shallow copy** copies only the top-level properties — nested objects still reference the same memory. A **deep copy** creates a completely independent clone including all nested objects.

```javascript
// Shallow copy
const shallow = { ...original };

// Deep copy
const deep = JSON.parse(JSON.stringify(original));
```

---

## 20. What is the difference between Array methods?

| Method | Returns | Mutates? |
|---|---|---|
| `forEach` | Nothing | No |
| `map` | New array (same length) | No |
| `filter` | New array (matching elements) | No |
| `reduce` | Single accumulated value | No |
| `find` | First matching element | No |

---

## 21. What are Generators in JavaScript?

Generators are functions that can pause and resume execution using the `yield` keyword. They return an iterator and are useful for lazy evaluation and infinite sequences.

```javascript
function* generator() {
  yield 1;
  yield 2;
  yield 3;
}
const gen = generator();
gen.next(); // { value: 1, done: false }
```

---

## 22. What is the difference between `localStorage`, `sessionStorage`, and `cookies`?

| Feature | localStorage | sessionStorage | Cookies |
|---|---|---|---|
| Expiry | Never (manual clear) | Tab close | Configurable |
| Size | ~5MB | ~5MB | ~4KB |
| Sent to server | ❌ | ❌ | ✅ |
| Accessible | Client only | Client only | Both |

---

## 23. What is IIFE?

An **Immediately Invoked Function Expression** is a function that is defined and called immediately. It creates its own scope, preventing variable pollution in the global scope.

```javascript
(function() {
  let x = 10;
  console.log(x);
})();
```

---

## 24. What is the Temporal Dead Zone?

The Temporal Dead Zone (TDZ) is the period between when a `let` or `const` variable is hoisted and when it is initialized. Accessing the variable during this period throws a `ReferenceError`.

```javascript
console.log(a); // ReferenceError: Cannot access 'a' before initialization
let a = 5;
```

---

## 25. What is Optional Chaining and Nullish Coalescing?

**Optional chaining** `?.` safely accesses nested properties without throwing an error if an intermediate value is null or undefined.

**Nullish coalescing** `??` returns the right-hand value only if the left is `null` or `undefined` — unlike `||` which also triggers for `0` or empty string.

```javascript
const name = user?.profile?.name ?? "Guest";
```

---

## Quick Revision Cheatsheet

| Concept | One-liner |
|---|---|
| Closure | Function remembers outer scope variables |
| Hoisting | Declarations moved to top before execution |
| Event Loop | Manages async in single-threaded JS |
| Prototype | Object inheritance via prototype chain |
| this | Refers to current execution context |
| Promise | Represents future async value |
| Debounce | Delay execution until user stops |
| Throttle | Execute at most once per interval |
| Memoization | Cache function results |
| IIFE | Self-invoking function for scope isolation |

---

*Good luck with your interview! 🚀*
