# 🤔 Undefined vs Not Defined

#### ❓ Undefined:
Jab hum JavaScript me koi variable declare karte hain lekin usko koi value assign nahi karte, toh wo `undefined` hota hai. Iska matlab hai ki variable ban gaya hai, par uski koi value abhi tak nahi hai.

**Example:**

```javascript
let name;
console.log(name); // Output: undefined
```

Yaha `name` variable ko declare kiya gaya hai par usme koi value nahi di gayi, isliye output `undefined` aayega.

#### ❌ Not Defined:
Jab hum JavaScript me koi aisa variable use karte hain jo exist hi nahi karta, toh JavaScript usko `not defined` kehti hai. Iska matlab hai ki aapne kabhi bhi ye variable declare nahi kiya.

**Example:**

```javascript
console.log(age); // ReferenceError: age is not defined
```

Yaha `age` variable kabhi declare nahi hua, isliye JavaScript error degi aur kahegi ki `age is not defined`.

**Short Definition:**
- **Undefined:** ✨ Variable declare ho gaya hai, par usko koi value nahi mili.
- **Not Defined:** 🚫 Variable kabhi declare hi nahi hua.

---

### English Explanation:

#### ❓ Undefined:
In JavaScript, when we declare a variable but do not assign any value to it, it is considered `undefined`. This means the variable exists, but it has no value assigned yet.

**Example:**

```javascript
let name;
console.log(name); // Output: undefined
```

Here, the variable `name` is declared but hasn't been assigned a value, so the output will be `undefined`.

#### ❌ Not Defined:
When we try to use a variable in JavaScript that hasn't been declared, it is called `not defined`. This means the variable doesn't exist in the current context.

**Example:**

```javascript
console.log(age); // ReferenceError: age is not defined
```

In this case, the variable `age` has never been declared, so JavaScript throws an error saying `age is not defined`.

**Short Definition:**
- **Undefined:** ✨ The variable is declared but not assigned a value.
- **Not Defined:** 🚫 The variable is not declared at all.
