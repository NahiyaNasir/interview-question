
JavaScript & Web Developer Interview Questions

A clean, GitHub-ready collection of full-stack web development and JavaScript interview questions and answers.

Use this README as a quick revision guide before technical interviews.

📚 Table of Contents

Behavioral Interview Questions

JavaScript Interview Questions

Variables & Hoisting

Core JavaScript

Functions & Scope

Modern JavaScript

Asynchronous JavaScript

Objects & Advanced Concepts

💬 Behavioral Interview Questions

1. Tell Me About Yourself

I’m a full-stack web developer who loves turning complex ideas into clean, fast, and easy-to-use web applications. Over the last few years, I’ve built everything from healthcare management portals to media streaming platforms and e-commerce stores.

My daily focus is on modern web tools like Next.js, React, Node.js, PostgreSQL, and Tailwind CSS. Beyond just writing code that works, I care a lot about smooth UI, fast performance, and clean database architecture. I really enjoy taking a project from an initial feature idea all the way to a live, working product.

2. What Is Your Strength?

My biggest strength is my problem-solving mindset and ability to pick up new tools fast.

When I run into a tricky bug—whether it’s handling real-time status updates in a database, setting up complex cron jobs, or debugging a tricky third-party API integration—I don't get frustrated. I systematically trace the problem, break it down, and fix it. I’m also super reliable when it comes to ownership; if a task is handed to me, I make sure it gets done right and on time.

3. What Is Your Weakness?

Sometimes I get too caught up in tweaking small UI details or optimizing code early on, which can slow down my initial speed.

For example, I’ll find myself spending extra time perfecting an animation or re-factoring a component when the core feature just needs to be shipped first. To fix this, I’ve started setting strict timer targets: get the functional MVP out first, get feedback, and then go back to polish the UI and performance.

4. Why Should We Hire You?

Because I bring a solid balance of technical skills, speed, and real product experience.

I don't just write code off a spec sheet; I think about the end user and how the app will handle real-world edge cases. Whether it’s setting up secure payment processing, managing complex database schemas, or crafting responsive interfaces with Tailwind and Framer Motion, I know how to deliver complete features without needing constant hand-holding. I’m ready to step in, collaborate with your team, and ship clean code from day one.

5. Why Did You Choose Web Development as a Career?

Honestly, it comes down to instant feedback and impact.

With web development, you write a few lines of code, refresh the browser, and suddenly there’s a real interactive tool on your screen that anyone in the world can use. That feeling never gets old for me. I love that the web is constantly evolving—there’s always a new framework to try, a faster way to query a database, or a better way to design an interface. It keeps work interesting every single day.

🟨 JavaScript Interview Questions

Variables & Hoisting

1. What Is the Difference Between var, let, and const?

var, let, and const are used to create variables in JavaScript.

var

var is the older way to declare variables. It is function-scoped and can be redeclared.

var name = "John";

var name = "Mike";

console.log(name);
// Mike

let

let is block-scoped and can be changed, but it cannot be redeclared in the same scope.

let age = 20;

age = 25;

console.log(age);
// 25

const

const is also block-scoped, but its value cannot be reassigned.

const country = "Bangladesh";

country = "India"; // Error

In simple words:

var → old way, can be redeclared

let → value can be changed

const → value cannot be reassigned

2. Explain the Concept of Hoisting in JavaScript

Hoisting means JavaScript processes declarations before running the code.

For example, a function declaration can be called before it is written.

greet();

function greet() {
  console.log("Hello");
}

// Hello

Variables declared with var are also hoisted, but their value is initially undefined.

console.log(name);

var name = "John";

// undefined

let and const are also hoisted, but they cannot be used before their declaration because of the Temporal Dead Zone (TDZ).

console.log(age); // Error

let age = 20;

Core JavaScript

3. What Are the Primitive Data Types in JavaScript?

Primitive data types are the basic types of values in JavaScript.

There are 7 primitive data types:

String

Number

BigInt

Boolean

Undefined

Null

Symbol

Example

let name = "John";        // String
let age = 25;             // Number
let bigNumber = 123n;     // BigInt
let isStudent = true;     // Boolean
let address;              // Undefined
let data = null;          // Null
let id = Symbol("id");    // Symbol

Primitive values are not objects and are treated as individual values.

4. What Is the Difference Between == and ===?

== and === are used to compare values, but they work differently.

==

== compares values after doing type conversion if needed.

console.log(5 == "5");

// true

Here, JavaScript converts the string "5" into a number before comparing.

===

=== compares both the value and the data type.

console.log(5 === "5");

// false

Here, one value is a number and the other is a string.

In most cases, === is preferred because it gives more predictable results.

In simple words:

== → compares after type conversion

=== → compares value and type

Functions & Scope

5. Explain How Closures Work in JavaScript

A closure happens when a function remembers variables from the place where it was created, even after that outer function has finished running.

Example

function counter() {
  let count = 0;

  return function () {
    count++;
    return count;
  };
}

const increase = counter();

console.log(increase());
// 1

console.log(increase());
// 2

console.log(increase());
// 3

6. What Is the Difference Between null and undefined?

