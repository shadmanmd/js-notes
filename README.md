# Array inbuilt methods
## Array forEach
```javascript
const grades = [10, 8, 13];

grades.forEach(function(grade) {
    // do something with individual grade
    console.log(grade);
});

/* Output
10
8
13 */
```
## Array filter
The  `.filter()`  method returns a new array that contains some of the items from the original array, based on the condition you specify.
```javascript
let numbers = [9, 5, 14, 3, 11];

let numbersAboveTen = numbers.filter(function(number) {
    return number >= 10;
});
console.log(numbersAboveTen); // [14, 11]
```
## Array find
When you call the  `.find(callback)`  method on an array, you will get back  **the first item**  that matches the condition that you specify. If no items were found, you will get back  `undefined`.
```javascript
let names = ["Sam", "Alex", "Charlie"];

let result = names.find(function(name) {
  return name === "Alex";
});
console.log(result); // "Alex"
```
## .filter() vs .find()
```javascript
let numbers = [9, 5, 14, 3, 11];

// filter() ALWAYS returns an array
numbers.filter(function(number) {
    return number >= 12;
}); // [14]

// .find() returns the first match or undefined
numbers.find(function(number) {
    return number >= 12;
}); // 14
```
```javascript
let numbers = [9, 5, 14, 3, 11];

// filter() ALWAYS returns an array (even if it's empty)
numbers.filter(function(number) {
    return number >= 15;
}); // []

// .find() returns the first match or undefined (when none of the items satisfy the condition)
numbers.find(function(number) {
    return number >= 15;
}); // undefined
```
## Array map
The `.map(callback)` method allows you to **transform** an array into another one. 
Notice that you always get back an array containing the  **same number of items**  compared to the original array, but every item has most likely undergone some transformation.
```javascript
const numbers = [4, 2, 5, 8];

const doubled = numbers.map(function(number) {
    return number * 2;
});
console.log(doubled); // [8, 4, 10, 16]
```
## Array includes
```javascript
const groceries = ["Apple", "Peach", "Tomato"];

groceries.includes("Tomato"); // true
groceries.includes("Bread"); // false
```
## Array join(glue)
```javascript
const groceries = ["Apple", "Peach", "Tomato"];
groceries.toString(); // "Apple,Peach,Tomato"
```
```javascript
const groceries = ["Apple", "Peach", "Tomato"];
groceries.join("; "); // "Apple; Peach; Tomato"
groceries.join(" . "); // "Apple . Peach . Tomato"
```


