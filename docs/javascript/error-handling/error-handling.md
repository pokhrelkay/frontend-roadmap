---
sidebar_position: 9
---

# Error Handling
- try...catch for synchronous code
- Promise.catch or async/await + try...catch for async

```js
try {
  throw new Error("Oops!");
} catch (err) {
  console.log(err.message);
}
```