# Class 10

Week 2 Project

Programming Interactivity

 ----

Harbour Space

---

## 


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