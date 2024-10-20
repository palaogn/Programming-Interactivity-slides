# Class 7

Javascript and DOM Elements

Programming Interactivity

 ----

Harbour Space

---

## Agenda

01/ DOM elements

02/ Selecting slemets

03/ Loops

04/ Events

05/ Manipulating the DOM

06/ Excercise

----

## 01/ DOM elements

---

### DOM

The DOM stands for Document Object Model

A tree of nodes created by the browser.

Each has its own properties and methods which can be manipulated using Javascript.

Note: The DOM is the data structure representing the content, structure, and style of a document. It allows programs and scripts to dynamically access and update the content, structure, and style of documents.

### Key Points

- **Tree Structure**: The DOM represents a document as a tree of nodes.
- **Node Types**: Elements, attributes, text, etc.
- **Manipulation**: JavaScript can be used to manipulate the DOM to change the document structure, style, and content.

---

![alt text](attachment/DOM-tree.png)

Note: DOM Tree

---

## 02/ Selecting elements

---

## Selecting Elements

Similar to CSS selectore, applied JavaScript.

---

### DOM Selecting methods

To select elements in the DOM, you can use various methods provided by the `document` object. Here are some common methods:

- **`getElementById`**: Selects a single element by its ID.
    ```javascript
    const element = document.getElementById('myId');
    ```

- **`getElementsByClassName`**: Selects all elements with a specific class name.
    ```javascript
    const elements = document.getElementsByClassName('myClass');
    ```

- **`getElementsByTagName`**: Selects all elements with a specific tag name.
    ```javascript
    const elements = document.getElementsByTagName('div');
    ```

- **`querySelector`**: Selects the first element that matches a CSS selector.
    ```javascript
    const element = document.querySelector('.myClass');
    ```

- **`querySelectorAll`**: Selects all elements that match a CSS selector.
    ```javascript
    const elements = document.querySelectorAll('.myClass');
    ```

These methods allow you to access and manipulate DOM elements efficiently.


---

## getElementById

To select an element by its ID, you can use the `getElementById` method. Here is an example:

```javascript
// HTML: <div id="myId">Hello World</div>

// JavaScript:
let element = document.getElementById('myId');
console.log(element.textContent); // Outputs: Hello World
```

This code selects the element with the ID `myId` and logs its text content to the console.


---

## getElementById

To select an element by its ID, you can use the `getElementById` method. Here is an example:

```javascript [1-5, 3-7]
// HTML: <div id="myId"></div>

// JavaScript:
let element = document.getElementById('myId');
element.textContent = "Hello world!";

// HTML: <div id="myId">Hello World</div>
```

This code selects the element with the ID `myId` and logs its text content to the console.

---

## querySelectorAll

``` javascript
let tabs = document.querySelectorAll('.tab');

console.log(tabs.length); // Returns 3

<a href="#tab1" class="tab active">Tab 1</a>
<a href="#tab2" class="tab">Tab 2</a>
<a href="#tab3" class="tab">Tab 3</a>
```

---

## 03/ Loops

---

### Loops

Loops execute a block of code a number of times.

The most used one in JavaScript is the "for" loop.

---

### For loop

``` javascript
for (let i = 0; i < 5; i++) {
  // Runs 5 times  
  console.log('Step number ' + (i+1));
}
```

Note: 

---

### Looping an array

``` javascript
let fruits = ['Orange', 'Apple', ...]

for (let i = 0; i < cars.length; i++) {
  // Runs for each item in the array
  let fruits = fruits[i];
  console.log('The car is ' + car);
}
```

---

### Looping trough elements

``` javascript
let tabs = document.querySelectorAll('.tab')

for (let i = 0; i < tabs.length; i++) {
  let tab = tabs[i];
  tab.innerHTML = 'Tab ' + (i+1);
}
```

---

### Does the same as previous slide

``` javascript
let tabs = document.querySelectorAll('.tab')

let tab1 = tabs[0]
tab1.innerHTML = 'Tab 1'

let tab2 = tabs[1]
tab2.innerHTML = 'Tab 2'

let tab3 = tabs[2]
tab3.innerHTML = 'Tab 3'
```

---


## 04/ Events

---

### Events

JavaScript's events are the way to handle in code when users interact with the site.
Examples:
- Click
- Scroll
- Submit (a form)
- Load (when page loads)


---
### Example event

``` javascript
let button = document.querySelector('.tab');

button.addEventListener('click', onButtonClick);

function onButtonClick () {
  // Do something here
}
```

HTML
``` html
<button href="#tab1" class="tab">Tab 1</button>
```

---

### Preventing default behaviour

``` javascript
let button = document.querySelector('.tab');

button.addEventListener('click', onButtonClick);

function onButtonClick (e) {
  // Do something here
  e.preventDefault();
}
```

HTML
``` html
<button href="#tab1" class="tab">Tab 1</button>
```

---

## 05/ Manipulating the DOM

---

### Manipulating the DOM


Making changes to the HTML through JavaScript.

Examples:
- Adding and removing classes
- Adding and removing elements

---

### Adding a class

``` javascript
tab.classList.add('active');
```
---

### Removing a class

``` javascript
tab.classList.remove('active');
```

---

## 06/ Exercise

