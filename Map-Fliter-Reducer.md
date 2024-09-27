# JavaScript `Map`, `Filter`, and `Reduce`

### 1. **Map**:
`map` function ka use tab hota hai jab humko ek list ke sabhi items ko modify karna hota hai. Jaise supermarket ki shopping list ka example lo, tumhare paas items ke prices hain, aur tumhe har item pe 10% discount calculate karna hai.

```js
const items = [100, 200, 150]; // Prices in Rs
const discountedPrices = items.map(item => item * 0.9);
console.log(discountedPrices); // [90, 180, 135]
```

**Example**: 
Supermarket mein doodh (₹100), bread (₹200), aur chips (₹150) ka 10% discount lagao aur naya price nikalo.

---

### 2. **Filter**:
`filter` function ka use tab karte hain jab hume kisi list ke kuch specific items ko chayan karna hota hai based on a condition. Jaise tumhare paas ek list hai fruits ki aur tumhe sirf "a" se shuru hone wale fruits chahiye.

```js
const fruits = ['apple', 'banana', 'mango', 'kiwi'];
const filteredFruits = fruits.filter(fruit => fruit.startsWith('a'));
console.log(filteredFruits); // ['apple']
```

**Example**: 
Fruit shop mein "a" se shuru hone wale fruits chuno, jaise `apple`.

---

### 3. **Reduce**:
`reduce` function ka use tab hota hai jab hum kisi list ke sabhi elements ka ek combined value nikalte hain. Socho tum restaurant mein gaye ho aur total bill calculate karna hai.

```js
const prices = [100, 200, 150];
const totalBill = prices.reduce((total, price) => total + price, 0);
console.log(totalBill); // 450
```

**Example**: 
Doodh (₹100), bread (₹200), aur chips (₹150) ka total ₹450 ban raha hai, toh ye calculation `reduce` karega.

---

### Summary:

- **Map**: Tumhari list ke sab items ko modify karta hai. (Jaise 10% discount lagana)
- **Filter**: List me se sirf kuch specific items ko select karta hai. (Jaise "a" se shuru hone wale fruits)
- **Reduce**: List ke sabhi items ka ek combined value deta hai. (Jaise total bill calculation)

---

### Method Definitions:
- **Map**: A method that creates a new array by applying a given function to each element of the original array.
- **Filter**: A method that creates a new array with elements that pass the condition defined in a given function.
- **Reduce**: A method that reduces an array to a single value by applying a function that accumulates the result of each element.
