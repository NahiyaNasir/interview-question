
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


🎯 One rule I want you to remember

When you see a difficult JavaScript question, don't try to guess the answer immediately.

Do this:

1. Is it synchronous or asynchronous?
2. If asynchronous, is it a microtask or a task?
3. If this appears, ask: how was the function called?
4. If there is await, remember that everything after await is postponed.
5. If objects are involved, ask: same reference or a copy?

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
# React Interview Questions — Q46 to Q60

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

# Node.js Interview Questions & Answers

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
# Express.js Interview Questions

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

