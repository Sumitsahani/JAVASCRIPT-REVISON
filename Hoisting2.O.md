
# **Hoisting in JavaScript**

**Hoisting** ek JavaScript ka concept hai jisme variables aur functions ko unke actual execution se pehle memory m allocate kiya jaata hai. 🧠

Iska matlab, aap koi variable ya function ko usse pehle bhi use kar sakte ho, jab wo code mein declare nahi hua hota. 💡

### 🕐 **Real-time Example**:
```javascript
console.log(name);  // Output: undefined
var name = "Sumit";
```
👀 Is example mein aap dekhoge ki humne `name` variable ko declare karne se pehle hi `console.log` ke through use kiya hai. Output `undefined` aaya, error nahi aaya. 

Yeh hoisting ki wajah se hota hai. JavaScript internally yeh kaam karti hai:

```javascript
var name;
console.log(name);  // Output: undefined
name = "Sumit";
```

📝 **Explanation**: JavaScript ne `name` ko memory mein pehle hi reserve kar liya tha, lekin jab tak value assign nahi hui, tab tak uska value `undefined` hota hai.

---

### 📞 **Function Hoisting**:
```javascript
greet(); // Output: Hello Sumit! 👋

function greet() {
    console.log("Hello Sumit!");
}
```

🔧 Humne `greet` function ko call karne se pehle define nahi kiya, lekin fir bhi JavaScript ne isko execute kar diya kyunki functions bhi hoist hote hain. 🛠️ Function declaration hoisting mein pura function memory mein pehle load ho jaata hai.

---

## 🔍 **Definition**:
Hoisting ka matlab hota hai ki variables aur function declarations ko code ke execution se pehle memory mein lift kar diya jaata hai. 🏗️ Variables ke liye `undefined` assign hota hai jab tak unhe koi value nahi milti, lekin functions puri tarah memory mein store ho jaate hain. 🤓

---

# 🚀 **Hoisting in JavaScript** (English)

**Hoisting** is a concept in JavaScript where variables and functions are allocated memory before the actual code execution. 🧠

This means you can use a variable or function even before it's declared in the code. 💡

### 🕐 **Real-time Example**:
```javascript
console.log(name);  // Output: undefined
var name = "Sumit";
```
👀 In this example, we are using the `name` variable before declaring it using `console.log`. The output is `undefined`, not an error.

This happens because of hoisting. JavaScript internally does this:

```javascript
var name;
console.log(name);  // Output: undefined
name = "Sumit";
```

📝 **Explanation**: JavaScript reserves memory for the `name` variable beforehand, but until a value is assigned, it holds `undefined`.

---

### 📞 **Function Hoisting**:
```javascript
greet(); // Output: Hello Sumit! 👋

function greet() {
    console.log("Hello Sumit!");
}
```

🔧 We called the `greet` function before defining it, but JavaScript still executed it because functions are hoisted. 🛠️ In function declaration hoisting, the entire function is loaded into memory.

---

## 🔍 **Definition**:
Hoisting means that variable and function declarations are lifted to the top of their scope before code execution. 🏗️ Variables are assigned `undefined` until they are given a value, while functions are fully stored in memory. 🤓