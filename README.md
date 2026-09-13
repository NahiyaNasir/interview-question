# 🧠 Full-Stack Web Developer Interview Questions (140+ Questions)

> A complete, beautifully organized collection of full-stack web development interview questions and answers — JavaScript, TypeScript, React, Next.js, Node.js, Express.js, Databases & Distributed Systems — curated for quick revision before technical interviews.

[![GitHub](https://img.shields.io/badge/GitHub-NahiyaNasir-181717?style=flat&logo=github)](https://github.com/NahiyaNasir/interview-question)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-f7df1e?style=flat&logo=javascript)](https://github.com/NahiyaNasir/interview-question)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-3178c6?style=flat&logo=typescript)](https://github.com/NahiyaNasir/interview-question)
[![React](https://img.shields.io/badge/React-18+-61dafb?style=flat&logo=react)](https://github.com/NahiyaNasir/interview-question)
[![Next.js](https://img.shields.io/badge/Next.js-14%2F15-000000?style=flat&logo=next.js)](https://github.com/NahiyaNasir/interview-question)
[![Node.js](https://img.shields.io/badge/Node.js-Backend-339933?style=flat&logo=node.js)](https://github.com/NahiyaNasir/interview-question)
[![Express](https://img.shields.io/badge/Express.js-Framework-000000?style=flat&logo=express)](https://github.com/NahiyaNasir/interview-question)
[![Database](https://img.shields.io/badge/Database-SQL%20%26%20NoSQL-4479a1?style=flat&logo=postgresql)](https://github.com/NahiyaNasir/interview-question)

---

## 📚 Complete Table of Contents

| # | Section | Questions Covered |
|---|---|---|
| 1 | [💬 Behavioral Interview Questions](#-behavioral-interview-questions) | Questions 1 – 5 |
| 2 | [🟨 JavaScript Core, Functions & Modern JS](#-javascript-interview-questions) | Questions 1 – 30 |
| 3 | [🔷 TypeScript Fundamentals & Advanced Types](#-typescript-interview-questions--answers) | TypeScript Questions |
| 4 | [⚛️ React — Components, Hooks & State Management](#️-react-interview-questions) | Questions 31 – 60 |
| 5 | [▲ Next.js — App Router, SSR, SSG & Server Actions](#-nextjs-interview-questions--answers) | Next.js Questions 1 – 30 |
| 6 | [🟢 Node.js Architecture, I/O & Streams](#-nodejs-interview-questions--answers) | Node.js Questions 1 – 15 |
| 7 | [🚂 Express.js Framework, Middleware & Security](#-expressjs-interview-questions) | Express.js Questions 1 – 15 |
| 8 | [🗄️ Database, Distributed Systems & Indexing](#️-database--distributed-systems-interview-questions) | Questions 75 – 108 |
| 9 | [⭐ Quick Revision Checklist & Mindset](#-quick-revision-checklist) | Checklist & Tips |

---

## 💬 Behavioral Interview Questions

---

### Q1. Tell Me About Yourself

I’m a full-stack web developer who loves turning complex ideas into clean, fast, and easy-to-use web applications. Over the last few years, I’ve built everything from healthcare management portals to media streaming platforms and e-commerce stores.

My daily focus is on modern web tools like **Next.js**, **React**, **Node.js**, **PostgreSQL**, and **Tailwind CSS**. Beyond just writing code that works, I care a lot about smooth UI, fast performance, and clean database architecture. I really enjoy taking a project from an initial feature idea all the way to a live, working product.

---

### Q2. What Is Your Strength?

My biggest strength is my **problem-solving mindset** and ability to pick up new tools fast.

When I run into a tricky bug—whether it’s handling real-time status updates in a database, setting up complex cron jobs, or debugging a tricky third-party API integration—I don't get frustrated. I systematically trace the problem, break it down, and fix it. I’m also super reliable when it comes to ownership; if a task is handed to me, I make sure it gets done right and on time.

---

### Q3. What Is Your Weakness?

Sometimes I get too caught up in tweaking small UI details or optimizing code early on, which can slow down my initial speed.

For example, I’ll find myself spending extra time perfecting an animation or re-factoring a component when the core feature just needs to be shipped first. To fix this, I’ve started setting strict timer targets: **get the functional MVP out first, get feedback, and then go back to polish the UI and performance.**

---

### Q4. Why Should We Hire You?

Because I bring a solid balance of **technical skills, speed, and real product experience**.

I don't just write code off a spec sheet; I think about the end user and how the app will handle real-world edge cases. Whether it’s setting up secure payment processing, managing complex database schemas, or crafting responsive interfaces with Tailwind and Framer Motion, I know how to deliver complete features without needing constant hand-holding. I’m ready to step in, collaborate with your team, and ship clean code from day one.

---

### Q5. Why Did You Choose Web Development as a Career?

Honestly, it comes down to **instant feedback and impact**.

With web development, you write a few lines of code, refresh the browser, and suddenly there’s a real interactive tool on your screen that anyone in the world can use. That feeling never gets old for me. I love that the web is constantly evolving—there’s always a new framework to try, a faster way to query a database, or a better way to design an interface. It keeps work interesting every single day.

---

## 🟨 JavaScript Interview Questions

### Variables & Hoisting

---

### Q1. What Is the Difference Between var, let, and const?

`var`, `let`, and `const` are used to create variables in JavaScript with different scoping and reassignment rules:

| Keyword | Scope | Re-declarable? | Re-assignable? | Hoisted? |
|---|---|---|---|---|
| `var` | Function scope | ✅ Yes | ✅ Yes | Hoisted (initialized as `undefined`) |
| `let` | Block scope | ❌ No | ✅ Yes | Hoisted (Temporal Dead Zone) |
| `const` | Block scope | ❌ No | ❌ No | Hoisted (Temporal Dead Zone) |

#### Examples:

**var:**
```javascript
var name = "John";
var name = "Mike"; // Redeclared
console.log(name); // Mike
```

**let:**
```javascript
let age = 20;
age = 25;          // Value can be updated
// let age = 30;   // ❌ SyntaxError: Identifier 'age' has already been declared
console.log(age);  // 25
```

**const:**
```javascript
const country = "Bangladesh";
// country = "India"; // ❌ TypeError: Assignment to constant variable.
```

**In simple words:**
* `var` → old way, function scoped, can be redeclared.
* `let` → block scoped, value can be changed.
* `const` → block scoped, value cannot be reassigned.

---

### Q2. Explain the Concept of Hoisting in JavaScript

Hoisting is JavaScript's default behavior of moving declarations to the top of the current scope before code execution.

#### 1. Function Declarations:
Function declarations are completely hoisted, so they can be called before they are defined.

```javascript
greet(); // Output: "Hello"

function greet() {
  console.log("Hello");
}
```

#### 2. var Variables:
Variables declared with `var` are hoisted, but only their declaration (initialized with `undefined`).

```javascript
console.log(name); // undefined
var name = "John";
```

#### 3. let and const (Temporal Dead Zone):
`let` and `const` declarations are hoisted to the top of the block, but are not initialized. Accessing them before declaration causes a `ReferenceError` due to the **Temporal Dead Zone (TDZ)**.

```javascript
console.log(age); // ❌ ReferenceError: Cannot access 'age' before initialization
let age = 20;
```

---

### Core JavaScript

---

### Q3. What Are the Primitive Data Types in JavaScript?

Primitive data types represent a single immutable value that is not an object and has no methods.

There are **7 primitive data types**:
1. **String** — text data
2. **Number** — integer or floating-point numbers
3. **BigInt** — arbitrarily large integers
4. **Boolean** — `true` or `false`
5. **Undefined** — variable declared but has no value assigned
6. **Null** — intentional absence of any object value
7. **Symbol** — unique and immutable identifier

#### Example:
```javascript
let name = "John";        // String
let age = 25;             // Number
let bigNumber = 123n;     // BigInt
let isStudent = true;     // Boolean
let address;              // Undefined
let data = null;          // Null
let id = Symbol("id");    // Symbol
```

---

### Q4. What Is the Difference Between == and ===?

| Operator | Name | Behavior | Example | Result |
|---|---|---|---|---|
| `==` | Loose Equality | Compares values after performing type coercion | `5 == "5"` | `true` |
| `===` | Strict Equality | Compares both value **and** data type without coercion | `5 === "5"` | `false` |

#### Example:
```javascript
// Loose equality (performs type conversion)
console.log(5 == "5");   // true
console.log(0 == false); // true

// Strict equality (checks value and type)
console.log(5 === "5");   // false
console.log(0 === false); // false
```

> 💡 **Best Practice:** In modern JavaScript, always prefer `===` because it prevents unexpected bugs caused by automatic type coercion.

---

### Functions & Scope

---

### Q5. Explain How Closures Work in JavaScript

A **closure** is created when an inner function retains access to variables from its outer (lexical) scope, even after the outer function has finished executing.

#### Example:
```javascript
function counter() {
  let count = 0;

  return function () {
    count++;
    return count;
  };
}

const increase = counter();

console.log(increase()); // 1
console.log(increase()); // 2
console.log(increase()); // 3
```

**Why it matters:**
* Data privacy (encapsulation)
* Factory functions
* Memoization and currying

---

### Q6. What Is the Difference Between null and undefined?

| Characteristic | `undefined` | `null` |
|---|---|---|
| **Meaning** | A variable has been declared but not assigned a value. | An intentional assignment representing "no value" or "empty". |
| **Type (`typeof`)** | `"undefined"` | `"object"` *(historical JavaScript quirk)* |
| **Origin** | Generated automatically by JavaScript. | Assigned intentionally by developers. |

#### Example:
```javascript
let name;
console.log(name);         // undefined
console.log(typeof name);  // "undefined"

let data = null;
console.log(data);         // null
console.log(typeof data);  // "object"

console.log(null == undefined);  // true (loose)
console.log(null === undefined); // false (strict)
```

---

### Q7. What Are Arrow Functions and How Do They Differ from Regular Functions?

Arrow functions (introduced in ES6) provide a cleaner, shorter syntax for writing functions.

#### Syntax Comparison:
```javascript
// Regular Function
function add(a, b) {
  return a + b;
}

// Arrow Function
const add = (a, b) => a + b;
```

#### Key Differences:
1. **`this` binding:** Arrow functions do not have their own `this`; they lexically inherit `this` from the surrounding execution context.
2. **`arguments` object:** Arrow functions do not have their own `arguments` object (use rest parameters `...args` instead).
3. **Constructor:** Arrow functions cannot be used as constructors with `new` and do not have a `prototype` property.

---

### Q8. What Is the Scope Chain in JavaScript?

The **scope chain** is the mechanism JavaScript uses to resolve variable names. When code references a variable, JavaScript searches:
1. The current local scope.
2. The enclosing (outer) function scopes one level up.
3. The global scope.

If not found in any scope up to the global scope, a `ReferenceError` is thrown.

#### Example:
```javascript
let name = "John"; // Global scope

function greet() {
  function sayHello() {
    console.log(name); // Resolved from outer global scope
  }
  sayHello();
}

greet(); // Output: "John"
```

---

### Q9. Explain the Concept of the Temporal Dead Zone (TDZ)

The **Temporal Dead Zone (TDZ)** is the period between entering a block scope and the actual line where a `let` or `const` variable is declared. Accessing the variable during this window throws a `ReferenceError`.

#### Example:
```javascript
{
  // TDZ begins for variable 'age'
  console.log(age); // ❌ ReferenceError: Cannot access 'age' before initialization

  let age = 25; // TDZ ends
  console.log(age); // 25
}
```

---

### Q10. What Is a Pure Function?

A **pure function** has two strict rules:
1. **Deterministic:** Given the same arguments, it will always return the exact same output.
2. **No Side Effects:** It does not modify any external state, variables, or I/O outside its scope.

#### Example:
```javascript
// Pure function
function add(a, b) {
  return a + b;
}

console.log(add(2, 3)); // 5
console.log(add(2, 3)); // 5 (always 5)
```

---

### Q11. What Is the Difference Between Function Declaration and Function Expression?

```javascript
// 1. Function Declaration (hoisted completely)
greet(); // Works! Output: "Hello"

function greet() {
  console.log("Hello");
}

// 2. Function Expression (only the variable is hoisted)
// sayHi(); // ❌ TypeError: sayHi is not a function

const sayHi = function () {
  console.log("Hi");
};
```

---

### Q12. What Are Default Parameters in JavaScript?

Default parameters allow formal parameters to be initialized with default values if no value or `undefined` is passed.

#### Example:
```javascript
function greet(name = "Guest") {
  console.log(`Hello ${name}`);
}

greet("John"); // Hello John
greet();       // Hello Guest
```

---

### Q13. What Is the typeof Operator?

The `typeof` operator returns a string indicating the type of the unevaluated operand.

#### Example:
```javascript
console.log(typeof "Hello");         // "string"
console.log(typeof 25);              // "number"
console.log(typeof true);            // "boolean"
console.log(typeof undefined);       // "undefined"
console.log(typeof {});              // "object"
console.log(typeof []);              // "object"
console.log(typeof null);            // "object" (known quirk)
console.log(typeof function () {});  // "function"
```

---

### Q14. Explain Type Coercion in JavaScript

Type coercion is the automatic or implicit conversion of values from one data type to another (such as strings to numbers).

#### Example:
```javascript
// String coercion with '+'
console.log("5" + 2);   // "52" (number 2 converted to string)

// Numeric coercion with '-', '*', '/'
console.log("5" - 2);   // 3    (string "5" converted to number)
console.log("10" * 2);  // 20

// Boolean coercion
console.log(!0);        // true
console.log(Boolean(""));// false
```

---

### Modern JavaScript

---

### Q15. What Is an Immediately Invoked Function Expression (IIFE)?

An **IIFE** is a function that runs immediately as soon as it is defined:

#### Example:
```javascript
(function () {
  const privateVar = "I am private";
  console.log("IIFE executed!");
})();
// console.log(privateVar); // ❌ ReferenceError
```

> 💡 **Use case:** Used to create private scope and prevent polluting the global namespace.

---

### Q16. What Is Destructuring in JavaScript?

Destructuring is an ES6 expression that allows unpacking values from arrays or properties from objects into distinct variables.

#### Array Destructuring:
```javascript
const numbers = [10, 20, 30];
const [a, b, c] = numbers;
console.log(a, b, c); // 10 20 30
```

#### Object Destructuring:
```javascript
const user = { name: "John", age: 25 };
const { name, age } = user;
console.log(name, age); // John 25
```

---

### Q17. What Are the Spread and Rest Operators?

Both operators use the three dots syntax (`...`), but they perform opposite tasks:

| Operator | Purpose | Example |
|---|---|---|
| **Spread (`...`)** | Expands an iterable into individual elements. | `[...arr, 4, 5]` or `{ ...user, role: 'admin' }` |
| **Rest (`...`)** | Condenses multiple elements into a single array. | `function sum(...numbers)` |

#### Spread Example:
```javascript
const numbers = [1, 2, 3];
const newNumbers = [...numbers, 4, 5];
console.log(newNumbers); // [1, 2, 3, 4, 5]
```

#### Rest Example:
```javascript
function addNumbers(...numbers) {
  return numbers.reduce((sum, num) => sum + num, 0);
}
console.log(addNumbers(10, 20, 30)); // 60
```

---

### Q18. Explain the Difference Between map(), filter(), and reduce()

| Method | Description | Return Value |
|---|---|---|
| `map()` | Transforms each item in the array | A new array of the same length |
| `filter()` | Selects items that pass a conditional test | A new array with filtered items |
| `reduce()` | Accumulates all items into a single result | Single value (number, object, array, etc.) |

#### Example:
```javascript
const numbers = [1, 2, 3, 4, 5];

// map: multiply each item by 2
const doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6, 8, 10]

// filter: keep only numbers greater than 2
const filtered = numbers.filter(num => num > 2);
console.log(filtered); // [3, 4, 5]

// reduce: sum all numbers
const sum = numbers.reduce((acc, curr) => acc + curr, 0);
console.log(sum); // 15
```

---

### Q19. What Is the Difference Between for...in and for...of?

| Loop | Iterates Over | Best Used For |
|---|---|---|
| `for...in` | **Keys / Property names** (enumerable properties) | Plain JavaScript Objects |
| `for...of` | **Values** of iterable collections | Arrays, Strings, Maps, Sets |

#### Example:
```javascript
const user = { name: "John", age: 25 };
for (let key in user) {
  console.log(key, "->", user[key]); // name -> John, age -> 25
}

const numbers = [10, 20, 30];
for (let num of numbers) {
  console.log(num); // 10, 20, 30
}
```

---

### Q20. What Are Template Literals and Tagged Templates?

**Template literals** use backticks (``) allowing embedded expressions (`${...}`) and multi-line strings.

```javascript
const name = "John";
const age = 25;
const message = `My name is ${name} and I am ${age} years old.`;
console.log(message); // "My name is John and I am 25 years old."
```

**Tagged templates** allow parsing template literals with a custom function:
```javascript
function highlight(strings, name) {
  return `${strings[0]}<mark>${name}</mark>`;
}

const name = "John";
console.log(highlight`Hello ${name}`); // "Hello <mark>John</mark>"
```

---

### Asynchronous JavaScript

---

### Q21. What Is the Event Loop in JavaScript?

JavaScript is single-threaded (executes one task at a time on the Call Stack). The **Event Loop** constantly coordinates:
1. **Call Stack:** Executes synchronous JavaScript code.
2. **Web APIs / Node APIs:** Handles async tasks (DOM events, timers, fetch).
3. **Microtask Queue:** Handles Promise callbacks, `queueMicrotask`, `process.nextTick`.
4. **Macrotask Queue:** Handles `setTimeout`, `setInterval`, I/O.

#### Example:
```javascript
console.log("Start");

setTimeout(() => {
  console.log("Timer");
}, 0);

Promise.resolve().then(() => {
  console.log("Promise (Microtask)");
});

console.log("End");
```

**Execution Order:**
```text
Start
End
Promise (Microtask)
Timer
```

---

### Q22. Explain How Promises Work in JavaScript

A **Promise** represents the eventual completion or failure of an asynchronous operation and its resulting value.

#### Three States:
1. **Pending:** Initial state, neither fulfilled nor rejected.
2. **Fulfilled:** The operation completed successfully.
3. **Rejected:** The operation failed.

#### Example:
```javascript
const myPromise = new Promise((resolve, reject) => {
  const success = true;

  if (success) {
    resolve("Operation successful!");
  } else {
    reject("Something went wrong.");
  }
});

myPromise
  .then(result => console.log(result))
  .catch(error => console.error(error))
  .finally(() => console.log("Done."));
```

---

### Q23. What Is async/await and How Does It Improve Upon Promises?

`async/await` is syntactic sugar built on top of Promises. It allows asynchronous code to be written and read like synchronous code, avoiding complex `.then()` promise chains.

#### Example:
```javascript
async function fetchData() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/todos/1");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Error fetching data:", error);
  }
}

fetchData();
```

---

### Objects & Advanced Concepts

---

### Q24. What Is the Difference Between call(), apply(), and bind()?

All three methods allow explicitly setting the execution context (`this`) of a function:

| Method | Executes Immediately? | How Arguments Are Passed |
|---|---|---|
| `call()` | ✅ Yes | Arguments passed individually: `fn.call(ctx, arg1, arg2)` |
| `apply()` | ✅ Yes | Arguments passed as an array: `fn.apply(ctx, [arg1, arg2])` |
| `bind()` | ❌ No (returns new function) | Arguments passed individually: `const newFn = fn.bind(ctx, arg1)` |

#### Example:
```javascript
function greet(city, country) {
  console.log(`Hello ${this.name} from ${city}, ${country}`);
}

const user = { name: "John" };

// call:
greet.call(user, "Dhaka", "Bangladesh");

// apply:
greet.apply(user, ["Dhaka", "Bangladesh"]);

// bind:
const boundGreet = greet.bind(user, "Dhaka", "Bangladesh");
boundGreet();
```

---

### Q25. What Is Prototypal Inheritance in JavaScript?

In JavaScript, every object has an internal link to another object called its **prototype**. When trying to access a property that doesn't exist directly on an object, JavaScript traverses up the prototype chain until it finds it or reaches `null`.

#### Example:
```javascript
const person = {
  greet() {
    console.log("Hello!");
  }
};

const student = Object.create(person);
student.name = "Alex";

student.greet(); // Output: "Hello!" (inherited from person prototype)
```

---

### Q26. Explain the Concept of the this Keyword

The `this` keyword refers to the object executing the current function. Its value depends entirely on **how** the function is invoked:

1. **Object Method:** Points to the owner object (`user.greet()`).
2. **Global Context:** Points to `window` in browsers or `global` in Node (`undefined` in strict mode).
3. **Event Listener:** Points to the DOM element that received the event.
4. **Constructor Function (`new`):** Points to the newly created instance.
5. **Arrow Function:** Has no own `this`; retains the `this` value of the enclosing lexical scope.

---

### Q27. What Are JavaScript Modules (import / export)?

ES Modules allow splitting JavaScript code into reusable, maintainable files.

#### Exporting:
```javascript
// math.js
export const add = (a, b) => a + b;
export default function multiply(a, b) {
  return a * b;
}
```

#### Importing:
```javascript
// app.js
import multiply, { add } from "./math.js";

console.log(add(2, 3));      // 5
console.log(multiply(2, 3)); // 6
```

---

### Q28. What Is the Difference Between Shallow Copy and Deep Copy?

| Copy Type | Behavior | How to create |
|---|---|---|
| **Shallow Copy** | Copies top-level properties. Nested objects still share references. | `{ ...obj }`, `Object.assign({}, obj)` |
| **Deep Copy** | Recursively duplicates all nested objects/arrays. Entirely independent. | `structuredClone(obj)` or `JSON.parse(JSON.stringify(obj))` |

#### Example:
```javascript
const user = {
  name: "John",
  address: { city: "Dhaka" }
};

// Shallow Copy
const shallow = { ...user };
shallow.address.city = "Chittagong";
console.log(user.address.city); // "Chittagong" ⚠️ (nested object was mutated!)

// Deep Copy
const deep = structuredClone(user);
deep.address.city = "Sylhet";
console.log(user.address.city); // Still "Chittagong" ✅ (safe!)
```

---

### Q29. What Are WeakMap and WeakSet?

`WeakMap` and `WeakSet` hold **weak references** to keys/values, meaning they do not prevent garbage collection if no other references exist to the stored objects.

#### Differences from Map/Set:
1. **Keys must be objects:** Primitive types are not allowed as keys in `WeakMap` or values in `WeakSet`.
2. **Non-enumerable:** You cannot loop over them (`for...of`, `.size`, or `.keys()` do not exist).
3. **Automatic memory cleanup:** Ideal for metadata caching and private class fields without memory leaks.

---

### Q30. Explain the Concept of Memoization

**Memoization** is an optimization technique that caches the results of expensive function calls based on the provided arguments.

#### Example:
```javascript
function memoize(fn) {
  const cache = {};

  return function (...args) {
    const key = JSON.stringify(args);
    if (cache[key]) {
      console.log("From cache:");
      return cache[key];
    }
    const result = fn(...args);
    cache[key] = result;
    return result;
  };
}

const square = (n) => {
  console.log("Calculating...");
  return n * n;
};

const memoizedSquare = memoize(square);

console.log(memoizedSquare(5)); // Calculating... -> 25
console.log(memoizedSquare(5)); // From cache: -> 25
```

---


## 🔷 TypeScript Interview Questions & Answers

---

### Q1. What is the difference between `type` and `interface`?

Both `type` and `interface` are used to define the structure of data in TypeScript.

```typescript
interface User {
  name: string;
  age: number;
}

type UserType = {
  name: string;
  age: number;
};

const user: User = {
  name: "Rahim",
  age: 25
};
```

#### Main Differences:

| Feature | `interface` | `type` |
|---|---|---|
| **Declaration Merging** | ✅ Yes (interfaces with same name auto-merge) | ❌ No (duplicate identifier error) |
| **Extends / Inheritance** | `interface Admin extends User` | `type Admin = User & { role: string }` (intersection) |
| **Unions & Primitives** | ❌ Cannot rename primitives or define unions directly | ✅ Can define unions (`type ID = string \| number`) |
| **Best Used For** | Object shapes, public library APIs, class contracts | Unions, tuples, mapped types, primitives |

```typescript
// Declaration merging with interface:
interface User {
  name: string;
}
interface User {
  age: number;
}
// User now has both 'name' and 'age'
```

> 💡 **Interview answer:** "I usually use `interface` for defining object shapes and contracts because of declaration merging and clear extensibility, and use `type` aliases when I need unions, intersections, primitives, tuples, or complex mapped types."

---

### Q2. Union vs Intersection Types

#### Union (`|`) — OR
A union type allows a value to be any one of several types.

```typescript
let id: string | number;

id = "ABC"; // ✅ Valid
id = 123;   // ✅ Valid
```

#### Intersection (`&`) — AND
An intersection type combines multiple types into one. The resulting value must satisfy **all** combined types.

```typescript
type Employee = {
  name: string;
};

type Manager = {
  teamSize: number;
};

type ManagerEmployee = Employee & Manager;

const person: ManagerEmployee = {
  name: "Rahim",
  teamSize: 10
};
```

**Quick Summary:**
* `|` = **OR** (can match any type)
* `&` = **AND** (must contain all properties)

---

### Q3. What is Type Inference?

Type inference means TypeScript automatically detects and assigns the type of a variable based on its initialized value, without needing explicit type annotations.

```typescript
let name = "Rahim"; // TypeScript infers type: string
// name = 123;      // ❌ Error: Type 'number' is not assignable to type 'string'

const age = 25;     // Inferred as literal type: 25
let count = 0;      // Inferred as: number
let isActive = true;// Inferred as: boolean
```

---

## ⚛️ React Interview Questions

### Components, Hooks & State Management

## Q31. What is React and what problem does it solve?

React is a JavaScript library used to build user interfaces, especially for web applications.

It helps developers build websites using small reusable parts called components. React also updates only the parts of the page that need to change, which makes applications faster and easier to manage.

---

## Q32. What is JSX and why is it used in React?

JSX stands for JavaScript XML. It lets us write HTML-like code inside JavaScript.

JSX makes React code easier to read and write because we can create the UI and its logic in the same place.

Example:

```jsx
const element = <h1>Hello World</h1>;
```

JSX is not directly understood by the browser. It is converted into normal JavaScript before running.

---

## Q33. What is the difference between functional and class components?

Functional components are normal JavaScript functions that return JSX.

Class components are JavaScript classes that extend `React.Component`.

Functional components are more commonly used today because they are simpler and support Hooks like `useState` and `useEffect`.

Example of a functional component:

```jsx
function Welcome() {
  return <h1>Hello</h1>;
}
```

---

## Q34. What is the virtual DOM and how does React use it?

The Virtual DOM is a lightweight copy of the real DOM.

When the state of a React application changes, React first updates the Virtual DOM. It then compares the new Virtual DOM with the previous one and updates only the necessary parts of the real DOM.

This helps React update the UI efficiently.

---

## Q35. Explain the useState hook with an example.

`useState` is a React Hook used to store and update data inside a functional component.

Example:

```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>
        Increase
      </button>
    </div>
  );
}
```

Here, `count` stores the current value and `setCount` is used to change it.

---

## Q36. What is the useEffect hook and what are its use cases?

`useEffect` is used to run code after a component renders.

It is commonly used for things like:

* Fetching data from an API
* Adding event listeners
* Working with timers
* Updating something outside React
* Running code when a value changes

Example:

```jsx
import { useEffect } from "react";

useEffect(() => {
  console.log("Component rendered");
}, []);
```

The empty array means the effect runs once when the component is mounted.

---

## Q37. What is the difference between controlled and uncontrolled components?

A **controlled component** is a form element whose value is controlled by React state.

Example:

```jsx
const [name, setName] = useState("");

<input
  value={name}
  onChange={(e) => setName(e.target.value)}
/>
```

An **uncontrolled component** stores its value in the DOM instead of React state. We can use `useRef` to get its value.

Controlled components are usually preferred when we need to control or validate form data.

---

## Q38. What are props in React and how are they passed?

Props are values passed from a parent component to a child component.

They are used to send data or functions to another component.

Example:

```jsx
function Welcome({ name }) {
  return <h1>Hello {name}</h1>;
}

function App() {
  return <Welcome name="John" />;
}
```

Here, `"John"` is passed as a prop to the `Welcome` component.

Props are read-only, so a child component should not directly change them.

---

## Q39. What is prop drilling and how can it be avoided?

Prop drilling happens when we pass props through several components just to send data to a component deep in the component tree.

For example:

```text
App
 ↓
Component A
 ↓
Component B
 ↓
Component C
```

If Component C needs some data from App, we may have to pass that data through A and B even though they don't need it.

Prop drilling can be avoided by using:

* Context API
* State management libraries
* Better component structure

For simple shared data, the Context API is often a good choice.

---

## Q40. Explain the useContext hook with an example.

`useContext` is used to access data from a React Context without passing props through every component.

Example:

```jsx
import { createContext, useContext } from "react";

const UserContext = createContext();

function App() {
  return (
    <UserContext.Provider value="John">
      <Profile />
    </UserContext.Provider>
  );
}

function Profile() {
  const user = useContext(UserContext);

  return <h1>Hello {user}</h1>;
}
```

Here, `Profile` can directly access the user value from `UserContext`.

It is useful for sharing things like user information, themes, or language settings.

---

## Q41. What is the useRef hook and when would you use it?

`useRef` is a Hook that lets us store a value that does not cause the component to re-render when it changes.

It is also commonly used to access a DOM element directly.

Example:

```jsx
import { useRef } from "react";

function Input() {
  const inputRef = useRef();

  const focusInput = () => {
    inputRef.current.focus();
  };

  return (
    <>
      <input ref={inputRef} />
      <button onClick={focusInput}>Focus</button>
    </>
  );
}
```

Here, `useRef` is used to access the input element and focus it.

---

## Q42. What are React keys and why are they important in lists?

Keys are unique values given to elements when rendering a list.

They help React identify which items have changed, been added, or been removed.

Example:

```jsx
const users = [
  { id: 1, name: "John" },
  { id: 2, name: "Mike" }
];

function Users() {
  return (
    <ul>
      {users.map((user) => (
        <li key={user.id}>{user.name}</li>
      ))}
    </ul>
  );
}
```

Using a unique key helps React update lists correctly and efficiently.

---

## Q43. What is the difference between state and props?

**Props** and **state** are both used to store data, but they have different purposes.

| Props                                 | State                        |
| ------------------------------------- | ---------------------------- |
| Passed from a parent component        | Managed inside a component   |
| Read-only                             | Can be changed               |
| Used to send data to child components | Used to manage changing data |
| Controlled by the parent              | Controlled by the component  |

Example:

```jsx
function User({ name }) {
  const [age, setAge] = useState(20);

  return (
    <p>
      {name} is {age} years old
    </p>
  );
}
```

Here, `name` is a prop and `age` is state.

---

## Q44. How does conditional rendering work in React?

Conditional rendering means showing different UI depending on a condition.

We can use normal JavaScript conditions such as `if`, the ternary operator, or `&&`.

Example using a ternary operator:

```jsx
function App({ isLoggedIn }) {
  return (
    <div>
      {isLoggedIn ? <h1>Welcome</h1> : <h1>Please Login</h1>}
    </div>
  );
}
```

If `isLoggedIn` is true, React shows "Welcome". Otherwise, it shows "Please Login".

---

## Q45. What is React.memo and when should you use it?

`React.memo` is used to prevent a component from re-rendering when its props have not changed.

Example:

```jsx
import React from "react";

const User = React.memo(function User({ name }) {
  return <h1>{name}</h1>;
});
```

React will skip rendering the component if its props are the same as before.

`React.memo` can improve performance, but it should not be used everywhere. It is mainly useful when a component renders often and its props usually stay the same.
### React Advanced Hooks & Routing (Q46 to Q60)

## Q46. What is the useReducer hook and when is it preferred over useState?

`useReducer` is a React hook used to manage state when the state logic is more complex.

It works with a **reducer function** and an **action**.

```jsx
const [state, dispatch] = useReducer(reducer, initialState);
```

I prefer `useReducer` when:

* There are multiple state values.
* State updates depend on previous state.
* There are different actions that can change the state.
* The state logic is becoming difficult to manage with `useState`.

For simple state like a boolean or input value, `useState` is usually easier.

### Follow-up questions

* What are `state` and `dispatch` in `useReducer`?
* What is a reducer function?
* Can we use `useState` and `useReducer` together?
* What is the difference between `useReducer` and Redux?

---

## Q47. Explain the useMemo hook and give a use case.

`useMemo` is used to remember the result of a calculation.

It helps avoid running an expensive calculation every time the component renders.

```jsx
const total = useMemo(() => {
  return calculateTotal(products);
}, [products]);
```

Here, `calculateTotal` only runs again when `products` changes.

A common use case is filtering or sorting a large list.

### Follow-up questions

* Does `useMemo` stop a component from re-rendering?
* What is the difference between `useMemo` and `useCallback`?
* Should we use `useMemo` everywhere?
* What happens if we don't use `useMemo`?

---

## Q48. What is the useCallback hook and when do you use it?

`useCallback` is used to remember a function between renders.

Normally, a new function is created every time the component renders.

```jsx
const handleClick = useCallback(() => {
  console.log("Clicked");
}, []);
```

It is mostly useful when passing a function to a child component that is optimized with `React.memo`.

### Follow-up questions

* What is the difference between `useCallback` and `useMemo`?
* When should you not use `useCallback`?
* Why does a function get recreated on every render?
* How does `React.memo` work with `useCallback`?

---

## Q49. What is React Router and how do you set up client-side routing?

React Router is a library used to handle navigation between pages in a React application without reloading the browser.

A basic setup looks like this:

```jsx
import { BrowserRouter, Routes, Route } from "react-router-dom";

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
      </Routes>
    </BrowserRouter>
  );
}
```

Now `/` shows the Home component and `/about` shows the About component.

### Follow-up questions

* What is client-side routing?
* What is `BrowserRouter`?
* What is the difference between `Route` and `Routes`?
* How do you create a dynamic route?
* How do you handle a 404 page?

---

## Q50. What is the difference between useNavigate and Link in React Router?

`Link` is mainly used when the user clicks something to navigate to another page.

```jsx
<Link to="/about">About</Link>
```

`useNavigate` is used when we want to navigate using JavaScript.

```jsx
const navigate = useNavigate();

navigate("/dashboard");
```

For example, after a successful login, we can use `useNavigate` to send the user to the dashboard.

### Follow-up questions

* When should you use `Link`?
* When should you use `useNavigate`?
* Can `Link` be used inside a button?
* How do you go back to the previous page?

---

## Q51. What are custom hooks in React? Write a simple example.

A custom hook is a JavaScript function that starts with `use` and lets us reuse React logic between components.

For example, we can create a hook for handling window width:

```jsx
import { useEffect, useState } from "react";

function useWindowWidth() {
  const [width, setWidth] = useState(window.innerWidth);

  useEffect(() => {
    const handleResize = () => setWidth(window.innerWidth);

    window.addEventListener("resize", handleResize);

    return () => {
      window.removeEventListener("resize", handleResize);
    };
  }, []);

  return width;
}
```

Then we can use it in any component:

```jsx
const width = useWindowWidth();
```

Custom hooks are useful when the same logic is needed in multiple components.

### Follow-up questions

* Why do custom hooks start with `use`?
* Can a custom hook use other hooks?
* Can a custom hook return an object?
* What is the difference between a custom hook and a normal function?

---

## Q52. What is lazy loading in React and how is it implemented?

Lazy loading means loading a component only when it is needed.

React provides `lazy()` for this.

```jsx
import { lazy, Suspense } from "react";

const About = lazy(() => import("./About"));

function App() {
  return (
    <Suspense fallback={<p>Loading...</p>}>
      <About />
    </Suspense>
  );
}
```

Instead of loading `About` when the whole application starts, React loads it when it is needed.

This can help reduce the initial bundle size.

### Follow-up questions

* What is `Suspense`?
* Why do we use `fallback`?
* What is the benefit of lazy loading?
* Can we lazy load routes?

---

## Q53. What are React error boundaries and why are they useful?

Error boundaries are used to catch JavaScript errors in a part of the React component tree.

If a component crashes, an error boundary can show a fallback UI instead of breaking the whole application.

Example idea:

```jsx
<ErrorBoundary>
  <Dashboard />
</ErrorBoundary>
```

They are useful for showing a friendly error message and preventing the entire UI from crashing.

Error boundaries are traditionally implemented with class components.

### Follow-up questions

* Can a functional component itself be an error boundary?
* What types of errors do error boundaries catch?
* What is fallback UI?
* Where should we use error boundaries?

---

## Q54. What is the Context API and when should you use Redux instead?

The Context API allows us to share data between components without passing props through every level.

For example, we can use Context for:

* Theme
* Logged-in user
* Language
* Simple global settings

Example:

```jsx
const ThemeContext = createContext();

<ThemeContext.Provider value="dark">
  <App />
</ThemeContext.Provider>
```

Redux is useful when the application has more complex global state and many parts of the application need to update or access that state.

I would normally start with local state or Context and use Redux when the application's state management becomes more complex.

### Follow-up questions

* What is prop drilling?
* How does Context solve prop drilling?
* Does Context replace Redux completely?
* What is a Redux store?
* When should you avoid Context?

---

## Q55. Explain the concept of reconciliation in React.

Reconciliation is the process React uses to figure out what changed in the UI.

When state or props change, React creates a new virtual representation of the UI and compares it with the previous one.

Then React updates only the necessary parts of the real DOM.

For example, if one item in a list changes, React does not need to rebuild the entire page.

Keys are also important during reconciliation because they help React identify list items.

```jsx
items.map(item => (
  <li key={item.id}>{item.name}</li>
));
```

### Follow-up questions

* What is the Virtual DOM?
* Why are keys important in React?
* What happens if we use array index as a key?
* Does React update the entire DOM after every state change?

---

## Q56. What is the difference between React.Fragment and empty tags (`<>`)?

Both are used to group multiple elements without adding an extra DOM element.

Using `Fragment`:

```jsx
<React.Fragment>
  <h1>Hello</h1>
  <p>Welcome</p>
</React.Fragment>
```

Using the short syntax:

```jsx
<>
  <h1>Hello</h1>
  <p>Welcome</p>
</>
```

They do almost the same thing.

The main difference is that the short syntax cannot accept props like `key`.

For example:

```jsx
<React.Fragment key={item.id}>
  ...
</React.Fragment>
```

### Follow-up questions

* Why would you use a Fragment?
* Does Fragment create a DOM element?
* Can we add a key to `<>`?
* When would you use `React.Fragment` instead of `<>`?

---

## Q57. How do you handle forms in React? Explain with Formik or react-hook-form.

There are two common ways to handle forms:

1. Controlled components using React state.
2. Form libraries such as Formik or react-hook-form.

With `react-hook-form`, a simple example is:

```jsx
import { useForm } from "react-hook-form";

function Login() {
  const {
    register,
    handleSubmit,
    formState: { errors }
  } = useForm();

  const onSubmit = (data) => {
    console.log(data);
  };

  return (
    <form onSubmit={handleSubmit(onSubmit)}>
      <input
        {...register("email", {
          required: "Email is required"
        })}
      />

      {errors.email && <p>{errors.email.message}</p>}

      <button type="submit">Login</button>
    </form>
  );
}
```

`react-hook-form` is useful because it makes form validation and form state easier to manage, especially for large forms.

### Follow-up questions

* What is a controlled component?
* What is an uncontrolled component?
* Why use react-hook-form?
* How do you validate a form?
* How do you handle errors in a form?

---

## Q58. What is code splitting in React and how does it improve performance?

Code splitting means splitting a large JavaScript bundle into smaller files.

Instead of downloading everything when the application starts, we can load some code only when it is needed.

React's `lazy()` is commonly used for this:

```jsx
const Dashboard = lazy(() => import("./Dashboard"));
```

This can make the initial page load faster because the browser doesn't need to download all the application code at once.

### Follow-up questions

* What is a JavaScript bundle?
* What is dynamic import?
* What is the difference between lazy loading and code splitting?
* How does code splitting improve initial load time?

---

## Q59. What are portals in React and when are they useful?

Portals allow us to render a React component into a different DOM node outside its normal parent.

Example:

```jsx
import { createPortal } from "react-dom";

function Modal() {
  return createPortal(
    <div className="modal">
      <h2>Hello</h2>
    </div>,
    document.getElementById("modal-root")
  );
}
```

Portals are commonly used for:

* Modals
* Dialog boxes
* Tooltips
* Dropdowns
* Notifications

They are useful when we don't want CSS like `overflow: hidden` or `z-index` from a parent element to cause problems.

### Follow-up questions

* Why are portals useful for modals?
* Does a portal still belong to the React component tree?
* Do events work normally with portals?
* Where should we create the portal root?

---

## Q60. Explain the lifecycle of a React functional component with hooks.

A functional component mainly goes through three stages:

### 1. Mounting

The component is created and added to the UI.

`useEffect` can run after the component is added to the screen.

```jsx
useEffect(() => {
  console.log("Component mounted");
}, []);
```

### 2. Updating

The component can re-render when its props or state change.

For example:

```jsx
const [count, setCount] = useState(0);
```

When `setCount` is called, the component renders again.

An effect can also run when specific values change:

```jsx
useEffect(() => {
  console.log("Count changed");
}, [count]);
```

### 3. Unmounting

The component is removed from the UI.

We can use the cleanup function inside `useEffect`:

```jsx
useEffect(() => {
  const timer = setInterval(() => {
    console.log("Running...");
  }, 1000);

  return () => {
    clearInterval(timer);
  };
}, []);
```

The cleanup function runs when the component is unmounted.

So, in simple terms:

**Mount → Update → Unmount**

### Follow-up questions

* When does `useEffect` run?
* What is the cleanup function in `useEffect`?
* What happens when the dependency array is empty?
* What happens when there is no dependency array?
* What causes a React component to re-render?
* Is there a lifecycle method in functional components?
* How is `useEffect` different from `componentDidMount`?
* How do you prevent memory leaks in a component?

---

# Quick Follow-up Questions

Here are some extra questions an interviewer may ask after these topics:

1. What is the difference between `useState` and `useReducer`?
2. What is the difference between `useMemo` and `useCallback`?
3. Why should we not optimize everything with `useMemo`?
4. What causes a React component to re-render?
5. What is prop drilling?
6. What is the Virtual DOM?
7. Why are keys important in React lists?
8. What is the difference between controlled and uncontrolled components?
9. What is the difference between Context API and Redux?
10. What is lazy loading?
11. What is code splitting?
12. What is `Suspense`?
13. What is an error boundary?
14. What is a custom hook?
15. Can hooks be called inside loops or conditions?
16. What are the Rules of Hooks?
17. What is the difference between `Link` and `useNavigate`?
18. What is client-side routing?
19. What are React portals?
20. What happens when a component unmounts?

## ▲ Next.js Interview Questions & Answers

A collection of common **Next.js interview questions**, with simple answers, real-world examples, and follow-up questions.

---

### Q1. What is Next.js?

Next.js is a production-ready React framework used to build modern full-stack web applications.

It provides features out of the box:
* **File-based routing** (App Router & Pages Router)
* **Server Components & Client Components**
* **Multiple rendering strategies:** SSR, SSG, ISR, Client-side
* **API Route Handlers & Server Actions**
* **Image, Font, and Script Optimization**
* **Built-in SEO & Metadata support**
* **Multi-level Caching & Edge Middleware**

#### Real-world example:
When building an e-commerce platform, Next.js handles:
* Product catalog pages (statically generated / cached)
* User account & checkout (server-side rendered / authenticated)
* Search & interactive filters (client components)
* Payment and cart actions (Server Actions / API routes)
* SEO & OpenGraph tags for search engines and social previews

#### Follow-up: Why use Next.js instead of plain React?
React is a UI library focused on components and view rendering. Next.js is a full framework built around React that provides everything needed for a complete web application (routing, data fetching, server rendering, bundling, API endpoints, and production optimization).

---

### Q2. What is the difference between React and Next.js?

| Feature | React | Next.js |
|---|---|---|
| **Type** | UI Library | Full-Stack Framework |
| **Routing** | Requires external library (`react-router-dom`) | Built-in file-system based routing (`app/` or `pages/`) |
| **Rendering** | Client-Side Rendering (CSR) by default | Server Components, SSR, SSG, ISR, CSR |
| **SEO** | Harder for crawlers without pre-rendering | Excellent built-in SEO and server-rendered HTML |
| **Backend / API** | Requires separate backend (Node/Express) | Built-in API routes (`route.js`) & Server Actions |
| **Performance** | Downloads large JS bundle before UI renders | Automatic code-splitting, streaming, and image optimization |

```text
React:
 ├── Components
 ├── Hooks
 └── Client UI

Next.js:
 ├── React
 ├── File-based Routing
 ├── React Server Components (RSC)
 ├── SSR / SSG / ISR
 ├── Server Actions & API Routes
 └── Built-in SEO & Image Optimization
```

---

### Q3. What is App Router?

App Router is the modern routing system introduced in Next.js 13+, built around the `app/` directory and React Server Components.

#### Directory Structure Example:
```text
app/
├── layout.js       # Root layout shared by all pages
├── page.js         # Homepage route (/)
├── about/
│   └── page.js     # Route: /about
└── products/
    ├── page.js     # Route: /products
    └── [id]/
        └── page.js # Dynamic route: /products/:id
```

#### Key features supported by App Router:
* **Server Components by default**
* **Nested layouts and templates**
* **Special file conventions:** `loading.js`, `error.js`, `not-found.js`, `route.js`
* **Server Actions** directly inside components
* **Streaming with React Suspense**

---

### Q4. What is a Server Component?

A **React Server Component (RSC)** executes and renders only on the server. Its code and dependencies never get sent to the browser.

In Next.js App Router, **all components inside `app/` are Server Components by default**.

#### Example:
```jsx
export default async function ProductsPage() {
  // Directly fetch data on the server without useEffect!
  const response = await fetch("https://api.example.com/products");
  const products = await response.json();

  return (
    <div>
      <h1>Product Catalog</h1>
      {products.map((product) => (
        <p key={product.id}>{product.name} - ${product.price}</p>
      ))}
    </div>
  );
}
```

#### Benefits:
* **Zero Client-Side JavaScript:** Reduces bundle size significantly.
* **Direct Backend Access:** Can query databases directly without exposing connection strings.
* **SEO Friendly:** Pre-renders complete HTML for search engines.

---

### Q5. What is a Client Component?

A Client Component is rendered on the client browser and has access to browser APIs, user events, and React client hooks (`useState`, `useEffect`).

You define a Client Component by adding the **`"use client"`** directive at the top of the file.

#### Example:
```jsx
"use client";

import { useState } from "react";

export default function Counter() {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + 1)}>
      Count: {count}
    </button>
  );
}
```

#### Best Practice Pattern:
Keep pages as Server Components, and push Client Components down to the smallest interactive leaves (e.g., an `AddToCartButton`).

---

### Q6. What is `"use client"`?

`"use client"` is a directive that marks the boundary between the server-only component graph and the client component graph.

* Must be placed at the very top of the file, before any imports.
* It tells Next.js to package this component and its child imports into the client JavaScript bundle.
* Use it only when you need: `useState`, `useEffect`, browser APIs (`localStorage`, `window`), or event handlers (`onClick`, `onChange`).

---

### Q7. What is Server-Side Rendering (SSR)?

**Server-Side Rendering (SSR)** generates the HTML dynamically on the server for **every incoming user request**.

```text
User requests page ──> Server fetches latest data ──> Generates HTML ──> Browser displays HTML
```

#### When to use SSR:
* Personalized user dashboards
* Pages showing real-time live stock/pricing data
* Pages dependent on incoming request headers or user authentication cookies

---

### Q8. What is SSG (Static Site Generation)?

**Static Site Generation (SSG)** generates the HTML pages at build time. The same pre-rendered HTML is stored on a CDN and served instantly to all users.

#### When to use SSG:
* Marketing pages, landing pages
* Blogs, portfolio sites
* Documentation websites
* Content that rarely changes

---

### Q9. What is ISR (Incremental Static Regeneration)?

**ISR** allows you to update static pages in the background after the site is deployed, without rebuilding the whole website.

```jsx
// Revalidate this page at most once every 60 seconds
const response = await fetch("https://api.example.com/products", {
  next: { revalidate: 60 }
});
```

#### Comparison: SSR vs SSG vs ISR

| Strategy | When is HTML generated? | Best Use Case | Performance |
|---|---|---|---|
| **SSG** | Build time | Documentation, landing pages | ⚡ Fastest (served from CDN) |
| **SSR** | Every request | User dashboards, dynamic auth pages | Dependent on server/database latency |
| **ISR** | Build time + periodically in background | E-commerce product catalogs, blog lists | ⚡ Fast with automatic freshness |

---

### Q10. What is Dynamic Routing?

Dynamic routes allow capturing variable parameters in URLs by using square brackets `[param]` in folder names.

#### Example:
```text
app/products/[id]/page.js  ==>  matches /products/10, /products/25
```

```jsx
export default async function ProductPage({ params }) {
  const { id } = await params;
  return <h1>Product Details for ID: {id}</h1>;
}
```

---

### Q11. What is `layout.js`?

A layout is UI that is **shared between multiple pages**. On navigation, layouts preserve state, remain interactive, and do not re-render.

```text
app/
├── layout.js       # Root layout with <html> and <body>
├── page.js
└── dashboard/
    ├── layout.js   # Dashboard sidebar/navigation layout
    └── page.js
```

---

### Q12. What is Middleware in Next.js?

Next.js Middleware runs **before a request is completed**, allowing you to modify requests and responses based on incoming URL, headers, and cookies.

```javascript
// middleware.js (in project root or src/)
import { NextResponse } from 'next/server';

export function middleware(request) {
  const token = request.cookies.get('token');

  if (!token && request.nextUrl.pathname.startsWith('/dashboard')) {
    return NextResponse.redirect(new URL('/login', request.url));
  }

  return NextResponse.next();
}
```

#### Common use cases:
* Authentication and role-based route protection
* Bot detection and rate limiting
* Internationalization / localization redirects
* Adding security headers

---

### Q13. How do you protect a route in Next.js?

1. **Middleware Check:** Check for auth cookies or JWT tokens and redirect unauthenticated users before rendering.
2. **Server-Side Validation:** Check session directly in Server Components or layout before serving sensitive data.
3. **API & Server Action Protection:** Always verify the caller's session on every server-side mutation.

---

### Q14. What is Authentication vs Authorization?

* **Authentication (AuthN):** "Who are you?" (verifying email/password, OAuth provider).
* **Authorization (AuthZ):** "What are you allowed to do?" (checking if user has `role === 'admin'` to delete a record).

---

### Q15. How do you create an API route in Next.js App Router?

Create a **`route.js`** file inside the `app/api/` directory exporting standard HTTP methods (`GET`, `POST`, `PUT`, `DELETE`, `PATCH`).

```javascript
// app/api/users/route.js
export async function GET(request) {
  const users = [{ id: 1, name: "Nahiya" }];
  return Response.json(users, { status: 200 });
}

export async function POST(request) {
  const body = await request.json();
  // save user to DB
  return Response.json({ success: true, user: body }, { status: 201 });
}
```

---

### Q16. What are Server Actions?

**Server Actions** are asynchronous functions that are executed on the server. They can be invoked directly from forms and buttons in both Server and Client Components.

```jsx
// Server Action definition
async function createPost(formData) {
  'use server';
  const title = formData.get('title');
  await db.post.create({ data: { title } });
}

export default function NewPostForm() {
  return (
    <form action={createPost}>
      <input name="title" placeholder="Title" required />
      <button type="submit">Create Post</button>
    </form>
  );
}
```

#### Benefits:
* Eliminates boilerplate API endpoints for mutations.
* Progressive enhancement: works even before client JavaScript loads.

---

### Q17. How do you fetch data in Next.js App Router?

Directly in Server Components using native `fetch`, OR via direct database ORM calls (Prisma, Drizzle, Mongoose):

```jsx
export default async function UserList() {
  const users = await db.user.findMany(); // Direct database query!
  return (
    <ul>
      {users.map(u => <li key={u.id}>{u.name}</li>)}
    </ul>
  );
}
```

---

### Q18. What is Caching in Next.js?

Next.js employs a comprehensive caching architecture:
1. **Request Memoization:** De-duplicates identical `fetch` requests within the same render pass.
2. **Data Cache:** Persists `fetch` responses across incoming requests and deployments.
3. **Full Route Cache:** Stores static HTML and RSC payloads on the server.
4. **Router Cache:** Client-side cache that stores visited route segments in browser memory.

---

### Q19. What is the `<Image />` component in Next.js?

The `next/image` component extends the HTML `<img>` element with automatic optimization:
* **Modern formats:** Serves WebP and AVIF automatically.
* **Responsive sizing:** Automatically generates responsive `srcset`.
* **Zero layout shift:** Prevents Cumulative Layout Shift (CLS).
* **Lazy loading:** Defers offscreen image loading until in viewport.

```jsx
import Image from "next/image";

<Image
  src="/profile.png"
  width={300}
  height={300}
  alt="Profile picture"
  priority // loads immediately if above the fold
/>
```

---

### Q20. How do you handle SEO in Next.js?

Next.js provides a built-in Metadata API to define page titles, descriptions, OpenGraph, and Twitter cards:

```jsx
// Static metadata
export const metadata = {
  title: "Products | My Store",
  description: "Browse our exclusive product catalog"
};

// Dynamic metadata
export async function generateMetadata({ params }) {
  const { id } = await params;
  const product = await getProduct(id);
  return {
    title: product.name,
    description: product.description,
    openGraph: { images: [product.imageUrl] }
  };
}
```

---

### Q21. What are Environment Variables in Next.js?

Next.js has built-in support for `.env.local`:
* **Server-Only (Secret):** Without prefix, accessible only in Server Components / API routes (`process.env.DATABASE_URL`).
* **Browser-Accessible (Public):** Must be prefixed with `NEXT_PUBLIC_` (`process.env.NEXT_PUBLIC_STRIPE_KEY`).

---

### Q22. What is Hydration?

Hydration is the process where React in the browser attaches event listeners and state management to the pre-rendered static HTML sent by the server.

#### Hydration Errors:
Occurs when the client-rendered output differs from the server-rendered HTML (e.g., displaying `new Date().toLocaleTimeString()` or `window.innerWidth` directly).

---

### Q23. How do you handle loading states in Next.js?

Create a **`loading.js`** file in the route folder. Next.js automatically wraps the page in a React `<Suspense>` boundary:

```jsx
// app/dashboard/loading.js
export default function Loading() {
  return <div className="skeleton-loader">Loading dashboard...</div>;
}
```

---

### Q24. How do you handle errors in Next.js?

Create an **`error.js`** file in the route segment. It must be a **Client Component**:

```jsx
// app/products/error.js
'use client';

export default function Error({ error, reset }) {
  return (
    <div>
      <h2>Something went wrong!</h2>
      <p>{error.message}</p>
      <button onClick={() => reset()}>Try again</button>
    </div>
  );
}
```

For 404 pages, use **`not-found.js`** and invoke the `notFound()` function from `next/navigation`.

---

### Q25. How do you optimize Next.js performance?

1. Use **Server Components** for non-interactive pages to minimize client JS bundle.
2. Use **`next/image`** for all raster graphics and **`next/font`** to eliminate layout shifts.
3. Apply **Dynamic Imports (`next/dynamic`)** for heavy libraries (charts, rich text editors).
4. Utilize **Route Handlers and ISR/revalidation** instead of re-fetching on every request.
5. Analyze bundles using `@next/bundle-analyzer`.

---

### Q26. What is Dynamic Import (`next/dynamic`)?

Dynamic import enables code-splitting by loading components lazily only when needed.

```jsx
import dynamic from 'next/dynamic';

const HeavyChart = dynamic(() => import('@/components/HeavyChart'), {
  ssr: false, // disable server-side rendering for browser-only canvas
  loading: () => <p>Loading chart...</p>
});
```

---

### Q27. How would you implement authentication in a Next.js project?

1. **Credentials verification:** Verify login email/password via a Server Action or Route Handler.
2. **Session creation:** Issue a cryptographic JWT or session token stored in an `httpOnly`, `secure`, `SameSite=Lax` cookie.
3. **Route protection:** Middleware inspects the cookie and redirects unauthenticated requests.
4. **Server Component validation:** Secure layouts extract and verify the user session.
5. **Popular libraries:** NextAuth.js (Auth.js), Lucia Auth, or Clerk.

---

### Q28. How do you handle a 404 page?

```jsx
// app/not-found.js
import Link from 'next/link';

export default function NotFound() {
  return (
    <div>
      <h2>Page Not Found</h2>
      <p>Could not find the requested resource.</p>
      <Link href="/">Return Home</Link>
    </div>
  );
}
```

---

### Q29. How would you structure a large Next.js project?

```text
my-app/
├── app/                  # App Router: routes, layouts, pages, loading, error
│   ├── (auth)/           # Route groups (clean URLs without path prefix)
│   │   ├── login/page.js
│   │   └── register/page.js
│   ├── dashboard/page.js
│   ├── api/              # API Route handlers
│   ├── layout.js
│   └── page.js
├── components/           # Reusable UI components
│   ├── ui/               # Buttons, Inputs, Dialogs (shadcn/radix)
│   └── forms/            # Complex forms
├── lib/                  # Utilities, DB clients, auth helpers
├── hooks/                # Custom React client hooks
├── services/             # Backend business logic & API services
├── types/                # TypeScript definitions
└── middleware.js         # Edge middleware
```

---

### Q30. Why choose Next.js for a production project?

> "I choose Next.js because it provides a complete, modern full-stack architecture with production optimizations built-in: React Server Components to keep client bundles tiny, flexible rendering (SSR, SSG, ISR), built-in file-based routing and Edge middleware, Server Actions for simple type-safe data mutations, and automatic image/font/SEO optimization."

---

## 🟢 Node.js Interview Questions & Answers

Simple English + real-world examples for interviews.

---

## 1. Explain the Node.js event loop architecture in detail.

Node.js uses an **event loop** to handle many requests without waiting for every operation to finish.

For example, if Node.js needs to read a file, it starts the file operation and continues doing other work. When the file is ready, Node.js runs the callback.

```js
const fs = require("fs");

console.log("Start");

fs.readFile("data.txt", "utf8", (err, data) => {
  console.log("File read");
});

console.log("End");
```

Output:

```text
Start
End
File read
```

The basic flow is:

```text
JavaScript
    ↓
Node.js
    ↓
libuv
    ↓
OS / Thread Pool
    ↓
Operation finishes
    ↓
Callback Queue
    ↓
Event Loop
    ↓
Callback runs
```

The event loop has different phases, such as timers, poll, check, and close callbacks.

**Simple interview answer:**

> The Node.js event loop allows Node.js to handle asynchronous operations without blocking the main JavaScript thread. When an async operation finishes, its callback is picked up by the event loop and executed.

---

## 2. What is the difference between process.nextTick(), setImmediate(), and setTimeout()?

All three are used to run code later, but their timing is different.

### process.nextTick()

Runs very soon after the current operation.

```js
process.nextTick(() => {
  console.log("nextTick");
});
```

### setImmediate()

Runs during the event loop's check phase.

```js
setImmediate(() => {
  console.log("Immediate");
});
```

### setTimeout()

Runs after the specified delay.

```js
setTimeout(() => {
  console.log("Timeout");
}, 0);
```

`setTimeout(..., 0)` does not mean exactly 0 milliseconds. It means the callback can run after the timer is ready.

**Easy way to remember:**

```text
process.nextTick()
      ↓
event loop continues
      ↓
setImmediate / setTimeout
```

The exact order between `setImmediate()` and `setTimeout(..., 0)` can depend on where they are called.

---

## 3. How does Node.js handle asynchronous operations internally?

When Node.js gets an asynchronous operation, it does not sit and wait for it.

For example:

```js
fs.readFile("users.json", callback);
```

Node.js gives the operation to the operating system or libuv.

The basic flow is:

```text
Node.js
   ↓
libuv
   ↓
OS / Thread Pool
   ↓
Operation completes
   ↓
Callback is queued
   ↓
Event Loop
   ↓
Callback executes
```

While the file is being read, Node.js can handle other requests.

This is why Node.js is good for applications with lots of I/O operations.

Examples:

* Database requests
* File operations
* HTTP requests
* Network operations

---

## 4. Explain the role of libuv in Node.js.

**libuv** is an important library used by Node.js.

It provides the event loop and helps Node.js handle asynchronous operations.

For example:

```js
fs.readFile("test.txt", callback);
```

libuv helps manage this asynchronous work.

It also has a thread pool for some operations that cannot be handled directly with non-blocking OS APIs.

Examples include:

* File system operations
* Some DNS operations
* Crypto operations
* Compression

**Interview answer:**

> libuv is the library behind Node.js that provides the event loop and asynchronous I/O infrastructure. It also uses a thread pool for some operations that could otherwise block the main thread.

---

## 5. What are streams in Node.js? Explain different stream types.

Streams allow us to process data **in small chunks** instead of loading the complete data into memory.

There are four main types.

### 1. Readable

Used to read data.

```js
const fs = require("fs");

const stream = fs.createReadStream("video.mp4");
```

### 2. Writable

Used to write data.

```js
const stream = fs.createWriteStream("output.txt");
```

### 3. Duplex

Can read and write data.

A TCP socket is an example.

### 4. Transform

Can modify data while it passes through the stream.

```text
Input
  ↓
Transform
  ↓
Output
```

### Real-world example

Suppose a user downloads a 5 GB video.

We don't want to load the whole 5 GB into RAM.

Instead:

```text
Video File
   ↓
Stream
   ↓
Network
   ↓
User
```

The video is sent in chunks.

---

## 6. How would you handle large file uploads efficiently in Node.js?

I would use **streams** instead of loading the complete file into memory.

For example, if a user uploads a 2 GB file, putting the whole file into RAM can cause memory problems.

A better approach is:

```text
Client
  ↓
Upload Stream
  ↓
Validation
  ↓
Storage
```

In a real project, I would also add:

* Maximum file size
* File type validation
* Authentication
* Virus scanning
* Proper error handling
* Cloud/object storage

For example, the file could be streamed directly to object storage instead of being completely stored in the Node.js server's memory.

**Interview answer:**

> For large uploads, I would use streams so the file is processed in chunks instead of loading the whole file into memory.

---

## 7. What is backpressure in streams and how do you solve it?

Backpressure happens when the producer sends data faster than the consumer can process it.

For example:

```text
Fast File Reader
       ↓↓↓↓↓↓↓
Slow Network
```

The reader produces data quickly, but the network cannot handle it that fast.

This can cause memory usage to increase.

Node.js streams provide backpressure handling.

A common solution is:

```js
readable.pipe(writable);
```

Example:

```js
const fs = require("fs");

const readStream = fs.createReadStream("large.mp4");
const writeStream = fs.createWriteStream("copy.mp4");

readStream.pipe(writeStream);
```

`pipe()` manages the data flow between the streams.

**Interview answer:**

> Backpressure happens when the writable side is slower than the readable side. Node.js streams handle this by controlling the flow of data so memory does not keep increasing.

---

## 8. Explain clustering in Node.js. When should you use it?

Normally, Node.js runs JavaScript on one main thread.

But a server can have multiple CPU cores.

The **cluster module** allows us to run multiple Node.js processes.

For example:

```text
CPU 1 → Node Process
CPU 2 → Node Process
CPU 3 → Node Process
CPU 4 → Node Process
```

Each process has its own memory.

### When can we use it?

It can be useful when:

* The application has high traffic.
* We want to use multiple CPU cores.
* We want multiple Node.js server processes.

**Simple interview answer:**

> Clustering allows us to run multiple Node.js processes so we can use multiple CPU cores and handle more traffic.

---

## 9. Difference between worker threads and cluster module?

The main difference is:

```text
Cluster       → Multiple processes
Worker Thread → Multiple threads
```

### Cluster

Cluster creates separate Node.js processes.

```text
Process 1
Process 2
Process 3
```

Each process has its own memory.

### Worker Threads

Worker threads run JavaScript work in separate threads within the same Node.js process.

They are useful for CPU-heavy tasks.

Examples:

* Image processing
* Large calculations
* Data processing
* CPU-heavy encryption

**Interview answer:**

> Cluster is mainly used to run multiple Node.js processes, while worker threads are used to run CPU-heavy JavaScript work in separate threads.

---

## 10. How does Node.js achieve non-blocking I/O?

Node.js does not wait for I/O operations to finish.

Example:

```js
const fs = require("fs");

fs.readFile("users.json", () => {
  console.log("File finished");
});

console.log("Continue");
```

Output:

```text
Continue
File finished
```

Node starts the file operation and continues with other work.

The basic idea is:

```text
Start I/O
   ↓
Node continues other work
   ↓
I/O finishes
   ↓
Callback executes
```

This is called **non-blocking I/O**.

It is one of the main reasons Node.js works well for applications with many network connections.

---

## 11. Explain CommonJS vs ES Modules in Node.js.

Node.js supports two major module systems.

### CommonJS

CommonJS is commonly seen in older Node.js projects.

```js
const express = require("express");

module.exports = myFunction;
```

It uses:

```js
require()
module.exports
```

### ES Modules

ES Modules use the standard JavaScript `import` and `export` syntax.

```js
import express from "express";

export default myFunction;
```

It uses:

```js
import
export
```

### Comparison

| CommonJS                   | ES Modules                 |
| -------------------------- | -------------------------- |
| `require()`                | `import`                   |
| `module.exports`           | `export`                   |
| Older/common Node.js style | Modern JavaScript standard |

**Interview answer:**

> CommonJS uses require and module.exports, while ES Modules use import and export. Node.js supports both.

---

## 12. What are memory leaks in Node.js and how do you debug them?

A memory leak happens when the application keeps objects in memory even though they are no longer needed.

Example:

```js
const users = [];

setInterval(() => {
  users.push({
    name: "John",
    time: Date.now()
  });
}, 1000);
```

Every second, a new object is added.

The array keeps growing, so memory usage can keep increasing.

### Common causes

* Global variables
* Unlimited caches
* Timers that are never cleared
* Event listeners that are never removed
* Keeping large objects unnecessarily

### How to debug

I would check:

* Memory usage
* Heap snapshots
* Garbage collection
* Large objects
* Event listeners
* Caches

Node.js also provides:

```js
console.log(process.memoryUsage());
```

For a real production problem, I would use heap snapshots and profiling tools to find what is staying in memory.

---

## 13. How would you optimize a slow Node.js application?

First, I would not randomly change code.

I would find the actual bottleneck.

I would check:

1. CPU usage
2. Memory usage
3. Database queries
4. API response time
5. Event loop blocking
6. Network calls
7. External services

For example:

```text
Node.js code     → 100 ms
Database query   → 2.5 sec
External API     → 400 ms
```

Here the database is the main problem.

Changing Node.js code won't solve the biggest issue.

### Things I might do

* Optimize database queries
* Add database indexes
* Add caching
* Use pagination
* Use connection pooling
* Use streams for large data
* Use worker threads for CPU-heavy tasks
* Remove unnecessary API calls
* Avoid synchronous operations

My approach would be:

```text
Measure
   ↓
Find bottleneck
   ↓
Fix it
   ↓
Measure again
```

**Interview answer:**

> I would first measure the application and find the bottleneck. Then I would optimize the database, Node.js code, network calls, or memory depending on where the actual problem is.

---

## 14. Explain Event Emitters with practical use cases.

An EventEmitter allows one part of the application to **emit an event** and another part to listen for it.

Example:

```js
const EventEmitter = require("events");

const emitter = new EventEmitter();

emitter.on("userRegistered", (user) => {
  console.log("Send welcome email to:", user.email);
});

emitter.emit("userRegistered", {
  email: "john@example.com"
});
```

Here:

```text
User registers
      ↓
userRegistered event
      ↓
Email listener
      ↓
Send welcome email
```

### Real-world examples

Event emitters can be used for:

* User registration
* Order creation
* Payment completion
* Notifications
* Logging
* Internal application events

Node.js itself uses events in many APIs.

For example, streams can emit:

```js
data
error
end
close
```

**Interview answer:**

> EventEmitter allows different parts of an application to communicate using events. One part emits an event and another part listens for it.

---

# 15. What happens internally when you run npm install?

Suppose we have this `package.json`:

```json
{
  "dependencies": {
    "express": "^5.1.0"
  }
}
```

Then we run:

```bash
npm install
```

### Step 1: npm reads package.json

npm checks which packages the project needs.

```text
package.json
     ↓
express
```

### Step 2: npm checks package-lock.json

If `package-lock.json` exists, npm uses it to help determine the dependency tree and resolved versions.

This makes installs more consistent.

### Step 3: npm resolves dependencies

Express has its own dependencies.

So npm creates a dependency tree.

```text
my-app
 └── express
      ├── dependency A
      ├── dependency B
      └── dependency C
```

Those dependencies can also have their own dependencies.

### Step 4: npm downloads packages

npm downloads the required packages from the configured npm registry.

They are installed into:

```text
node_modules/
```

After installation:

```text
project/
├── package.json
├── package-lock.json
├── node_modules/
└── src/
```

### Step 5: npm runs lifecycle scripts

Some packages have installation scripts.

For example, a package may need to compile native code or perform some setup.

### Step 6: npm updates package-lock.json

If the dependency tree changes, npm can update the lock file.

---

## Real-world npm install example

Imagine I join a company and get a Node.js project from GitHub.

I clone it:

```bash
git clone company-project
cd company-project
```

I see:

```text
package.json
package-lock.json
src/
```

There is no `node_modules` folder because it normally isn't committed to Git.

I run:

```bash
npm install
```

npm basically does this:

```text
Read package.json
       ↓
Check package-lock.json
       ↓
Resolve dependencies
       ↓
Download packages
       ↓
Install into node_modules
       ↓
Run required scripts
```

After that, I can run:

```bash
npm run dev
```

and start the application.

---

## npm install vs npm ci

### npm install

Usually used during development.

```bash
npm install
```

It can install dependencies and update the lock file when needed.

### npm ci

Commonly used in CI/CD pipelines.

```bash
npm ci
```

It installs from the lock file and is designed for clean, reproducible installs.

For example, a GitHub Actions workflow might use:

```yaml
- name: Install dependencies
  run: npm ci
```

---

# Quick Revision

| Topic                | Easy Meaning                                 |
| -------------------- | -------------------------------------------- |
| Event Loop           | Handles async work                           |
| `process.nextTick()` | Runs very soon after current operation       |
| `setImmediate()`     | Runs in check phase                          |
| `setTimeout()`       | Runs after timer delay                       |
| libuv                | Provides event loop and async infrastructure |
| Streams              | Process data in chunks                       |
| Backpressure         | Producer is faster than consumer             |
| Cluster              | Multiple Node.js processes                   |
| Worker Threads       | Separate threads for CPU-heavy work          |
| Non-blocking I/O     | Node doesn't wait for I/O                    |
| CommonJS             | `require()` / `module.exports`               |
| ES Modules           | `import` / `export`                          |
| Memory Leak          | Unwanted objects stay in memory              |
| EventEmitter         | Communicate using events                     |
| `npm install`        | Resolves and installs dependencies           |

---
## 🚂 Express.js Interview Questions

Simple English answers with real-world examples for Express.js interviews.

---

## 1. Explain the Express.js Request-Response Lifecycle

When a client sends a request to an Express.js server, the request goes through middleware and then reaches the correct route.

The basic flow is:

```text
Client
  ↓
Request
  ↓
Middleware
  ↓
Authentication / Validation
  ↓
Route
  ↓
Controller
  ↓
Database
  ↓
Response
  ↓
Client
```

### Example

```js
app.get('/users', (req, res) => {
  res.json({
    message: 'Users fetched successfully'
  });
});
```

When the client sends:

```text
GET /users
```

Express finds the `/users` route and sends the response.

### Real-world example

Imagine an online shopping website.

When you open your orders:

1. Request comes from the browser.
2. Middleware checks the request.
3. Authentication checks if you are logged in.
4. Route receives the request.
5. Controller gets orders from the database.
6. Server sends the orders back to the browser.

---

# 2. What is Middleware in Express.js?

Middleware is a function that runs between the request and the response.

It can be used for:

* Authentication
* Logging
* Validation
* Error handling
* Checking permissions
* Modifying request data

### Example

```js
const logger = (req, res, next) => {
  console.log(req.method, req.url);
  next();
};

app.use(logger);
```

Here, `next()` tells Express to continue to the next middleware or route.

### Real-world example

Think about entering an office.

A security guard checks your ID before allowing you inside.

The security guard is like middleware.

```text
Visitor
   ↓
Security Guard
   ↓
Office
```

---

# 3. Difference Between Application-Level, Router-Level, and Error-Handling Middleware

## Application-Level Middleware

Application-level middleware is added to the main Express application.

```js
app.use((req, res, next) => {
  console.log('Request received');
  next();
});
```

It can work for many routes.

---

## Router-Level Middleware

Router-level middleware is attached to a specific router.

```js
const express = require('express');

const router = express.Router();

router.use(authMiddleware);

router.get('/profile', getProfile);

module.exports = router;
```

Here, `authMiddleware` is mainly used for routes inside this router.

---

## Error-Handling Middleware

Error-handling middleware handles errors in one common place.

It has four parameters:

```js
app.use((err, req, res, next) => {
  res.status(500).json({
    message: err.message
  });
});
```

### Simple way to remember

```text
Application middleware → Whole application

Router middleware → Specific router

Error middleware → Handles errors
```

---

# 4. How Does `next()` Work?

`next()` tells Express to continue to the next middleware.

### Example

```js
app.use((req, res, next) => {
  console.log('Middleware 1');
  next();
});

app.use((req, res, next) => {
  console.log('Middleware 2');
  next();
});
```

Output:

```text
Middleware 1
Middleware 2
```

If we don't call `next()` and don't send a response, the request may keep waiting.

### `next(error)`

We can pass an error to Express:

```js
next(error);
```

Then Express sends the error to error-handling middleware.

### Real-world example

Think of a production line.

```text
Worker 1
   ↓
Worker 2
   ↓
Worker 3
   ↓
Finished Product
```

`next()` means:

> "My work is finished. Send it to the next worker."

---

# 5. How Would You Structure a Scalable Express.js Project?

For a small project, we can keep everything in a few files.

For a large project, I would separate the code.

### Example structure

```text
project/
│
├── src/
│   ├── routes/
│   │   ├── userRoutes.js
│   │   ├── productRoutes.js
│   │   └── orderRoutes.js
│   │
│   ├── controllers/
│   │   ├── userController.js
│   │   ├── productController.js
│   │   └── orderController.js
│   │
│   ├── services/
│   │
│   ├── models/
│   │
│   ├── middleware/
│   │
│   ├── validators/
│   │
│   ├── config/
│   │
│   └── app.js
│
└── server.js
```

### What each folder does

```text
routes       → Defines API routes

controllers  → Handles requests and responses

services     → Business logic

models       → Database models

middleware   → Authentication, validation, etc.

validators   → Checks incoming data

config       → Database and application configuration
```

### Real-world example

For an e-commerce application, I would keep:

```text
users
products
orders
payments
```

separate instead of putting everything into one huge file.

This makes the project easier to maintain.

---

# 6. Explain REST API Best Practices in Express.js

REST API means creating APIs using standard HTTP methods and clear URLs.

### Common HTTP methods

```text
GET     → Get data
POST    → Create data
PUT     → Update data
PATCH   → Partially update data
DELETE  → Delete data
```

### Example

```text
GET    /users
POST   /users
GET    /users/10
PUT    /users/10
DELETE /users/10
```

### Use proper status codes

```text
200 → Success

201 → Created

400 → Bad Request

401 → Not Authenticated

403 → Not Allowed

404 → Not Found

500 → Server Error
```

### Example

```js
app.post('/users', (req, res) => {
  res.status(201).json({
    message: 'User created successfully'
  });
});
```

### Other good practices

* Validate input
* Use authentication
* Use authorization
* Handle errors properly
* Use consistent response formats
* Don't expose sensitive information
* Use pagination for large data
* Use meaningful API URLs

---

# 7. How Do You Implement Centralized Error Handling?

Centralized error handling means handling application errors in one place.

Instead of writing different error responses in every route, we create one error middleware.

### Example

```js
app.get('/users/:id', async (req, res, next) => {
  try {
    const user = await getUser(req.params.id);

    if (!user) {
      const error = new Error('User not found');
      error.statusCode = 404;
      throw error;
    }

    res.json(user);
  } catch (error) {
    next(error);
  }
});
```

Then at the end of the application:

```js
app.use((err, req, res, next) => {
  const statusCode = err.statusCode || 500;

  res.status(statusCode).json({
    success: false,
    message: err.message || 'Internal Server Error'
  });
});
```

### Why is this useful?

It keeps error responses consistent.

### Real-world example

Suppose the database is down.

Instead of every API showing a different error message, the centralized error handler can return a common response.

```json
{
  "success": false,
  "message": "Database connection failed"
}
```

---

# 8. How Do You Validate Incoming Request Data?

Validation means checking whether the data sent by the client is correct before using it.

For example, during registration:

```text
email → Required and valid

password → Required and strong enough

name → Required
```

### Simple example

```js
app.post('/register', (req, res) => {
  const { email, password } = req.body;

  if (!email) {
    return res.status(400).json({
      message: 'Email is required'
    });
  }

  if (!password) {
    return res.status(400).json({
      message: 'Password is required'
    });
  }

  res.json({
    message: 'Validation successful'
  });
});
```

For bigger projects, I would use a validation library such as Joi, Zod, or express-validator.

### Real-world example

If a user creates an account without an email address, we should not send that data directly to the database.

We validate it first.

```text
Request
   ↓
Validation
   ↓
Valid?
 ┌─┴─┐
Yes  No
 ↓    ↓
DB   Error
```

---

# 9. Explain Route Modularization in Express.js

Route modularization means putting different routes into different files.

Instead of having this:

```text
app.js
  ↓
1000 lines of routes
```

we can have:

```text
routes/
├── userRoutes.js
├── productRoutes.js
├── orderRoutes.js
└── authRoutes.js
```

### Example

`userRoutes.js`

```js
const express = require('express');

const router = express.Router();

router.get('/', getUsers);

router.post('/', createUser);

module.exports = router;
```

Then in `app.js`:

```js
const userRoutes = require('./routes/userRoutes');

app.use('/users', userRoutes);
```

Now these APIs are available:

```text
GET  /users
POST /users
```

### Why use it?

It makes the project:

* Cleaner
* Easier to understand
* Easier to test
* Easier to maintain

---

# 10. Difference Between Authentication and Authorization

These two words are very common in interviews.

## Authentication

Authentication means:

> Who are you?

For example, a user logs in using:

```text
Email
Password
```

The server checks whether the login details are correct.

---

## Authorization

Authorization means:

> What are you allowed to do?

For example:

```text
Admin → Can delete users

Manager → Can update users

Normal User → Can only view their profile
```

### Easy way to remember

```text
Authentication = Who are you?

Authorization = What can you do?
```

### Real-world example

When you enter a company:

The security guard checks your ID.

That is **authentication**.

After entering, your employee role decides whether you can enter the server room.

That is **authorization**.

---

# 11. How Do You Implement Role-Based Access Control (RBAC)?

RBAC means giving permissions based on a user's role.

For example:

```text
Admin
Manager
User
```

Each role has different permissions.

### Example

```js
const checkRole = (role) => {
  return (req, res, next) => {
    if (req.user.role !== role) {
      return res.status(403).json({
        message: 'Access denied'
      });
    }

    next();
  };
};
```

Then:

```js
app.delete(
  '/users/:id',
  authMiddleware,
  checkRole('admin'),
  deleteUser
);
```

Now only an admin can delete users.

### Real-world example

Imagine an employee management system:

```text
Admin:
- Create employee
- Update employee
- Delete employee

Manager:
- View employee
- Update employee

Employee:
- View own profile
```

This is RBAC.

---

# 12. How Would You Secure an Express.js API?

I would use multiple security methods.

### 1. Use HTTPS

HTTPS encrypts data between the client and server.

### 2. Validate input

Never trust data coming from the client.

### 3. Hash passwords

Never store plain-text passwords.

For example:

```text
Wrong:

password = "hello123"

Correct:

password = "$2b$10$...."
```

### 4. Authentication

Only logged-in users should access protected APIs.

### 5. Authorization

Users should only access resources they are allowed to use.

### 6. Rate limiting

Rate limiting helps stop users from sending too many requests.

### 7. Secure cookies

When using cookies for authentication, configure them securely.

### 8. CORS

Only allow trusted frontend origins when appropriate.

### 9. Environment variables

Don't put secrets directly in the source code.

```js
const dbPassword = process.env.DB_PASSWORD;
```

### 10. Keep dependencies updated

Old packages can contain security problems.

### Real-world example

For a banking application, I would not allow a normal user to access admin APIs.

I would use:

```text
HTTPS
+
Authentication
+
Authorization
+
Validation
+
Rate Limiting
+
Secure Cookies/Tokens
+
Error Handling
```

---

# 13. Explain CORS and Common Issues Developers Face

CORS stands for:

**Cross-Origin Resource Sharing**

It controls which websites can make requests to your API from a browser.

For example:

```text
Frontend:
https://myshop.com

Backend:
https://api.myshop.com
```

These are different origins.

The backend needs to allow the frontend if browser requests are expected.

### Express example

```js
const cors = require('cors');

app.use(cors({
  origin: 'https://myshop.com'
}));
```

### Common CORS problems

Developers often see:

```text
Access to fetch has been blocked by CORS policy
```

Common reasons include:

* Wrong frontend URL
* Backend doesn't allow the frontend origin
* Incorrect credentials configuration
* OPTIONS/preflight request not handled correctly
* Different configuration between development and production

### Real-world example

During development:

```text
Frontend:
http://localhost:3000
```

But after deployment:

```text
Frontend:
https://myshop.com
```

If the backend only allows:

```text
http://localhost:3000
```

the production frontend can get a CORS error.

---

# 14. How Do Cookies and Sessions Work in Express.js?

A cookie is a small piece of data stored in the user's browser.

The server can send a cookie to the browser.

The browser then sends that cookie with future requests.

### Basic flow

```text
User Login
    ↓
Server creates session
    ↓
Server sends session cookie
    ↓
Browser stores cookie
    ↓
Browser sends cookie with next request
    ↓
Server finds session
    ↓
User is recognized
```

### Express example

Using `express-session`:

```js
const session = require('express-session');

app.use(session({
  secret: process.env.SESSION_SECRET,
  resave: false,
  saveUninitialized: false
}));
```

After login:

```js
req.session.userId = user.id;
```

Now the server can identify the logged-in user using the session.

### Real-world example

Suppose you log in to an online shopping website.

You don't want to log in again every time you open:

```text
Profile
Orders
Cart
Settings
```

The session helps the server remember that you are logged in.

### Important point

In a production application, sessions should use an appropriate shared session store rather than relying on a single server's memory.

---

# 15. Difference Between Stateless and Stateful Authentication

## Stateful Authentication

In stateful authentication, the server stores information about the user's session.

### Flow

```text
User Login
    ↓
Server creates session
    ↓
Session stored on server
    ↓
Browser receives session ID
    ↓
Browser sends session ID
    ↓
Server finds session
```

The server keeps information about the user's login.

---

## Stateless Authentication

In stateless authentication, the server does not keep the login session in server memory.

A common example is JWT-based authentication.

### Flow

```text
User Login
    ↓
Server creates token
    ↓
Client receives token
    ↓
Client sends token with requests
    ↓
Server verifies token
```

The server mainly verifies the token instead of looking up a server-side session.

---

## Simple Example

Think about a hotel.

### Stateful

The hotel keeps your booking information in its system.

When you arrive, they look up your booking.

```text
Your ID
   ↓
Hotel System
   ↓
Your Booking
```

### Stateless

You have a valid signed ticket.

The staff checks the ticket instead of looking up your session.

```text
Your Ticket
    ↓
Verify Ticket
    ↓
Allow Access
```

---

# Quick Interview Revision

Before an interview, remember these simple points:

```text
1. Request lifecycle
   → Request → Middleware → Route → Controller → Database → Response

2. Middleware
   → Function between request and response

3. Middleware types
   → Application, Router, Error handling

4. next()
   → Moves to the next middleware

5. Project structure
   → Routes, Controllers, Services, Models, Middleware

6. REST API
   → Use proper HTTP methods and status codes

7. Error handling
   → One centralized error middleware

8. Validation
   → Check request data before using it

9. Route modularization
   → Keep routes in separate files

10. Authentication
    → Who are you?

11. Authorization
    → What can you do?

12. RBAC
    → Permissions based on roles

13. API security
    → HTTPS, validation, auth, rate limiting, secure cookies, etc.

14. CORS
    → Controls browser cross-origin requests

15. Sessions
    → Server remembers the user's session

16. Stateless auth
    → Server verifies a token instead of storing the session
```

# One-Line Answers for Fast Revision

**What is Express.js?**

Express.js is a Node.js framework used to build web servers and APIs easily.

**What is middleware?**

Middleware is a function that runs between the request and response.

**What is `next()`?**

`next()` tells Express to continue to the next middleware or route.

**Authentication vs Authorization?**

Authentication checks who you are, while authorization checks what you can do.

**What is RBAC?**

RBAC gives users permissions based on their roles.

**What is CORS?**

CORS controls which origins can make browser requests to an API.

**What is centralized error handling?**

It means handling application errors in one common middleware.

**What is validation?**

Validation checks whether incoming data is correct and acceptable.

**What is a session?**

A session allows the server to remember a user's login state.

**Stateful vs Stateless?**

Stateful authentication stores session information on the server, while stateless authentication verifies information such as a token without keeping that login session in server memory.
## 🗄️ Database & Distributed Systems Interview Questions

## Transaction Isolation & Locking

### Q75. What are transaction isolation levels?

Transaction isolation levels define how much one transaction is isolated from other transactions running at the same time.

Common levels are:

* Read Uncommitted
* Read Committed
* Repeatable Read
* Serializable

---

### Q76. What is Read Uncommitted?

Read Uncommitted allows a transaction to read data that another transaction has **not committed yet**.

* Lowest isolation level
* Can cause dirty reads
* Provides better performance but less consistency

---

### Q77. What is Read Committed?

Read Committed allows a transaction to read only **committed data**.

* Prevents dirty reads
* Can still have non-repeatable reads
* Common default isolation level in many databases

---

### Q78. What is Repeatable Read?

Repeatable Read ensures that once a transaction reads a row, reading the same row again during the transaction returns the **same value**.

* Prevents dirty reads
* Prevents non-repeatable reads
* Phantom-read behavior can depend on the database implementation

---

### Q79. What is Serializable isolation?

Serializable is the **highest standard isolation level**.

It makes concurrent transactions behave as if they were executed **one after another**.

* Prevents dirty reads
* Prevents non-repeatable reads
* Prevents phantom reads
* Provides strong consistency but can reduce performance

---

### Q80. What are dirty reads, non-repeatable reads, and phantom reads?

**Dirty Read:**
Reading data written by another transaction before that transaction commits.

**Non-Repeatable Read:**
Reading the same row twice and getting different values because another transaction changed it.

**Phantom Read:**
Running the same query twice and getting a different set of rows because another transaction inserted or deleted matching rows.

---

### Q81. What is optimistic locking?

Optimistic locking assumes that **conflicts are rare**.

The application checks whether the data has changed before updating it, usually using a **version number**.

Example:

```text
Read record → version = 5

Update record only if version = 5

If version changed → update fails
```

---

### Q82. What is pessimistic locking?

Pessimistic locking assumes that **conflicts are likely**.

The database locks the data before modifying it so that other transactions cannot modify it at the same time.

Example:

```sql
SELECT * FROM users
WHERE id = 10
FOR UPDATE;
```

---

### Q83. What is the difference between optimistic and pessimistic locking?

| Optimistic Locking            | Pessimistic Locking            |
| ----------------------------- | ------------------------------ |
| Assumes conflicts are rare    | Assumes conflicts are common   |
| Does not lock immediately     | Locks the data                 |
| Usually uses version numbers  | Uses database locks            |
| Better concurrency            | Can cause waiting/blocking     |
| Good for low-conflict systems | Good for high-conflict systems |

---

# Distributed Systems & Data Architecture

### Q84. What is the CAP theorem?

CAP theorem says that a distributed system cannot guarantee **Consistency, Availability, and Partition Tolerance simultaneously during a network partition**.

During a partition, the system must choose between:

* Consistency
* Availability

---

### Q85. What are Consistency, Availability, and Partition Tolerance?

**Consistency:**
Every node sees the same/latest data.

**Availability:**
Every request receives a response, even if some nodes fail.

**Partition Tolerance:**
The system continues working even when network communication between nodes fails.

---

### Q86. What is the difference between CP and AP systems?

**CP — Consistency + Partition Tolerance**

The system prioritizes correct, consistent data. During a network partition, it may reject or delay some requests.

**AP — Availability + Partition Tolerance**

The system continues accepting requests during a partition, but different nodes may temporarily have different data.

```text
CP → Consistency + Partition Tolerance

AP → Availability + Partition Tolerance
```

---

### Q87. What is the PACELC theorem?

PACELC extends CAP.

It says:

```text
If Partition:
    Choose Availability or Consistency

Else:
    Choose Latency or Consistency
```

So PACELC considers both **network failures** and **normal operation**.

---

### Q88. How does PACELC extend the CAP theorem?

CAP mainly explains the trade-off between **Consistency and Availability during a network partition**.

PACELC adds another trade-off:

**During normal operation, should the system prioritize lower Latency or stronger Consistency?**

---

### Q89. What happens when an asynchronous read replica lags behind the primary node?

The read replica may contain **old or stale data**.

Example:

```text
Primary:
User balance = $100

Replica:
User balance = $80
```

If the application reads from the replica before replication catches up, it may see `$80`.

---

### Q90. How can replication lag and read-your-own-writes consistency be handled?

Common solutions include:

* Read important data from the **primary**
* Use **sticky sessions**
* Wait for the replica to catch up
* Track replication position/LSN
* Use synchronous replication when strong consistency is required

Example:

```text
User writes data
       ↓
Read from Primary
       ↓
Always sees latest write
```

---

# Deep-Dive Indexing Mechanics

### Q91. What is a B-Tree?

A B-Tree is a **balanced tree data structure** commonly used for database indexes.

It makes searching, inserting, deleting, and range queries efficient.

Example:

```text
        [50]
       /    \
 [10,20]   [60,70]
```

---

### Q92. What is an LSM-Tree?

LSM stands for **Log-Structured Merge-Tree**.

It is a data structure designed for efficient writes.

Data is first written to memory and later flushed and merged into sorted files on disk.

It is commonly used in **write-heavy systems**.

---

### Q93. What is the difference between a B-Tree and an LSM-Tree?

| B-Tree                          | LSM-Tree                      |
| ------------------------------- | ----------------------------- |
| Updates data in place           | Writes data and merges later  |
| Good read performance           | Excellent write performance   |
| Common in traditional databases | Common in write-heavy systems |
| Less compaction                 | Requires compaction           |
| Good for range queries          | Also supports range queries   |

---

### Q94. What is a covering index?

A covering index is an index that contains **all the columns required by a query**.

Example:

```sql
CREATE INDEX idx_users
ON users(id, name, email);
```

Query:

```sql
SELECT name, email
FROM users
WHERE id = 10;
```

The index contains everything the query needs, so the database may not need to access the main table.

---

### Q95. What is an index-only scan?

An index-only scan happens when the database can answer a query **using only the index**, without reading the table/heap.

Example:

```text
Query
  ↓
Index
  ↓
Result
```

Instead of:

```text
Query
  ↓
Index
  ↓
Table/Heap
  ↓
Result
```

---

### Q96. When can a query be satisfied entirely from an index without accessing the table/heap?

A query can be satisfied entirely from an index when the index contains **all the data required by the query**.

For example:

```sql
CREATE INDEX idx_users
ON users(id, name, email);
```

Query:

```sql
SELECT name, email
FROM users
WHERE id = 10;
```

The database can potentially get `name` and `email` directly from the index.

---

# Connection Management & Caching

### Q97. What is connection pooling?

Connection pooling means maintaining a **pool of reusable database connections**.

Instead of creating a new connection for every request, the application reuses existing connections.

```text
Request
   ↓
Connection Pool
   ↓
Database
```

---

### Q98. Why do databases fail under sudden traffic spikes without connection pooling?

Without connection pooling, every request may create a new database connection.

During a traffic spike:

```text
Thousands of requests
        ↓
Thousands of connections
        ↓
Database connection limit reached
        ↓
Slowdown / errors
```

Connection pooling limits the number of active connections and reuses them.

---

### Q99. What are caching strategies?

Caching strategies define **how an application reads and writes cached data**.

Common strategies include:

* Cache-aside
* Write-through
* Write-behind
* Read-through

---

### Q100. What is cache-aside (lazy loading)?

The application first checks the cache.

If the data is not found, it reads from the database and then stores the result in the cache.

```text
Request
   ↓
Cache
   ↓ miss
Database
   ↓
Cache
   ↓
Response
```

This is one of the most commonly used caching strategies.

---

### Q101. What is write-through caching?

With write-through caching, data is written to the **cache and database together**.

```text
Application
     ↓
   Cache
     ↓
 Database
```

It provides better consistency but can make writes slower.

---

### Q102. What is write-behind caching?

With write-behind caching, data is first written to the **cache**.

The cache writes the data to the database later, usually asynchronously.

```text
Application
     ↓
   Cache
     ↓
Database later
```

It provides fast writes but introduces a risk of data loss if the cache fails before the database is updated.

---

### Q103. What are cache stampede/thundering herd, cache penetration, and cache breakdown?

**Cache Stampede / Thundering Herd:**
Many requests try to load the same data from the database when a popular cache entry expires.

**Cache Penetration:**
Requests repeatedly ask for data that does not exist, causing repeated database queries.

**Cache Breakdown:**
A very popular cache entry expires and many requests suddenly access the database at the same time.

Common solutions include:

* TTL with jitter
* Distributed locks
* Request coalescing
* Caching negative results
* Cache warming

---

# Production Node.js & ORM Nuances

### Q104. What is the N+1 query problem?

The N+1 problem happens when the application executes **1 query to get a list and then N additional queries for each item**.

Example:

```text
1 query → Get 100 users

100 queries → Get orders for each user

Total = 101 queries
```

This can cause serious performance problems.

---

### Q105. How can the N+1 query problem be solved?

Common solutions include:

* Use JOINs
* Use eager loading
* Use batch queries
* Use `IN` queries
* Use DataLoader/batching

Instead of:

```text
101 queries
```

try to fetch the data using:

```text
1–few queries
```

---

### Q106. What are database migrations in zero-downtime deployments?

Database migrations are controlled changes to the database schema.

In zero-downtime deployments, migrations should allow **old and new application versions to work at the same time**.

Example:

```text
Old App ──┐
          ├── Database
New App ──┘
```

The application should continue working while the database changes are applied.

---

### Q107. What is the expand-and-contract pattern?

Expand-and-contract is a safe way to change a database schema without breaking running applications.

### Step 1: Expand

Add the new column/table while keeping the old one.

### Step 2: Migrate

Update the application and migrate the data.

### Step 3: Contract

After all old application versions are gone, remove the old column/table.

```text
Expand → Migrate → Contract
```

---

### Q108. Why should you avoid renaming or dropping a column in a single migration while older application instances are still running?

Because older application instances may still use that column.

Example:

```text
Old Application
      ↓
Reads "name" column

Migration
      ↓
Drops "name" column

Old Application
      ↓
ERROR
```

Instead, use the **expand-and-contract pattern**.

```text
Add new column
      ↓
Update application
      ↓
Migrate data
      ↓
Remove old column
```

This allows old and new application versions to run safely during deployment.


# Interview Tip

Don't try to memorize the answers word-for-word.

For most Node.js questions, answer in this order:

```text
1. What is it?
2. Why do we use it?
3. Give a small example.
4. Give a real-world example.
```

For example, if they ask about streams:

> "Streams allow us to process data in chunks instead of loading the whole thing into memory. They are useful for large files, uploads, and downloads. For example, if a user uploads a 2 GB file, I would use a stream instead of putting the complete file into memory."


📌 About

This README is organized as a personal interview-preparation guide for JavaScript and full-stack web development.

