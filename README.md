# interview-question
```

1. Tell Me About Yourself

```
"I’m a full-stack web developer who loves turning complex ideas into clean, fast, and easy-to-use web applications. Over the last few years, I’ve built everything from healthcare management portals to media streaming platforms and e-commerce stores.

My daily focus is on modern web tools like Next.js, React, Node.js, PostgreSQL, and Tailwind CSS. Beyond just writing code that works, I care a lot about smooth UI, fast performance, and clean database architecture. I really enjoy taking a project from an initial feature idea all the way to a live, working product."

```

2. What Is Your Strength?

```
"My biggest strength is my problem-solving mindset and ability to pick up new tools fast.

When I run into a tricky bug—whether it’s handling real-time status updates in a database, setting up complex cron jobs, or debugging a tricky third-party API integration—I don't get frustrated. I systematically trace the problem, break it down, and fix it. I’m also super reliable when it comes to ownership; if a task is handed to me, I make sure it gets done right and on time."

```

3. What Is Your Weakness?

```

"Sometimes I get too caught up in tweaking small UI details or optimizing code early on, which can slow down my initial speed.

For example, I’ll find myself spending extra time perfecting an animation or re-factoring a component when the core feature just needs to be shipped first. To fix this, I’ve started setting strict timer targets: get the functional MVP out first, get feedback, and then go back to polish the UI and performance."

```

4. Why Should We Hire You?

 ```
"Because I bring a solid balance of technical skills, speed, and real product experience.

I don't just write code off a spec sheet; I think about the end user and how the app will handle real-world edge cases. Whether it’s setting up secure payment processing, managing complex database schemas, or crafting responsive interfaces with Tailwind and Framer Motion, I know how to deliver complete features without needing constant hand-holding. I’m ready to step in, collaborate with your team, and ship clean code from day one."

```

5. Why Did You Choose Web Development as a Career?
```

"Honestly, it comes down to instant feedback and impact.

With web development, you write a few lines of code, refresh the browser, and suddenly there’s a real interactive tool on your screen that anyone in the world can use. That feeling never gets old for me. I love that the web is constantly evolving—there’s always a new framework to try, a faster way to query a database, or a better way to design an interface. It keeps work interesting every single day."
```

6.. What is the difference between var, let, and const in JavaScript?
```
var a = 1;
var a = 2; // Valid

let b = 1;
// let b = 2; // SyntaxError: Identifier 'b' has already been declared
b = 2; // Valid

const c = 10;
// c = 20; // Type Error: Assignment to constant variable.
```

7.Explain the concept of hoisting in JavaScript.

```
Hoisting is JavaScript's default behavior of moving function and variable declarations to the top of their containing scope during the compilation phase, before execution.

Functions: Full function declarations are hoisted completely, meaning they can be called before they appear in the code.

var: Declarations are hoisted and initialized to undefined.

let and const: Declarations are hoisted, but remain uninitialized in the Temporal Dead Zone (TDZ) until execution reaches their declaration line.

```
## Q16. What is destructuring in JavaScript? Explain with array and object examples.

Destructuring is a way to take values from an array or properties from an object and store them in separate variables.

### Array example:
```js
const numbers = [10, 20, 30];

const [a, b, c] = numbers;

console.log(a); // 10
console.log(b); // 20
console.log(c); // 30

## Q17. What are the spread and rest operators and how are they used?

The spread and rest operators both use `...`, but they are used for different purposes.

### Spread Operator

The spread operator is used to expand the values of an array or object.

```js
const numbers = [1, 2, 3];

const newNumbers = [...numbers, 4, 5];

console.log(newNumbers);
// [1, 2, 3, 4, 5]
###  Rest Operator

The rest operator is used to collect multiple values into one array.
```js
function addNumbers(...numbers) {
  return numbers.reduce((sum, num) => sum + num, 0);
}

console.log(addNumbers(10, 20, 30));
// 60


### Q18

```markdown
## Q18. Explain the difference between map(), filter(), and reduce().

These are common methods used with arrays.

### map()

`map()` is used to change every item in an array and returns a new array.

```js
const numbers = [1, 2, 3];

const result = numbers.map(num => num * 2);

console.log(result);
// [2, 4, 6]
### filtter()

`filter() ` is used to get only the items that match a condition.

