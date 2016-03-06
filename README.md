# Javascript

#### Functional programming



## Higher order functions

A higher-order function is a function that does at least one of the following:

  * Take one or more functions as an input
  * Output a function

All other functions are first order functions.

Unlike many other languages with imperative features, JavaScript allows you to utilize higher-order functions because it has "first-class functions". This means functions can be treated just like any other value in JavaScript: just like Strings or Numbers, Function values can be stored as variables, properties on objects or passed to other functions as arguments. Function values are actually Objects (inheriting from Function.prototype) so you can even add properties and store values on them, just like any regular Object.

The key difference between Functions and other value types in JavaScript is the call syntax: if a reference to a function is followed by parens and some optional comma-separated values: someFunctionValue(arg1, arg2, etc), then the function body will be executed with the supplied arguments (if any).

### 

## **Basic functions**

### 1. Filter - [reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/GlobalObjects/Array/filter)

The **filter()** method creates a new array with all elements that pass the test implemented by the provided function.

#### Syntax

```
arr.filter(callback[, thisArg])
```

#### Parameters

- **callback**

  Function to test each element of the array. Invoked with arguments `(element, index, array)`. Return `true` to keep the element, `false` otherwise.

- **thisArg**

  Optional. Value to use as `this` when executing `callback`.

#### Code Example ([@jsbin](https://jsbin.com/wejebotuse/1/edit?js,console))

```javascript
var animals = [
{ name: 'Pepito',    species: 'cow' },
{ name: 'Menagnito', species: 'fish'},
{ name: 'Juanito',   species: 'dog' },
{ name: 'Jaimito',   species: 'cat' },
{ name: 'Boniatito', species: 'dog' },
{ name: 'Adolfito',  species: 'cow' }
];

var isDog = function(animal){
  return animal.species === 'dog'
}

var dogs = animals.filter(isDog);

console.log(dogs);
// result -> [{name: "Juanito", species: "dog"},{name: "Boniatito", species: "dog"}]
```





### 2. Map - [reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

The **map()** method creates a new array with the results of calling a provided function on every element in this array.

#### Syntax

```
arr.map(callback[, thisArg])
```

#### Parameters

- **callback**

  Function that produces an element of the new Array, taking three arguments:`currentValue`The current element being processed in the array.`index`The index of the current element being processed in the array.`array`The array `map` was called upon.

- **thisArg**

  Optional. Value to use as `this` when executing `callback`. Default value is the [Window ](https://developer.mozilla.org/en-US/docs/Web/API/Window)object

#### Code Example ([@jsbin](https://jsbin.com/ziwabaliwe/1/edit?js,console))

```javascript
var animals = [
{ name: 'Pepito',    species: 'cow' },
{ name: 'Menagnito', species: 'fish'},
{ name: 'Juanito',   species: 'dog' },
{ name: 'Jaimito',   species: 'cat' },
{ name: 'Boniatito', species: 'dog' },
{ name: 'Adolfito',  species: 'cow' }
];

var getName = function(animal){
  return animal.name
}

var namesOfAnimals = animals.map(getName);

console.log(namesOfAnimals);
// result -> ["Pepito", "Menagnito", "Juanito", "Jaimito", "Boniatito", "Adolfito"]
```





1. Every Some
2. Reduce
3. Recursion
4. Call



## Other Learning material

### A. Video Tutorials:

- [Higher-order functions - Part 1 of Functional Programming in JavaScript](https://www.youtube.com/watch?v=BMUiFMZr7vk&index=1&list=PL0zVEGEvSaeEd9hlmCXrk5yUyqUag-n84)


- [Map - Part 2 of Functional Programming in JavaScript](https://www.youtube.com/watch?v=bCqtb-Z5YGQ&index=2)
- [Reduce basics - Part 3 of Functional Programming in JavaScript](https://www.youtube.com/watch?v=Wl98eZpkp-c)

### B. NodeSchool.io

#### [Functional Javascript](https://github.com/timoxley/functional-javascript-workshop)

Learn fundamental functional programming features of JavaScript in vanilla ES5.

```
npm install -g functional-javascript-workshop
```