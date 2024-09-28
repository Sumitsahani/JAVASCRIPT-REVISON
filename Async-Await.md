
# `async` & `await` in JavaScript 

### **Example**

Imagine karo tumne online food order kiya hai. 🍕 Tum order place karte ho (`async function`), fir tumhe wait karna padta hai jab tak food prepare nahi hota (`await`). 🍽️ Jab tak food ready hota hai, tum doosri cheezein kar sakte ho, lekin khana tab tak nahi milega jab tak wo prepare nahi hota (`await`). 😋

#### 🍔 **Code Example:**

```javascript
async function placeOrder() {
    console.log('🍕 Order placed!');
    let orderStatus = await prepareFood();
    console.log(orderStatus);
}

function prepareFood() {
    return new Promise((resolve) => {
        setTimeout(() => {
            resolve('🍽️ Food is ready!');
        }, 3000); // Food banne mein 3 second lagte hain ⏳
    });
}

placeOrder();
console.log('🕺 Doing other things while waiting...');
```

Is code mein tumne pehle order place kiya 🛒, fir tumne food banne ka wait kiya (`await`) ⏳, aur jab food ready ho gaya toh print ho gaya "🍽️ Food is ready!". Jab tak food ban raha tha, tum doosre kaam kar rahe the! 💻

### **Short Definition**  
`async` aur `await` ka use JavaScript mein promises ko handle karne ke liye hota hai, aur code ko asynchronous banata hai. 🚀  
`async` function ka matlab hai function asynchronous hai, aur `await` ka use hota hai kisi promise ke resolve hone ka wait karne ke liye, bina baaki ke code ko roke hue. ⏳

--- 

### **English Explanation** 

Imagine ordering food online. 🍕 You place the order (`async function`), then wait for the food to be prepared (`await`). 🍽️ While the food is being prepared, you can do other things, but you won’t get the food until it’s ready (`await`). 😋

#### 🍔 **Code Example:**

```javascript
async function placeOrder() {
    console.log('🍕 Order placed!');
    let orderStatus = await prepareFood();
    console.log(orderStatus);
}

function prepareFood() {
    return new Promise((resolve) => {
        setTimeout(() => {
            resolve('🍽️ Food is ready!');
        }, 3000); // It takes 3 seconds to prepare the food ⏳
    });
}

placeOrder();
console.log('🕺 Doing other things while waiting...');
```

In this example, you first place the order 🛒, then you wait for the food to be ready (`await`) ⏳. Once the food is ready, it prints "🍽️ Food is ready!" While the food is being prepared, you can do other tasks! 💻

---
### **Short Definition**    

`async` and `await` are JavaScript keywords that make working with promises easier. `async` tells us the function is asynchronous 🚀, and `await` pauses the function execution until the promise is resolved ⏳.