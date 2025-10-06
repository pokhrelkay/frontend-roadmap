---
sidebar_position: 1
---

# Variables

Variables are fundamental building blocks in JavaScript. They allow you to store and manage data that your program can use and manipulate later.

---

## 1. Declaring Variables

JavaScript provides three main ways to declare variables:

### `var`
- The **oldest** way to declare variables.
- Function-scoped or globally scoped.
- Can be **redeclared** and **updated**.

```js
var name = "Alice";
var name = "Bob"; // ✅ redeclaration allowed
```
> ⚠️ `var` can lead to unexpected behavior due to its scoping and hoisting rules. It is generally avoided in modern code.

> ⚠️ `var` can be accessed outside the function it was declared.

### `let`
- Introduced in ES6 (2015).
- Block-scoped (limited to `{ }`).
- Can be updated but not redeclared in the same scope.

```js
let age = 25;
age = 30; // ✅ allowed
let age = 40; // ❌ Error: already declared
```

### `const`
- Also introduced in ES6 (2015).
- Block-scoped like `let`.
- Must be initialized at declaration.
- Cannot be reassigned.

```js
const pi = 3.14;
pi = 3.14159; // ❌ Error
```
> ⚠️ `const` does not make objects immutable — it only prevents reassignment:

```js
const person = { name: "Alice" };
person.name = "Bob"; // ✅ allowed
```

## 2. Variable Naming Rules

When naming variables in JavaScript:
- Must start with a letter, _ (underscore), or $ (dollar sign).
- Cannot start with a number.
- Case-sensitive (myVar and myvar are different).
- Cannot be reserved keywords (for, if, class, etc.).

✅ Valid names:
```js
let userName;
let _privateVar;
let $dollarSign;
```

❌ Invalid names:

```js
let 123name;   // cannot start with number
let for;       // reserved keyword
```

## 3. Hoisting

Hoisting is JavaScript’s behavior of moving variable and function declarations to the top of their scope during compilation.
- `var` is hoisted and initialized with `undefined`.
- `let` and `const` are hoisted but stay in the Temporal Dead Zone (TDZ) until declared.

```js
console.log(a); // undefined
var a = 5;

console.log(b); // ❌ ReferenceError
let b = 10;
```

## 4. Variable Scopes

Scope defines where a variable is accessible.

### Global Scope

Declared outside functions → accessible everywhere.

```js
var globalVar = "I am global";
console.log(globalVar); // works anywhere
```

### Function Scope

`var` inside a function → accessible only inside that function.

```js
function test() {
  var x = 10;
  console.log(x); // 10
}
console.log(x); // ❌ Error
```

### Block Scope

`let` and `const` → limited to { } block.

```js
if (true) {
  let y = 20;
  const z = 30;
  console.log(y, z); // works inside
}
console.log(y); // ❌ Error
```

## Summary

- Use `let` when you expect the variable’s value to change.
- Use `const` by default for constants or values you don’t want reassigned.
- Avoid `var` in modern JavaScript.
- Understand hoisting and scopes to avoid unexpected bugs.