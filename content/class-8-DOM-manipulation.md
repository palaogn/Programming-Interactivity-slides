# Class 8

DOM Manipulation

Programming Interactivity

 ----

Harbour Space

---

## Agenda

<div style="text-align: left;">

01/ DOM elements

02/ Selecting elements

04/ Events

05/ Manipulating the DOM

06/ Excercise

---

## 01/ DOM elements

---

### DOM

<div style="text-align: left;">

The DOM stands for Document Object Model

A tree of nodes created by the browser.

Each has its own properties and methods which can be manipulated using Javascript.

</div>

Note: The DOM is the data structure representing the content, structure, and style of a document. It allows programs and scripts to dynamically access and update the content, structure, and style of documents.

### Key Points

- **Tree Structure**: The DOM represents a document as a tree of nodes.
- **Node Types**: Elements, attributes, text, etc.
- **Manipulation**: JavaScript can be used to manipulate the DOM to change the document structure, style, and content.

---

<img src="attachment/DOM-tree.png" width="600px" />

Note: DOM Tree

---
Inspect elements shows live presentation of the DOM

<img src="attachment/c7/inspect-dom.png" />

Note:
- If you go to Inspect in your browser and choose Elements
- Then you are looking at the current DOM of your page
- Its the current state your HTML is technically at, but it will contain everything that is displayed.
- News page for example, will already have all the news page data displayed there.

---

### DOM manipulation

<div style="text-align: left;">

DOM manipulation refers to the process of interacting or modifying the DOM.

- We can create element and append them

- We can add event listeners to listen for actions

- We can add/remove classes and chang styles
</div>

---

## 02/ Selecting elements

---

## Selecting Elements

Similar to CSS selectors as we select by ***id***, ***class*** or html ***tag names***

---

### DOM Selecting methods

To select elements in the DOM, you can use various methods provided by the `document` object. Here are some common methods:

``` js
  // Selects a single element by its ID.
  const element = document.getElementById('myId');
  // Selects all elements with a specific class 
  const elements = document.getElementsByClassName('myClass');
  // Selects all elements with a specific tag name
  const elements = document.getElementsByTagName('div');
  // Selects the first element that matches a CSS selector
  const element = document.querySelector('.myClass');
  // Selects all elements that match a CSS selector
  const elements = document.querySelectorAll('.myClass');
```

---

## get Element By Id

To select an element by its ID, you can use the `getElementById` method.

```javascript
// HTML
<div id="myId">Hello World</div>

// JavaScript:
let element = document.getElementById('myId');
console.log(element.textContent); // Outputs: Hello World
```

This code selects the element with the ID `myId` and logs its text content to the console.


---

## get Element By Class Name

To select all elements with a specified class, you can use the `getElementByClassName` method.

``` js
// HTML: 
<div class="tile"></div>
<div class="tile"></div>

// JavaScript:
let elements = document.getElementByClassName('tile');
```

---

## get Element By Tag Name

To select all elements with a specified tag name, you can use the `getElementByTagName` method.

``` js
// HTML: 
<p class="tile"></p>
<p class="tile"></p>

// JavaScript:
let elements = document.getElementByTagName('p');
```

---

## query Selector

To select an element by a CSS selector, you can use the `querySelector` method. Selects the first element that matches a CSS selector.

``` js
// HTML: 
<div id="myId" class="class-selector"></div>

// JavaScript:
let elementById = document.qerySelector('#myId');
let elementByClass = document.qerySelector('.class-selector');
```

Note:
- querySelector, selects the first element that matches a CSS selector.
- here you can see it with an id and class selector

---

## query Selector All

``` javascript
let tabs = document.querySelectorAll('.tab');

console.log(tabs.length); // Returns 3

<a href="#tab1" class="tab active">Tab 1</a>
<a href="#tab2" class="tab">Tab 2</a>
<a href="#tab3" class="tab">Tab 3</a>
```

---

## 04/ Events

---

### Events

JavaScript's events are the way to handle in code when users interact with the site.

<div style="text-align: left;">

Examples:
- Click
- Scroll
- Submit (a form)
- Mouseover
- Keydown

</div>


---
### Example event

``` js
// HTML
<button href="#tab1" id="tab-button">Tab 1</button>

// JavaScript
let button = document.getElementById('tab-button');

button.addEventListener('click', () => {
  // Do something here
});

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
let button = document.querySelector('.tab');

button.classList.add('active');
```
---

### Removing a class

``` javascript
let button = document.querySelector('.tab');

button.classList.remove('active');
```

---

### Creating an element

``` js
const tile = document.createElement(‘div’);

const container = document.getElementById("container");
container.append(tile);

```
---

### Removing an element

``` js

const container = document.getElementById("container");
container.remove();

```

---

### Change innerText

``` js
const container = document.getElementById("container");
constainer.innerText = "Hello!";
```
---

### Change innerHTML

``` js
const container = document.getElementById("container");
constainer.innerHTML = "<p>Hello!</p>";
```
---

## 06/ Exercise

