---
sidebar_position: 7
---

# Functional Programming

## Higher-Order Functions

A higher-order function is a function that

- Takes one or more functions as arguments Or returns a function
- Examples in JavaScript include map, filter, reduce, forEach, some, and every.

```js
function greet(name) {
  return `Hello, ${name}`;
}
function processUser(name, callback) {
  return callback(name);
}
processUser("John", greet); // Output: Hello, John
```

## Currying

- Currying transforms a function with multiple arguments into a series of unary (single-argument) functions.
- Useful in scenarios where partial function application is needed.

```js
function multiply(a) {
  return function(b) {
    return a * b;
  };
}
const double = multiply(2);
double(5); // Output: 10
```

## Function Composition

- Function composition is combining two or more functions to produce a new function.
- The result of one function is passed as input to the next.

```js
const add = x => x + 2;
const square = x => x * x;

const compose = (f, g) => x => f(g(x));

const addThenSquare = compose(square, add);
addThenSquare(3); // Output: 25 → square(add(3)) = 25
```

## Immutability

- Immutability means once a data structure is created, it cannot be changed.
- This avoids side effects and makes debugging easier.

```js
const person = { name: 'John' };
const updated = { ...person, age: 30 };

console.log(person); // { name: 'John' }
console.log(updated); // { name: 'John', age: 30 }
```

