### ``Rest`` and ``Spread`` Operators in JavaScript 😎🚀

---

**1. Rest Operator**  
Rest operator ka kaam hota hai baaki bachi hui values ko ek array ke andar store karna. Iska syntax `...` hota hai, aur jab humein pata nahi hota kitni arguments pass honge, toh hum rest operator use karte hain. 😁

```javascript
function sum(...numbers) {
  let total = 0;
  numbers.forEach((num) => {
    total += num;
  });
  return total;
}

console.log(sum(2, 3, 5, 7)); // Output: 17
```

🔍 **Explanation:**  
Yahan pe `...numbers` saare extra arguments ko ek array `numbers[]` mein convert kar deta hai, aur fir hum us array ka use karke sum nikal rahe hain. ➕💻

---

**2. Spread Operator**  
Spread operator ka kaam hota hai kisi array ya object ke elements ko individual items mein todna. 🧩 Iska syntax bhi `...` hota hai, lekin ye existing array ya object ko expand karta hai.

```javascript
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5, 6];

console.log(arr2); // Output: [1, 2, 3, 4, 5, 6]
```

🛠️ **Explanation:**  
Yahan pe `...arr1` ne array ke har element ko tod ke `arr2` ke andar daal diya. ⚡️🎯

---

### Rest and Spread Operators 🌟💡

---

**1. Rest Operator**  
The rest operator is used to collect all remaining elements into an array. 📥 Its syntax is `...`, and we use it when we are unsure of the number of arguments that will be passed.

```javascript
function sum(...numbers) {
  let total = 0;
  numbers.forEach((num) => {
    total += num;
  });
  return total;
}

console.log(sum(2, 3, 5, 7)); // Output: 17
```

🔍 **Explanation:**  
Here, `...numbers` converts all extra arguments into an array `numbers[]`, and then we use that array to calculate the sum. ✨✅

---

**2. Spread Operator**  
The spread operator is used to split an array or object into individual elements. 🌀 Its syntax is also `...`, but it expands an existing array or object.

```javascript
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5, 6];

console.log(arr2); // Output: [1, 2, 3, 4, 5, 6]
```

🛠️ **Explanation:**  
Here, `...arr1` splits the array elements and adds them to `arr2`. ⚡️🔧

---

### **Short Definition** 📚  
- **Rest Operator**: Combines multiple values into an array. 
- **Spread Operator**: Expands an array or object into individual elements.
