## ``Event Bubbling`` and  ``Event Capturing`` In Javascript
**Event Bubbling aur Event Capturing** JavaScript mein events ko handle karne ke do tareeke hote hain. Jab tum DOM ke kisi element pe event (jaise click) lagate ho, to ye decide karta hai ki event ka propagation kaise hoga. Chaliye dono concepts ko detail mein samjhte hain, aur diagram ke saath explain karte hain.

---

### 1. **Event Bubbling**

Event bubbling mein, jab ek event fire hota hai, sabse pehle wo target element (jis element pe event laga hai) par fire hota hai, aur phir wo outer elements tak bubble karta hai. Yani andar se bahar tak propagate hota hai.

#### Diagram:

```html
<html>
  <body>
    <div id="outerDiv">
      <button id="innerButton">Click me</button>
    </div>
  </body>
</html>
```

Agar tum `<button>` pe click karte ho to event pehle button pe chalega, fir div, body aur html tak bubble hoke pohchega.

#### Bubbling mein event flow kuch is tarah hota hai:

```
Button (target) → Div (parent) → Body → Html
```

**Example Code:**

```html
<div id="outerDiv">
  <button id="innerButton">Click me</button>
</div>

<script>
  document.getElementById("outerDiv").addEventListener("click", function () {
    alert("Div clicked");
  });

  document.getElementById("innerButton").addEventListener("click", function () {
    alert("Button clicked");
  });
</script>
```

**Explanation**: 
Jab tum `<button>` ko click karoge, pehle "Button clicked" alert show hoga, kyunki event sabse pehle button par fire hoga, phir bubble hokar parent element `div` par jayega aur alert "Div clicked" aayega.

---

### 2. **Event Capturing (Trickling)**

Event capturing mein, event sabse outer element (html ya body) se shuru hota hai aur andar wale target element tak trickle karta hai. Matlab, sabse pehle event parent elements pe trigger hota hai, phir target element pe.

#### Diagram:

```html
<html>
  <body>
    <div id="outerDiv">
      <button id="innerButton">Click me</button>
    </div>
  </body>
</html>
```

Is example mein agar tum `<button>` pe click karte ho, event pehle html, body, div, aur phir button tak propagate hoke pohchega.

#### Capturing mein event flow:

```
Html (outermost) → Body → Div → Button (target)
```

**Example Code:**

```html
<div id="outerDiv">
  <button id="innerButton">Click me</button>
</div>

<script>
  document.getElementById("outerDiv").addEventListener(
    "click",
    function () {
      alert("Div clicked");
    },
    true // 'true' capturing mode enable karta hai
  );

  document.getElementById("innerButton").addEventListener("click", function () {
    alert("Button clicked");
  });
</script>
```

**Explanation**: 
Jab tum `<button>` pe click karoge, event pehle outermost element (`div`) pe trigger hoga, phir target element (`button`) par. Isme "Div clicked" alert pehle aayega, phir "Button clicked".

---

### **English Explanation:**

**Event Bubbling and Event Capturing** are two ways in JavaScript to control how an event propagates through the DOM when it is triggered on an element. Let's explain both in detail with diagrams.

---

### 1. **Event Bubbling**

In **event bubbling**, the event starts at the innermost element (target) and then bubbles up through its parent elements until it reaches the root of the DOM tree (usually the `<html>` element).

#### Diagram:

```html
<html>
  <body>
    <div id="outerDiv">
      <button id="innerButton">Click me</button>
    </div>
  </body>
</html>
```

If you click on the `<button>`, the event will first be triggered on the button, then bubble up to the div, then to the body, and finally to the html element.

#### Bubbling Event Flow:

```
Button (target) → Div (parent) → Body → Html
```

**Example Code:**

```html
<div id="outerDiv">
  <button id="innerButton">Click me</button>
</div>

<script>
  document.getElementById("outerDiv").addEventListener("click", function () {
    alert("Div clicked");
  });

  document.getElementById("innerButton").addEventListener("click", function () {
    alert("Button clicked");
  });
</script>
```

**Explanation**: 
When you click the `<button>`, the "Button clicked" alert will fire first because the event starts at the button (target). Then, the event bubbles up to the parent `div`, showing the "Div clicked" alert.

---

### 2. **Event Capturing (Trickling)**

In **event capturing**, the event starts from the outermost ancestor (like `<html>`) and propagates inward towards the target element. This means the parent elements receive the event first, and finally, the target element receives it.

#### Diagram:

```html
<html>
  <body>
    <div id="outerDiv">
      <button id="innerButton">Click me</button>
    </div>
  </body>
</html>
```

In this example, if you click the `<button>`, the event will start at the outermost element (html) and move inward to the button.

#### Capturing Event Flow:

```
Html (outermost) → Body → Div → Button (target)
```

**Example Code:**

```html
<div id="outerDiv">
  <button id="innerButton">Click me</button>
</div>

<script>
  document.getElementById("outerDiv").addEventListener(
    "click",
    function () {
      alert("Div clicked");
    },
    true // 'true' enables capturing mode
  );

  document.getElementById("innerButton").addEventListener("click", function () {
    alert("Button clicked");
  });
</script>
```

**Explanation**: 
When you click the `<button>`, the event is captured first by the parent elements (div), so the "Div clicked" alert fires first. Then, the event reaches the target button, showing the "Button clicked" alert.

---

### Summary with Diagrams:

#### **Event Bubbling** (Default behavior):

- **Flow**: Starts at the innermost element and bubbles outward.
  
```
Button → Div → Body → Html
```

#### **Event Capturing** (If enabled):

- **Flow**: Starts at the outermost element and trickles inward.
  
```
Html → Body → Div → Button
```

In **event bubbling**, the event moves from **target** to **outer** elements, whereas in **event capturing**, the event flows from **outer** elements to the **target** element.
