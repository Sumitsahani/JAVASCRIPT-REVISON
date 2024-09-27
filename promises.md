# 🎩✨ Introducing the Promise Trio! 

Welcome to the magical world of JavaScript Promises! 🪄 Join us as we follow the journey of **Promise 1**, **Promise 2**, and **Promise 3**—each with their unique flair and timing. Watch as they try to resolve and see if they all succeed in the end! 🎉

## 🎈 Table of Contents
- [Introduction](#introduction)
- [The Promise Trio](#the-promise-trio)
- [The Big Show](#the-big-show)
- [How Promises Work](#how-promises-work)
- [Conclusion](#conclusion)

## 🎉 Introduction
Promises in JavaScript are like magical contracts—either they keep their promise (resolve) or they break it (reject). Each promise takes time to perform a task, and we can handle the outcomes using `.then()` and `.catch()`.

In this analogy, we have **three promises**: **Promise 1**, **Promise 2**, and **Promise 3**—each one representing a magical performance with its own timing. Let's dive into the show!

## 🎩 The Promise Trio

### Promise 1: 🪄 The Magic Wand
```javascript
let promise1 = new Promise((resolve, reject) => {
    setTimeout(() => {
        const status = true; // The magic wand says true! 🪄
        if (status) {
            resolve("Promise 1: Ta-da! Status code: 200 🎉"); // Success magic! 🥳
        } else {
            reject("Promise 1: Oops! Status code: 404 😱"); // Sad magic fails. 😢
        }
    }, 1000); // Wait for 1 second... the suspense! ⏳
});
```
**Promise 1** takes 1 second to perform its magic trick. If successful, it says, "Ta-da! Status code: 200 🎉". If not, we get a sad "Oops! Status code: 404 😱."

### Promise 2: 💃 The Flashy Performer
```javascript
let promise2 = new Promise((resolve, reject) => {
    setTimeout(() => {
        const status = true; // The spotlight is on! 🌟
        if (status) {
            resolve("Promise 2: Look at me! Status code: 200 🎊"); // Success strut! 💪
        } else {
            reject("Promise 2: Uh-oh! Status code: 404 😬"); // A dramatic fall! 🎭
        }
    }, 1500); // 1.5 seconds for a fabulous entrance! 🎉
});
```
**Promise 2** loves to make a flashy entrance—taking 1.5 seconds to show off! If successful, it struts with "Status code: 200 🎊", but if it falls, it says "Uh-oh! Status code: 404 😬."

### Promise 3: 🐢 The Slowpoke
```javascript
let promise3 = new Promise((resolve, reject) => {
    setTimeout(() => {
        const status = true; // Slow but steady wins the race! 🐌
        if (status) {
            resolve("Promise 3: Finally! Status code: 200 🎈"); // The grand reveal! 🎆
        } else {
            reject("Promise 3: Oh no! Status code: 404 😩"); // The tragic twist! 📉
        }
    }, 2000); // 2 seconds... grab your popcorn! 🍿
});
```
**Promise 3** is slow but steady—it takes 2 full seconds for the grand reveal. If successful, it exclaims "Finally! Status code: 200 🎈", but if it fails, it's a sad "Oh no! Status code: 404 😩."

## 🎭 The Big Show: Can They All Succeed?
Now, let's see if all three promises can succeed together. Using `Promise.all()`, we wait for all the promises to resolve before showing the results:

```javascript
Promise.all([promise1, promise2, promise3])
    .then(results => {
        console.log("🎉 All promises resolved: 🎊");
        results.forEach(result => console.log(result)); // Let’s hear the applause! 👏
    })
    .catch(error => {
        console.error("😱 One or more promises rejected: 😢");
        console.error(error); // The sad ending... boo! 🎭
    });
```

When all the promises succeed, the console will cheer:  
```text
🎉 All promises resolved: 🎊
Promise 1: Ta-da! Status code: 200 🎉
Promise 2: Look at me! Status code: 200 🎊
Promise 3: Finally! Status code: 200 🎈
```

But if any of the promises fail, it will display a sad message:
```text
😱 One or more promises rejected: 😢
```

## 🌟 How Promises Work
1. **Pending**: The promise is in progress and hasn’t completed yet. It’s like waiting for the magic trick to finish.
2. **Resolved (Fulfilled)**: The promise completed successfully, like when the magician pulls a rabbit out of a hat—"Ta-da!" 🎉
3. **Rejected**: The promise failed, like when the trick goes wrong—"Oops!" 😢

When you chain promises with `.then()`, you're saying, "Once this promise is fulfilled, do this next thing." If it fails, `.catch()` handles the rejection, catching any errors or failed promises.

## 📜 Conclusion
In this magical journey, you’ve learned how to work with JavaScript promises:
- **Promise 1**: Quick with its magic trick.
- **Promise 2**: A little more dramatic and flashy.
- **Promise 3**: Slow but steady!

We used `Promise.all()` to wait for all promises to resolve before continuing, and saw how we can handle successes and failures in an elegant way. 🎩✨
