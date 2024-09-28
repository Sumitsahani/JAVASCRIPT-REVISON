
# `call` | `apply` | `bind` in JavaScript

Hey there! 👋 Welcome to the magical world of **`call`**, **`apply`**, and **`bind`**! 🪄 These methods let you control how functions behave with different objects. Let's explore them with fun examples! 😄

---

#### 1️⃣ **`call` Method** 📞:

Socho ki tumhare pass ek function hai jo kisi ka naam aur uska kaam bata raha hai. Jaise ki:

```javascript
function introduce(role) {
  console.log(`Hi, mera naam ${this.name} hai aur main ${role} hoon.`);
}
```

Aur ek object hai:

```javascript
const person = {
  name: 'Sumit'
};
```

Ab agar tumhe ye function `introduce` call karna hai `person` object ke saath, toh `call` use karo:

```javascript
introduce.call(person, 'Developer');
```

Output 🖨:
```
Hi, mera naam Sumit hai aur main Developer hoon.
```

🚀 **`call`** se tum kisi function ko ek specific object ke saath turant run karwa sakte ho!

---

#### 2️⃣ **`apply` Method** 📱:

`apply` method bhi same hi kaam karta hai jaise `call`, bas difference yeh hai ki yeh arguments array 🧺 mein leta hai:

```javascript
introduce.apply(person, ['Front-End Developer']);
```

Output 🖨:
```
Hi, mera naam Sumit hai aur main Front-End Developer hoon.
```

🚀 **`apply`** bhi function ko run karta hai, bas arguments array 🧺 mein pass karne hote hain.

---

#### 3️⃣ **`bind` Method** 🛠:

**`bind`** thoda alag hai. Yeh function ko immediately run nahi karta, balki ek naya function banaata hai, jo baad mein call ho sakta hai:

```javascript
const introduceDeveloper = introduce.bind(person, 'Full-Stack Developer');
introduceDeveloper();
```

Output 🖨:
```
Hi, mera naam Sumit hai aur main Full-Stack Developer hoon.
```

🚀 **`bind`** ek naya function return karta hai jo specific `this` value ke saath bind hota hai!

---

### 🌟 English Explanation

---

#### 1️⃣ **`call` Method** 📞:

Imagine you have a function that introduces a person with their name and role:

```javascript
function introduce(role) {
  console.log(`Hi, my name is ${this.name} and I am a ${role}.`);
}
```

And an object:

```javascript
const person = {
  name: 'Sumit'
};
```

Now, you can use the `call` method to execute the `introduce` function with the `person` object:

```javascript
introduce.call(person, 'Developer');
```

Output 🖨:
```
Hi, my name is Sumit and I am a Developer.
```

🚀 **`call`** immediately invokes the function with a specific object.

---

#### 2️⃣ **`apply` Method** 📱:

The `apply` method works just like `call`, but it passes arguments as an array 🧺:

```javascript
introduce.apply(person, ['Front-End Developer']);
```

Output 🖨:
```
Hi, my name is Sumit and I am a Front-End Developer.
```

🚀 **`apply`** invokes the function, but with an array of arguments.

---

#### 3️⃣ **`bind` Method** 🛠:

The `bind` method is different because it returns a new function instead of calling it immediately:

```javascript
const introduceDeveloper = introduce.bind(person, 'Full-Stack Developer');
introduceDeveloper();
```

Output 🖨:
```
Hi, my name is Sumit and I am a Full-Stack Developer.
```

🚀 **`bind`** creates a new function that can be called later with a specific `this` value.

---

### 📌 One-liner Summary

1. **`call`** 📞: Executes the function immediately with a specific object.
2. **`apply`** 📱: Similar to `call`, but takes arguments as an array 🧺.
3. **`bind`** 🛠: Creates a new function that can be called later with a specific object.