undefined usually means a variable has been declared but no value has been given to it.

let name;

console.log(name);

// undefined

In simple words:

undefined → value has not been assigned

null → intentionally empty value

7. What Are Arrow Functions and How Do They Differ from Regular Functions?

Arrow functions are a shorter way to write functions.

Regular Function

function add(a, b) {
  return a + b;
}

Arrow Function

const add = (a, b) => {
  return a + b;
};

8. What Is the Scope Chain in JavaScript?

The scope chain is the way JavaScript looks for a variable.

When JavaScript cannot find a variable in the current scope, it looks in the outer scope. It keeps going until it finds the variable or reaches the global scope.

Example

let name = "John";

function greet() {
  function sayHello() {
    console.log(name);
  }

  sayHello();
}

greet();

// John

9. Explain the Concept of the Temporal Dead Zone

The Temporal Dead Zone, or TDZ, is the time between entering a scope and declaring a let or const variable.

During this time, the variable cannot be used.

Example

console.log(age);

let age = 25;

10. What Is a Pure Function?

A pure function is a function that always gives the same output for the same input.

It also does not change anything outside the function.

Example

function add(a, b) {
  return a + b;
}

console.log(add(2, 3));
// 5

console.log(add(2, 3));
// 5

11. What Is the Difference Between Function Declaration and Function Expression?

A function declaration is created using the function keyword with a function name.

function greet() {
  console.log("Hello");
}

greet();

A function expression assigns a function to a variable.

const greet = function () {
  console.log("Hello");
};

12. What Are Default Parameters in JavaScript?

Default parameters allow us to give a default value to a function parameter.

If the caller does not provide a value, the default value is used.

Example

function greet(name = "Guest") {
  console.log(`Hello ${name}`);
}

greet("John");
// Hello John

greet();
// Hello Guest

13. What Is the typeof Operator?

The typeof operator is used to check the type of a value.

Example

console.log(typeof "Hello");
// string

console.log(typeof 25);
// number

console.log(typeof true);
// boolean

console.log(typeof undefined);
// undefined

console.log(typeof {});
// object

console.log(typeof function () {});
// function

14. Explain Type Coercion in JavaScript

Type coercion means JavaScript automatically converts one data type into another when needed.

Example

console.log("5" + 2);

// "52"

Modern JavaScript

15. What Is an Immediately Invoked Function Expression (IIFE)?

An IIFE is a function that runs immediately after it is created.

Example

(function () {
  console.log("Hello");
})();

16. What Is Destructuring in JavaScript?

Destructuring is a way to take values from an array or properties from an object and store them in separate variables.

Array Example

const numbers = [10, 20, 30];

const [a, b, c] = numbers;

console.log(a); // 10
console.log(b); // 20
console.log(c); // 30

17. What Are the Spread and Rest Operators?

The spread and rest operators both use ..., but they are used for different purposes.

Spread Operator

The spread operator is used to expand the values of an array or object.

const numbers = [1, 2, 3];

const newNumbers = [...numbers, 4, 5];

console.log(newNumbers);
// [1, 2, 3, 4, 5]

Rest Operator

The rest operator is used to collect multiple values into one array.

function addNumbers(...numbers) {
  return numbers.reduce((sum, num) => sum + num, 0);
}

console.log(addNumbers(10, 20, 30));
// 60

18. Explain the Difference Between map(), filter(), and reduce()

These are common methods used with arrays.

map()

map() is used to change every item in an array and returns a new array.

const numbers = [1, 2, 3];

const result = numbers.map(num => num * 2);

console.log(result);
// [2, 4, 6]

filter()

filter() is used to get only the items that match a condition.

const numbers = [1, 2, 3, 4, 5];

const result = numbers.filter(num => num > 2);

console.log(result);
// [3, 4, 5]

reduce()

reduce() is used to calculate one final value from an array.

const numbers = [1, 2, 3, 4];

const total = numbers.reduce((sum, num) => sum + num, 0);

console.log(total);
// 10

19. What Is the Difference Between for...in and for...of?

for...in is mainly used to loop through the keys or property names of an object.

const user = {
  name: "John",
  age: 25
};

for (let key in user) {
  console.log(key);
}

// name
// age

for...of is used to loop through the values of an array or other iterable objects.

const numbers = [10, 20, 30];

for (let number of numbers) {
  console.log(number);
}

// 10
// 20
// 30

20. What Are Template Literals and Tagged Templates?

Template literals are a way to create strings using backticks.

They make it easy to add variables inside a string.

const name = "John";
const age = 25;

const message = `My name is ${name} and I am ${age} years old.`;

console.log(message);
// My name is John and I am 25 years old.

Tagged templates allow a function to process a template literal.

function greet(strings, name) {
  return `${strings[0]}${name}`;
}

const name = "John";

console.log(greet`Hello ${name}`);
// Hello John

Asynchronous JavaScript

21. What Is the Event Loop in JavaScript?

JavaScript is single-threaded, which means it normally runs one task at a time.

The event loop helps JavaScript handle things like timers, promises, and user events without blocking the main code.

Example

