
# JavaScript Array Methods and Data Structures

## Introduction
This project is designed to provide a thorough understanding of advanced array methods and key data structures in JavaScript. It covers the usage of `map`, `filter`, and `reduce` on arrays, as well as introduces typed arrays and the Set, Map, and Weak data structures.

## How to Use `map`, `filter`, and `reduce` on Arrays
### `map`
The `map` method creates a new array populated with the results of calling a provided function on every element in the calling array.

**Example:**

const numbers = [1, 2, 3, 4];
const squared = numbers.map(num => num * num);
console.log(squared); // Logs: [1, 4, 9, 16]


### `filter`
The `filter` method creates a new array with all elements that pass the test implemented by the provided function.

**Example:**

const numbers = [1, 2, 3, 4];
const even = numbers.filter(num => num % 2 === 0);
console.log(even); // Logs: [2, 4]


### `reduce`
The `reduce` method executes a reducer function (that you provide) on each element of the array, resulting in a single output value.

**Example:**

const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((acc, curr) => acc + curr, 0);
console.log(sum); // Logs: 10


## Typed Arrays
Typed arrays in JavaScript provide a mechanism for accessing raw binary data with specific types (e.g., `Int8Array`, `Uint8Array`, `Float32Array`).

**Example:**

const buffer = new ArrayBuffer(8); // Create a buffer of 8 bytes
const view = new Int32Array(buffer); // Create a typed array view
view[0] = 42;
console.log(view[0]); // Logs: 42


## The Set, Map, and Weak Data Structures
### Set
A `Set` is a collection of unique values. It can store any type of value, whether primitive or object references.

**Example:**

const set = new Set([1, 2, 3, 3, 4]);
set.add(5);
console.log([...set]); // Logs: [1, 2, 3, 4, 5]


### Map
A `Map` is a collection of key-value pairs where keys can be of any type.

**Example:**

const map = new Map();
map.set('name', 'Lencho');
map.set('age', 30);
console.log(map.get('name')); // Logs: Lencho


### WeakMap
A `WeakMap` is a collection of key-value pairs where keys are objects and values can be arbitrary values. It does not prevent garbage collection of keys.

**Example:**

let obj = {};
const weakMap = new WeakMap();
weakMap.set(obj, 'value');
console.log(weakMap.get(obj)); // Logs: value
obj = null; // obj is now eligible for garbage collection


### WeakSet
A `WeakSet` is similar to a `Set`, but its values must be objects and it does not prevent garbage collection of its items.

**Example:**

let obj1 = {};
const weakSet = new WeakSet();
weakSet.add(obj1);
console.log(weakSet.has(obj1)); // Logs: true
obj1 = null; // obj1 is now eligible for garbage collection


## Conclusion
This project covers essential array methods and data structures in JavaScript, including `map`, `filter`, and `reduce`, as well as typed arrays and collections such as Set, Map, and WeakMap. These tools and data structures are fundamental for efficient and effective JavaScript programming. Explore the code examples and documentation to deepen your understanding and mastery of these topics.

