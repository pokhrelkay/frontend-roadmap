---
sidebar_position: 5
---

# Objects

## Prototypal Inheritance
Objects inherit from other objects using prototypes

```js
function Person(name) {
  this.name = name;
}
Person.prototype.greet = function() {
  return Hello, ${this.name};
};
```

## Copying Objects

### Shallow Copy
A shallow copy creates a new object and copies the top-level properties of the original object to it.

```js
const originalObject = { a: 1, b: { c: 2 } };
const shallowCopy = { ...originalObject };

const originalObject = { a: 1, b: { c: 2 } };
const shallowCopy = Object.assign({}, originalObject);
```

### Deep Copy
A deep copy creates a new object and recursively copies all properties, including nested objects and arrays, ensuring that no references are shared between the original and the copy.

```js
const originalObject = { a: 1, b: { c: 2 }, d: [3, 4] };
const deepCopy = JSON.parse(JSON.stringify(originalObject));

const originalObject = { a: 1, b: { c: 2 }, d: new Date() };
const deepCopy = structuredClone(originalObject);
```


## Object Iterations

#### Object.entries(object)
Returns an array of the key/value pairs of an object

#### Object.keys(object)
Returns an array of the keys of an object

#### Object.values(object)
Returns an array of the property values of an object

#### Object.groupBy(object, callback)
Groups object elements according to a function