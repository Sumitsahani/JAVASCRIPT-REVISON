# Map, Reduce, and Filter in JavaScript

### `Map`, `Reduce`, and `Filter` in  Real-Life Examples:

#### 1. **Map**:
Jab humko ek list ke sabhi items ko modify karna ho toh `map` function ka use karte hain. Jaise maan lo tum supermarket gaye ho aur tumhari paas ek list hai items ki (e.g. doodh, bread, chips). Tumko price calculate karna hai har item ka 10% discount ke saath.

```js
const items = [100, 200, 150]; // Prices in Rs
const discountedPrices = items.map(item => item * 0.9);
console.log(discountedPrices); // [90, 180, 135]
```

**Real-life Example**:
Supermarket mein tumhne doodh (₹100), bread (₹200), aur chips (₹150) liye. Ab tumko sabka price calculate karna hai 10% discount ke saath. `map` ki madad se har item pe ye discount laga ke naya price milega.

---

#### 2. **Filter**:
`Filter` ka use tab karte hain jab hum kisi list ke items ko filter karna chahte hain based on some condition. Jaise tumhare paas ek list hai fruits ki, aur tumhe sirf wo fruits chahiye jo "a" se start hote hain.

```js
const fruits = ['apple', 'banana', 'mango', 'kiwi'];
const filteredFruits = fruits.filter(fruit => fruit.startsWith('a'));
console.log(filteredFruits); // ['apple']
```

**Real-life Example**:
Socho tum fruit shop gaye ho aur shopkeeper ke paas bahut saare fruits hain. Tumko sirf "a" se start hone wale fruits chahiye, toh tum `filter` use karke sirf "apple" nikal loge.

---

#### 3. **Reduce**:
`Reduce` tab use hota hai jab hum kisi list ke elements ko ek single value mein combine karna chahte hain. Socho tum restaurant gaye ho, aur tumhe total bill calculate karna hai.

```js
const prices = [100, 200, 150];
const totalBill = prices.reduce((total, price) => total + price, 0);
console.log(totalBill); // 450
```

**Real-life Example**:
Tum restaurant mein gaye aur tumne doodh (₹100), bread (₹200), aur chips (₹150) order kiya. Tumhe in sab ka total bill calculate karna hai, toh tum `reduce` use kar ke total ₹450 nikal sakte ho.

---

### Summary:
- `Map`: Tumhari list ke sab items ko modify karta hai. (Jaise 10% discount lagana)
- `Filter`: List me se sirf kuch specific items ko select karta hai. (Jaise "a" se shuru hone wale fruits)
- `Reduce`: List ke sabhi items ka ek combined value deta hai. (Jaise total bill calculation)

Aise real-life example ke through tum `map`, `filter`, aur `reduce` easily samajh sakte ho!

---

# Map, Reduce, and Filter in JavaScript

### `Map`, `Reduce`, and `Filter` in English with Real-Life Examples:

#### 1. **Map**:
When you want to modify all items in a list, you use the `map` function. For example, let’s say you went to the supermarket and you have a list of items (e.g. milk, bread, chips). You want to calculate the price of each item with a 10% discount.

```js
const items = [100, 200, 150]; // Prices in Rs
const discountedPrices = items.map(item => item * 0.9);
console.log(discountedPrices); // [90, 180, 135]
```

**Real-life Example**:
At the supermarket, you bought milk (₹100), bread (₹200), and chips (₹150). Now you want to calculate the price of each item with a 10% discount. Using `map`, you apply this discount to each item and get the new prices.

---

#### 2. **Filter**:
You use `filter` when you want to filter items in a list based on some condition. For example, you have a list of fruits, and you only want the fruits that start with "a".

```js
const fruits = ['apple', 'banana', 'mango', 'kiwi'];
const filteredFruits = fruits.filter(fruit => fruit.startsWith('a'));
console.log(filteredFruits); // ['apple']
```

**Real-life Example**:
Imagine you go to a fruit shop where the shopkeeper has many fruits. You only want the fruits that start with "a", so you use `filter` to get just "apple".

---

#### 3. **Reduce**:
`Reduce` is used when you want to combine elements of a list into a single value. For instance, imagine you went to a restaurant, and you want to calculate the total bill.

```js
const prices = [100, 200, 150];
const totalBill = prices.reduce((total, price) => total + price, 0);
console.log(totalBill); // 450
```

**Real-life Example**:
You went to a restaurant and ordered milk (₹100), bread (₹200), and chips (₹150). To calculate the total bill, you can use `reduce` to get a total of ₹450.

---

### Summary:
- **Map**: Modifies all items in your list. (Like applying a 10% discount)
- **Filter**: Selects only specific items from the list. (Like fruits starting with "a")
- **Reduce**: Provides a combined value of all items in the list. (Like calculating the total bill)

Through these real-life examples, you can easily understand `map`, `filter`, and `reduce`!