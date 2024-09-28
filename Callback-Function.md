### JavaScript ``Callbacks`` in with Real-Life Example 🤔💻

---
**Example:** 📝

Socho tumhe ek website pe login karna hai. Jab tum login karte ho, to server ko request bhejte ho, right? Server ko thoda time lagta hai response dene mein, but tab tak tumhe wait nahi karna padta. Tum request bhejne ke saath ek function dete ho jo kehta hai, "jab server response de de, tab is function ko call kar dena." ⏳📡

```javascript
function loginUser(email, password, callback) {
  console.log("Login request bheja ja raha hai..."); 😎
  
  setTimeout(() => {
    console.log("Login successful for", email); 🎉
    callback(); 
  }, 2000); // Assume yeh time lagta hai server ko response dene mein ⏲️
}

function showWelcomeMessage() {
  console.log("Welcome! Tum login ho chuke ho."); 👏
}

loginUser("sumit@example.com", "password123", showWelcomeMessage);
```

Is example mein, `showWelcomeMessage` ek callback function hai jo login hone ke baad execute hota hai. 🏁💬
## Definition

JavaScript mein **callback function** ek aisa function hota hai jo kisi doosre function ko argument ke roop mein diya jata hai aur us doosre function ke kaam khatam hone ke baad call hota hai. 🤓

---

## English Explanation

**Example:** 📝

Imagine you are logging into a website. When you log in, you send a request to the server, right? It takes some time for the server to respond, but you don’t have to wait around. You give a function along with the request, saying, “When the server responds, call this function.” ⏳📡

```javascript
function loginUser(email, password, callback) {
  console.log("Sending login request..."); 😎
  
  setTimeout(() => {
    console.log("Login successful for", email); 🎉
    callback();
  }, 2000); // Simulates server response time ⏲️
}

function showWelcomeMessage() {
  console.log("Welcome! You are now logged in."); 👏
}

loginUser("sumit@example.com", "password123", showWelcomeMessage);
```

In this example, `showWelcomeMessage` is a callback function that gets executed after the login process is completed. 🏁💬

## Defination

In JavaScript, a **callback function** is a function that is passed as an argument to another function and is called after that other function has completed its task. 🧐