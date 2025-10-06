---
sidebar_position: 2
---

# Data Types

JavaScript is a dynamically typed language, which means that variables can hold values of any data type and types are determined at runtime. Understanding JavaScript data types is fundamental to writing effective and bug-free code.

## Primitive Data Types

Primitive data types are the most basic data types in JavaScript. They represent a single value and are immutable (cannot be changed).

### 1. Number

Represents both integer and floating-point numbers.

```javascript
let age = 25;
let price = 19.99;
```

### 2. String

Represents sequences of characters enclosed in single quotes, double quotes, or backticks (template literals).

```javascript
let name = "John";
let greeting = 'Hello, world!';
let message = `Hi, ${name}!`;
```

### 3. Boolean

Represents logical entities and can have two values: `true` or `false`.

```javascript
let isActive = true;
let isLoggedIn = false;
```

### 4. Undefined

A variable that has been declared but not assigned a value has the value `undefined`.

```javascript
let x;
console.log(x); // undefined
```

### 5. Null

Represents the intentional absence of any object value.

```javascript
let data = null;
```

### 6. Symbol (ES6)

Represents a unique and immutable value, often used as identifiers for object properties.

```javascript
let sym = Symbol('id');
```

### 7. BigInt (ES2020)

Represents integers with arbitrary precision.

```javascript
let bigNumber = 9007199254740991n;
```

## Reference Data Types

Reference types are objects and collections of values.

### 1. Object

An unordered collection of key-value pairs.

```javascript
let person = {
  name: "Alice",
  age: 30
};
```

### 2. Array

An ordered list of values.

```javascript
let colors = ["red", "green", "blue"];
```

### 3. Function

Functions are also objects in JavaScript.

```javascript
function greet() {
  console.log("Hello!");
}
```

### 4. Date, RegExp, Map, Set, etc.

JavaScript provides many built-in objects for different purposes.

## Type Checking

You can check the type of a value using the `typeof` operator.

```javascript
console.log(typeof 42); // "number"
console.log(typeof "hello"); // "string"
console.log(typeof true); // "boolean"
console.log(typeof undefined); // "undefined"
console.log(typeof null); // "object" (this is a known quirk)
console.log(typeof {}); // "object"
console.log(typeof function(){}); // "function"
```

Note: `typeof null` returning `"object"` is a historical bug in JavaScript.

To check if a value is an array, use `Array.isArray()`:

```javascript
console.log(Array.isArray([1, 2, 3])); // true
```

## Type Conversion

JavaScript automatically converts types in many situations (type coercion), but you can also convert explicitly.

### Implicit Conversion

```javascript
console.log('5' + 3); // "53" (number 3 converted to string)
console.log('5' - 3); // 2 (string '5' converted to number)
```

### Explicit Conversion

- To Number:

```javascript
Number("123"); // 123
parseInt("123", 10); // 123
parseFloat("3.14"); // 3.14
```

- To String:

```javascript
String(123); // "123"
(123).toString(); // "123"
```

- To Boolean:

```javascript
Boolean(0); // false
Boolean("hello"); // true
```

## Summary

| Data Type   | Description                          | Example                  |
|-------------|----------------------------------|--------------------------|
| Number      | Numeric values                    | `42`, `3.14`             |
| String      | Textual data                     | `"hello"`, `'world'`     |
| Boolean     | Logical true/false               | `true`, `false`          |
| Undefined   | Variable declared but unassigned | `undefined`              |
| Null        | Intentional absence of value     | `null`                   |
| Symbol      | Unique identifiers               | `Symbol('id')`           |
| BigInt      | Large integers                  | `9007199254740991n`      |
| Object      | Collections of key-value pairs   | `{ name: "Alice" }`      |
| Array       | Ordered list of values           | `[1, 2, 3]`              |
| Function    | Callable objects                 | `function() {}`          |

