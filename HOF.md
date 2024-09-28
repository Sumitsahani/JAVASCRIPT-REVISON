# JavaScript Higher-Order Functions

### 🤔 What's a Higher-Order Function?

A **higher-order function** is a function that takes another function as an argument or returns a function. These are super handy, especially when working with arrays like `map()`, `filter()`, and `reduce()`! 💡

---

## Explanation

**Higher order functions** kaafi useful hote hain jab hum arrays ke sath kaam karte hain, jaise `map()`, `filter()`, aur `reduce()`. 🎯

For example, tumhe ek list of numbers ko modify karna hai, lekin tumhe pata nahi ki kaise modify karna hai. Toh tum ek higher-order function bana sakte ho jo ek function ko input lega aur numbers ke sath jo karna hai, wo karega! 😎

### 🔧 Example:

```javascript
function modifyArray(arr, operation) {
  let result = [];
  for (let i = 0; i < arr.length; i++) {
    result.push(operation(arr[i]));
  }
  return result;
}

function square(num) {
  return num * num;
}

function double(num) {
  return num * 2;
}

let numbers = [1, 2, 3, 4, 5];

console.log(modifyArray(numbers, square)); // [1, 4, 9, 16, 25] 🔢
console.log(modifyArray(numbers, double)); // [2, 4, 6, 8, 10] 💥
```

Is example mein, `modifyArray` ek higher-order function hai jo ek function ko (jaise `square` ya `double`) as an argument le raha hai aur use har ek element pe apply kar raha hai! 🚀

## Definition

**Hinglish**: Higher-order function ek aisa function hai jo dusre functions ko as argument accept karta hai ya return karta hai. Ye array operations ke liye kaafi useful hote hain! 😎

---

## 🌍 English Explanation

**Higher-order functions** are incredibly useful when working with arrays, like `map()`, `filter()`, and `reduce()`! 🌟

For instance, if you have a list of numbers and you're not sure how you want to modify them, you can create a higher-order function that takes another function as an input and applies it to the array elements. 💻

### 🔧 Example:

```javascript
function modifyArray(arr, operation) {
  let result = [];
  for (let i = 0; i < arr.length; i++) {
    result.push(operation(arr[i]));
  }
  return result;
}

function square(num) {
  return num * num;
}

function double(num) {
  return num * 2;
}

let numbers = [1, 2, 3, 4, 5];

console.log(modifyArray(numbers, square)); // [1, 4, 9, 16, 25] 🔢
console.log(modifyArray(numbers, double)); // [2, 4, 6, 8, 10] 💥
```

In this example, `modifyArray` is a higher-order function that takes a function (like `square` or `double`) and applies it to each element of the array. A great way to demonstrate higher-order functions in interviews! 🎯

---

## English Definition

**English**: A higher-order function is a function that accepts another function as an argument or returns a function. It's super useful for array operations! 💡
