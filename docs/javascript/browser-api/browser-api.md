---
sidebar_position: 10
---

# Browser APIs & Environment

## Event Handling

- Event Flow: **Capturing → Target → Bubbling**
- Techniques: Event Delegation, addEventListener

## Data Storage

- **Cookies**: Small, sent with every HTTP request
- **Local Storage**: Synchronous, 5MB, persistent

```js
localStorage.setItem("name", "John Doe");
localStorage.getItem("name");
```

- **Session Storage**: Synchronous, clears on tab close
- **IndexedDB**: Asynchronous, large data storage

## Fetch API

```js
async function getText(file) {
  let myObject = await fetch(file);
  let myText = await myObject.text();
  myDisplay(myText);
}
```

## Geolocation API
```js
navigator.geolocation.getCurrentPosition((position) => {
  console.log(position.coords.latitude);
});
```