---
sidebar_position: 8
---

# Asynchronous Javascript

## Callbacks

```js
function fetchData(callback) {
  setTimeout(() => {
    callback();
  }, 2000);
}
fetchData(() => console.log('Data fetched'));
```

## Promises

```js
const fetchData = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Data fetched"), 2000);
});
```

## Async/Await

```js
async function getData() {
  const result = await fetchData;
  console.log(result);
}
```

## Event Loop

- Handles the execution of multiple pieces of code over time.
- Tasks: Call Stack, Web APIs, Callback Queue, Event Loop.