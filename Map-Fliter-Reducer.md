
# Map, Filter, and Reduce in JavaScript

## 1. Map

`map` ek method hai jo ek nayi array banata hai by applying ek diya hua function har element pe original array ke.

### Example:
```js
const numbers = [1, 2, 3];
const doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6]
```

---

## 2. Filter

`filter` ek method hai jo ek nayi array banata hai sirf un elements ke saath jo ek condition ko pass karte hain jo function mein define ki gayi hai.

### Example:
```js
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // [2, 4]
```

---

## 3. Reduce

`reduce` ek method hai jo ek array ko single value mein reduce karta hai ek function ke zariye jo har element ka result accumulate karta hai.

### Example:
```js
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((total, num) => total + num, 0);
console.log(sum); // 10
```

---

### Summary:

- **Map**: Array ke har element ko transform karta hai.
- **Filter**: Array ke elements ko filter karta hai based on a condition.
- **Reduce**: Ek array ko ek single value mein reduce karta hai.

---

# Map, Filter, and Reduce in JavaScript

*Here begins the English explanation of what was written above.*

## 1. Map

`map` is a method that creates a new array by applying a given function to each element of the original array.

### Example:
```js
const numbers = [1, 2, 3];
const doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6]
```

---

## 2. Filter

`filter` is a method that creates a new array with elements that pass the condition defined in the provided function.

### Example:
```js
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // [2, 4]
```

---

## 3. Reduce

`reduce` is a method that reduces an array to a single value by applying a function that accumulates the result of each element.

### Example:
```js
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((total, num) => total + num, 0);
console.log(sum); // 10
```

---

### Summary:

- **Map**: Transforms each element of the array.
- **Filter**: Filters elements based on a condition.
- **Reduce**: Reduces an array to a single value.