```js
const numbers = [1, 2, 3, 4, 5];

const result = numbers.filter(num => num > 2);

console.log(result);
// [3, 4, 5]

###reduce()

reduce() is used to calculate one final value from an array.
const numbers = [1, 2, 3, 4];

const total = numbers.reduce((sum, num) => sum + num, 0);

console.log(total);
// 10

### Q19

```markdown
## Q19. What is the difference between for...in and for...of loops?

`for...in` is mainly used to loop through the keys or property names of an object.

```js
const user = {
  name: "John",
  age: 25
};

for (let key in user) {
  console.log(key);
}

// name
// age
// age

`for...of `is used to loop through the values of an array or other iterable objects.
```js
const numbers = [10, 20, 30];

for (let number of numbers) {
  console.log(number);
}

// 10
// 20
// 30

### Q20

```markdown
## Q20. What are template literals and tagged templates?

Template literals are a way to create strings using backticks.

They make it easy to add variables inside a string.

```js
const name = "John";
const age = 25;

const message = `My name is ${name} and I am ${age} years old.`;

console.log(message);
// My name is John and I am 25 years old.
Tagged templates allow a function to process a template literal.
```js
function greet(strings, name) {
  return `${strings[0]}${name}`;
}

const name = "John";

console.log(greet`Hello ${name}`);
// Hello John


### Q21

```markdown
## Q21. What is the event loop in JavaScript?

JavaScript is single-threaded, which means it normally runs one task at a time.

The event loop helps JavaScript handle things like timers, promises, and user events without blocking the main code.

Example:

```js
console.log("Start");

setTimeout(() => {
  console.log("Timer");
}, 0);

console.log("End");
The timer does not run immediately. JavaScript first finishes the current code and then runs the timer callback.

The event loop keeps checking for tasks that are waiting to run.





### Q22

```markdown
## Q22. Explain how Promises work in JavaScript.

A Promise is used to handle an operation that will finish in the future.

A Promise has three main states:

- Pending
- Fulfilled
- Rejected

Example:

```js
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

### Q23

```markdown
## Q23. What is async/await and how does it improve upon Promises?

`async/await` is a simpler way to work with Promises.

An `async` function always returns a Promise.

`await` waits for a Promise to finish before moving to the next line.

Example:

```js
async function getData() {
  try {
    const response = await fetch("https://example.com/data");
    const data = await response.json();

    console.log(data);
  } catch (error) {
    console.log(error);
  }
}

``Without async/await, we normally use .then() and .catch().

``async/await makes asynchronous code look more like normal step-by-step code, so it is easier to read and understan



### Q24

```markdown
## Q24. What is the difference between call(), apply(), and bind()?

`call()`, `apply()`, and `bind()` are used to control the value of `this` inside a function.

### call()

`call()` runs the function immediately and takes arguments separately.

```js
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

// Hello John from DhakaIn simple words:

call() → runs now, arguments separately
apply() → runs now, arguments in an array
bind() → returns a new function


### Q25

```markdown
## Q25. What is prototypal inheritance in JavaScript?

Prototypal inheritance means that an object can use properties and methods from another object through its prototype.

Example:

```js
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


### Q26

```markdown
## Q26. Explain the concept of this keyword in different contexts.

The `this` keyword refers to the object connected to the function when the function is called.

### Inside an Object Method

```js
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
### Q27

```markdown
## Q27. What are JavaScript modules (import/export)?

Modules allow us to split JavaScript code into different files.

We can export something from one file and import it into another file.

### Export Example

```js
// math.js

export function add(a, b) {
  return a + b;
}

### Q28

```markdown
## Q28. What is the difference between shallow copy and deep copy of objects?

A shallow copy copies only the first level of an object.

If the object contains another object, the nested object is still shared.

Example:

```js
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


### Q29

```markdown
## Q29. What are WeakMap and WeakSet and when would you use them?

`WeakMap` and `WeakSet` are similar to `Map` and `Set`, but they hold objects weakly.

### WeakMap

A `WeakMap` stores key-value pairs where the keys must be objects.

```js
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


### Q30

```markdown
## Q30. Explain the concept of memoization with an example.

Memoization is a technique used to make a function faster by saving its previous results.

If the same input is given again, the function can use the saved result instead of calculating it again.

Example:

```js
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
