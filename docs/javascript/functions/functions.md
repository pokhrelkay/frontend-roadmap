---
sidebar_position: 4
---

# Functions
- Function declarations are hoisted, meaning they can be called before their definition in the code. 
- Function expressions are not hoisted in the same way.


## Pure Functions

- Always return the same output for the same input.
- No side effects – do not depend on or modify external state.

## Anonymous Functions

- Functions without a name.
- Common in callbacks and IIFEs.

```js
setTimeout(function() {
  console.log('Execute later after 1 second')
}, 1000);
```

## IIFEs (Immediately Invoked Function Expressions)

```js
(function () {
  const message = "Hello from IIFE";
  console.log(message);
})();
```

## Closures

Functions that remember the scope in which they were created.

```js
var updateClickCount = (function(){
  var counter = 0;
  return function(){
    ++counter;
    console.log(counter);
  }
})();
```

Use Case: Private Variables, Data Encapsulation

## This Keyword

- Refers to different values depending on context (global, object, strict mode)
- Use  **call, apply, bind** to control this

```js
function greet(greeting) {
  console.log(`${greeting}, I'm ${this.name}`);
}
const person = { name: "John" };
```

#### call
The call() method allows you to call a function with a specified `this` value
```js 
greet.call(person, "Hello"); // Hello, I'm John
```

#### apply
The apply() method is similar to the call() method, but it takes an `array of arguments` instead of individual arguments

```js
greet.apply(person, ["Hi"]); // Hi, I'm John
```

#### bind
- The bind() method returns a new function with a specified this value and any arguments that are passed to it.
- The bind() method does not call the function immediately but instead returns a new function that can be called later.
```js
const greetJohn = greet.bind(person);
greetJohn("Hola"); // Hola, I'm John
```
