---
sidebar_position: 99
---

# Modern Javascript

## Array Destructuring

Way to extract values from arrays or properties from objects

```js
const [x, y] = arr;
```

## Default Parameters

```js
const [a = 1, b = 2] = [10];
console.log(a); // 10
console.log(b); // 2
```

## Spread Operator (...)

Used to “spread” or expand values from arrays or objects

```js
const arr1 = [1, 2];
const arr2 = [3, 4];

const combined = [...arr1, ...arr2];
```

## Rest Parameter (...)

Used to collect remaining items into an array or object.

```js
const [first, ...rest] = [10, 20, 30, 40];
console.log(first); // 10
console.log(rest);  // [20, 30, 40]
```

## ES6 and Modern JavaScript

- let, const, Arrow Functions, Array Destructuring, Spread Operator, Rest Parameter, Template Literals, Modules (import / export), Promises & Async/Await

### Debounce vs Throttle

- Debounce - Delays execution of a function until after a specified time has passed. Keypress, Search box input
- Throttle - Ensures a function is only called once in a specified interval, even if triggered multiple times. - limit the rate of execution - Tracking scroll position at most once every 200ms