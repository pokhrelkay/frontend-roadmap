---
sidebar_position: 3
---

# Expressions and Operators

In JavaScript, **expressions** and **operators** are fundamental building blocks that allow you to perform calculations, assign values, compare data, and control the flow of your program. This chapter introduces you to the different types of expressions and operators commonly used in JavaScript.

## What is an Expression?

An **expression** is any valid unit of code that resolves to a value. For example:

```javascript
5 + 3       // evaluates to 8
x * 10      // evaluates to the value of x multiplied by 10
"Hello" + " " + "World"  // evaluates to "Hello World"
```

Expressions can be as simple as a single value or variable, or more complex combinations involving operators and other expressions.

## Arithmetic Operators

Arithmetic operators perform mathematical operations on numeric values.

| Operator | Description          | Example       | Result  |
|----------|----------------------|---------------|---------|
| `+`      | Addition             | `2 + 3`       | `5`     |
| `-`      | Subtraction          | `5 - 2`       | `3`     |
| `*`      | Multiplication       | `4 * 3`       | `12`    |
| `/`      | Division             | `10 / 2`      | `5`     |
| `%`      | Modulus (remainder)  | `7 % 3`       | `1`     |
| `**`     | Exponentiation       | `2 ** 3`      | `8`     |

### Examples

```javascript
let a = 10;
let b = 3;

console.log(a + b); // 13
console.log(a - b); // 7
console.log(a * b); // 30
console.log(a / b); // 3.3333333333333335
console.log(a % b); // 1
console.log(a ** b); // 1000
```

## Assignment Operators

Assignment operators assign values to variables, often combining assignment with an arithmetic operation.

| Operator | Description               | Example          | Equivalent to          |
|----------|---------------------------|------------------|-----------------------|
| `=`      | Simple assignment         | `x = 5`          | Assigns 5 to x        |
| `+=`     | Add and assign            | `x += 3`         | `x = x + 3`           |
| `-=`     | Subtract and assign       | `x -= 2`         | `x = x - 2`           |
| `*=`     | Multiply and assign       | `x *= 4`         | `x = x * 4`           |
| `/=`     | Divide and assign         | `x /= 5`         | `x = x / 5`           |
| `%=`     | Modulus and assign        | `x %= 3`         | `x = x % 3`           |

### Examples

```javascript
let x = 10;

x += 5;  // x = 15
x *= 2;  // x = 30
x -= 10; // x = 20
x /= 4;  // x = 5
x %= 3;  // x = 2

console.log(x); // 2
```

## Comparison Operators

Comparison operators compare two values and return a Boolean (`true` or `false`).

| Operator | Description                    | Example         | Result          |
|----------|--------------------------------|-----------------|-----------------|
| `==`     | Equal to (loose equality)     | `5 == "5"`      | `true`          |
| `===`    | Equal to (strict equality)    | `5 === "5"`     | `false`         |
| `!=`     | Not equal (loose inequality) | `5 != "5"`      | `false`         |
| `!==`    | Not equal (strict inequality) | `5 !== "5"`     | `true`          |
| `>`      | Greater than                 | `7 > 3`         | `true`          |
| `<`      | Less than                    | `2 < 5`         | `true`          |
| `>=`     | Greater than or equal to     | `4 >= 4`        | `true`          |
| `<=`     | Less than or equal to        | `3 <= 2`        | `false`         |

### Examples

```javascript
console.log(5 == "5");   // true (loose equality)
console.log(5 === "5");  // false (strict equality)
console.log(10 != 5);    // true
console.log(10 !== "10"); // true
console.log(7 > 3);      // true
console.log(2 < 5);      // true
```

## Logical Operators

Logical operators are used to combine or invert Boolean values.

| Operator | Description          | Example             | Result  |
|----------|----------------------|---------------------|---------|
| `&&`     | Logical AND          | `true && false`     | `false` |
| `\|\|`   | Logical OR           | `true \|\| false`   | `true`  |
| `!`      | Logical NOT (negation) | `!true`           | `false` |

### Examples

```javascript
let isAdult = true;
let hasTicket = false;

console.log(isAdult && hasTicket);  // false
console.log(isAdult || hasTicket);  // true
console.log(!isAdult);               // false
```

## Ternary (Conditional) Operator

The ternary operator provides a shorthand way to write conditional expressions.

Syntax:

```javascript
condition ? expressionIfTrue : expressionIfFalse
```

### Example

```javascript
let age = 18;
let canVote = (age >= 18) ? "Yes" : "No";

console.log(canVote); // "Yes"
```

This is equivalent to:

```javascript
let canVote;
if (age >= 18) {
  canVote = "Yes";
} else {
  canVote = "No";
}
```

## Operator Precedence

Operator precedence determines the order in which operators are evaluated in an expression.

For example:

```javascript
let result = 3 + 4 * 5;
console.log(result); // 23
```

Here, multiplication (`*`) has higher precedence than addition (`+`), so `4 * 5` is evaluated first, then added to `3`.

### Common Precedence Rules (from highest to lowest):

1. Parentheses `()`
2. Exponentiation `**`
3. Multiplication `*`, Division `/`, Modulus `%`
4. Addition `+`, Subtraction `-`
5. Comparison operators `<`, `>`, `<=`, `>=`
6. Equality operators `==`, `!=`, `===`, `!==`
7. Logical AND `&&`
8. Logical OR `||`
9. Assignment `=`, `+=`, `-=`, etc.

Use parentheses to explicitly specify the order of evaluation and improve code readability:

```javascript
let result = (3 + 4) * 5;
console.log(result); // 35
```

```js
if (true) {
  let y = 20;
  const z = 30;
  console.log(y, z); // works inside
}
console.log(y); // ❌ Error
```

### `??` vs `||`

- The ?? operator returns its right-hand side operand only if its left-hand side operand is **null** or **undefined**.

- The || operator returns its right-hand side operand if its left-hand side operand is "**falsy**".

- Falsy values in JavaScript include **false**, **0**, **"" (empty string)**, **null**, **undefined**, and **NaN**.

## Summary

- **Expressions** are units of code that produce a value.
- **Arithmetic operators** perform mathematical calculations.
- **Assignment operators** assign and update variable values.
- **Comparison operators** compare values and return Booleans.
- **Logical operators** combine or invert Boolean values.
- **Ternary operator** provides a concise conditional expression.
- **Operator precedence** determines the order of evaluation in expressions.