console.log("Start");

setTimeout(() => {
  console.log("Timer");
}, 0);

console.log("End");

The timer does not run immediately. JavaScript first finishes the current code and then runs the timer callback.

The event loop keeps checking for tasks that are waiting to run.

22. Explain How Promises Work in JavaScript

A Promise is used to handle an operation that will finish in the future.

A Promise has three main states:

Pending

Fulfilled

Rejected

Example

const promise = new Promise((resolve, reject) => {
  const success = true;

  if (success) {
    resolve("Operation successful");
  } else {
    reject("Something went wrong");
  }
});

promise
  .then(result => {
    console.log(result);
  })
  .catch(error => {
    console.log(error);
  });

23. What Is async/await and How Does It Improve Upon Promises?

async/await is a simpler way to work with Promises.

An async function always returns a Promise.

await waits for a Promise to finish before moving to the next line.

Example

async function getData() {
  try {
    const response = await fetch("https://example.com/data");
    const data = await response.json();

    console.log(data);
  } catch (error) {
    console.log(error);
  }
}

Without async/await, we normally use .then() and .catch().

async/await makes asynchronous code look more like normal step-by-step code, so it is easier to read and understand.

Objects & Advanced Concepts

24. What Is the Difference Between call(), apply(), and bind()?

call(), apply(), and bind() are used to control the value of this inside a function.

call()

call() runs the function immediately and takes arguments separately.

apply()

apply() runs the function immediately and takes arguments in an array.

bind()

bind() returns a new function.

function greet(city) {
  console.log(`Hello ${this.name} from ${city}`);
}

const user = {
  name: "John"
};

greet.call(user, "Dhaka");

// Hello John from Dhaka

greet.apply(user, ["Dhaka"]);

// Hello John from Dhaka

const newGreet = greet.bind(user);

newGreet("Dhaka");

// Hello John from Dhaka

In simple words:

call() → runs now, arguments separately

apply() → runs now, arguments in an array

bind() → returns a new function

25. What Is Prototypal Inheritance in JavaScript?

Prototypal inheritance means that an object can use properties and methods from another object through its prototype.

Example

const person = {
  greet() {
    console.log("Hello");
  }
};

const student = Object.create(person);

student.greet();

// Hello

Here, student does not have its own greet() method.

It gets the greet() method from person through the prototype.

JavaScript uses prototypes to share properties and methods between objects.

26. Explain the Concept of the this Keyword

The this keyword refers to the object connected to the function when the function is called.

Inside an Object Method

const user = {
  name: "John",

  greet() {
    console.log(this.name);
  }
};

user.greet();

// John

function show() {
  console.log(this);
}

27. What Are JavaScript Modules (import / export)?

Modules allow us to split JavaScript code into different files.

We can export something from one file and import it into another file.

Export Example

// math.js

export function add(a, b) {
  return a + b;
}

Import Example

// app.js

import { add } from "./math.js";

console.log(add(2, 3));

28. What Is the Difference Between Shallow Copy and Deep Copy?

A shallow copy copies only the first level of an object.

If the object contains another object, the nested object is still shared.

Example

const user = {
  name: "John",
  address: {
    city: "Dhaka"
  }
};

const copy = { ...user };

copy.address.city = "Chittagong";

console.log(user.address.city);

// Chittagong

29. What Are WeakMap and WeakSet?

WeakMap and WeakSet are similar to Map and Set, but they hold objects weakly.

WeakMap

A WeakMap stores key-value pairs where the keys must be objects.

const weakMap = new WeakMap();

const user = {};

weakMap.set(user, "User data");

console.log(weakMap.get(user));

// User data

WeakSet

A WeakSet stores objects.

const weakSet = new WeakSet();

const user = {};

weakSet.add(user);

console.log(weakSet.has(user));

// true

30. Explain the Concept of Memoization

Memoization is a technique used to make a function faster by saving its previous results.

If the same input is given again, the function can use the saved result instead of calculating it again.

Example

function memoize(fn) {
  const cache = {};

  return function (num) {
    if (cache[num]) {
      return cache[num];
    }

    const result = fn(num);
    cache[num] = result;

    return result;
  };
}

function square(num) {
  console.log("Calculating...");
  return num * num;
}

const memoizedSquare = memoize(square);

console.log(memoizedSquare(5));
// Calculating...
// 25

console.log(memoizedSquare(5));
// 25

⭐ Quick Revision Checklist

Before an interview, make sure you can explain these without reading the answers:

var, let, const

Hoisting and TDZ

Primitive data types

== vs ===

Closures

null vs undefined

Arrow functions

Scope chain

Pure functions

Function declarations vs expressions

Default parameters

typeof

Type coercion

IIFE

Destructuring

Spread and rest

map(), filter(), reduce()

for...in vs for...of

Template literals

Event loop

Promises

async/await

call(), apply(), bind()

Prototypal inheritance

this

Modules

Shallow vs deep copy

WeakMap and WeakSet

Memoization

   REACT QUES
# Components, Hooks & State Management

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

📌 About

This README is organized as a personal interview-preparation guide for JavaScript and full-stack web development.

