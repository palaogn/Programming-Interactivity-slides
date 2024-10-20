# Class 6

Javascript fundamentals

Programming Interactivity

 ----

Harbour Space

---

## Agenda

01/ Programming foundation

02/ Variables

03/ Data types

04/ Arithmetic operators

05/ Comparison operators

06/ Functions

07/ Excercise

---

## 01/ Programming foundation

---

## Javascript

JavaScript is a text-based programming language used both on the client-side and server-side that allows you to make web pages interactive.

---

## Roles

***HTML***
What it says.

***CSS***
How it looks.

***JAVASCRIPT***
How it behaves.

---

## Hello World

```
const myHeading = document.querySelector('h1');
myHeading.textContent = 'Hello world!';

<h1>Text will show here!</h1>
```

---

## HTML Reference

```
<h1>Text will show here!</h1>
```

---

## JavaScript -
THe most popular programming language in the world.

---

## JavaScript -
The only programming language you can use for the web.

---

## JavaScript -
You can use it to build anything; Web, Native Apps, Web Services.

---

## JavaScript -
Initially written in 10 days to be flexible, simple, dynamic and accessible to non-developers.

---

## Javascript -
Flexibility also makes it complicated, many ways to write.

---

## EcmaScript
... ES6

---

## 02/ Variables

---

## Variables
We have ***var*** - ***const*** and ***let***

---

## Variables

let and const if from ES6(EcmaScript)

---

## Variables

```
let myVariable;
myVariable = ‘Bob';
…
myVariable = 'Siri';
```

---

## Constants

```
const PI;
PI = 3.14159265359;

PI = 100; // NOT POSSIBLE!
```

---

## 03/ Data types

---

## Data types

JavaScript is dynamic in nature, meaning that variables and types are decided as assigned in run-time.


The opposite are type-safe languages that are usually pre-compiled.

---

## Data types

Boolean - Number - String - Object - Array

undefined - null

---

### Boolean

A Boolean represents one of two values: `true` or `false`.

```javascript
let isRaining = false;

if (isRaining) {
    console.log('Take an umbrella!');
} else {
    console.log('No need for an umbrella.');
}
```

---

---
### Number

A Number represents both integer and floating-point numbers.

```javascript
let integerNumber = 42;
let floatingPointNumber = 3.14;

console.log(integerNumber); // Output: 42
console.log(floatingPointNumber); // Output: 3.14
```

---

### String

A String represents a sequence of characters.

```javascript
let greeting = "Hello, world!";
let name = 'Alice';

console.log(greeting); // Output: Hello, world!
console.log(name); // Output: Alice
```

---



### Object

An Object is a collection of properties, and a property is an association between a name (or key) and a value.

```javascript
let person = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
    isEmployed: true,
    }
};

console.log(person.firstName); // Output: John
console.log(person["lastName"]); // Output: Doe
```

---

### Array

An Array is a list-like object that can store multiple values.

```javascript
let fruits = ["Apple", "Banana", "Cherry"];

console.log(fruits[0]); // Output: Apple
console.log(fruits[1]); // Output: Banana
console.log(fruits[2]); // Output: Cherry

fruits.push("Pear");
console.log(fruits[3]) // Output: Pear
```

---

### Checking type

``` javascript
let myVariable = 'Hello!';

typeof myVariable; // Returns "string"
```

---

### Undefined

``` javascript
let myVariable;

typeof myVariable; // Returns undefined
```

### undefined

A variable that has been declared but not assigned a value is of type `undefined`.

```javascript
let myVariable;

console.log(myVariable); // Output: undefined
```

In this example, `myVariable` is declared but not assigned a value, so it is `undefined`.

---

### null

A variable that has been assigned but has no value is set to null.

```javascript
let myVariable = null;

console.log(myVariable); // Output: null
```

In this example, `myVariable` is explicitly set to `null`, indicating the absence of any object value.

---


## 04/ Arithmetic operators

You can also perform arithmetic operations with numbers:

```javascript
let sum = 10 + 5;          // = 15 , Addiiton
let difference = 10 - 5;   // = 5, Subtraction
let product = 10 * 5;      // = 50, Multiplication
let quotient = 10 / 5;     // = 2, Division
```

---

## 05/ Comparison operators

---

### Comparison Operators

Comparison operators are used to compare two values. They return a Boolean value: either `true` or `false`.

```javascript
let a = 5;
let b = 10;

console.log(a == b);  // Equal to, Output: false
console.log(a != b);  // Not equal to, Output: true
console.log(a > b);   // Greater than, Output: false
console.log(a < b);   // Less than, Output: true
console.log(a >= b);  // Greater than or equal to, Output: false
console.log(a <= b);  // Less than or equal to, Output: true
```

---

### Comparison Operators

In addition to these, there are also strict comparison operators that check both value and type:

```javascript
let a = 5;
let c = '5';

console.log(a === c); // Strict equal to, Output: false
console.log(a !== c); // Strict not equal to, Output: true
```

---

## 06/ Functions

---

## Functions

Functions are te first class in JavaScript

Meaning that they can be assigned, can be passed around and used as closures.

---

## Using Functions

``` javascript
'hello'.toUpperCase(); // Returns "HELLO"

[3, 2, 1].reverse(); // Returns "[1,2,3]"

Math.random(); // Random number between 0 and 1
```

---

## Defining Functions

``` javascript
const sayHelloWithName = (name) => {
  return 'Hello ' + name;
}

let name = sayHelloWithName('Pála');
console.log(name); // Hello Pála
```

---

## Functions vs Arrow functions

### Example of Function vs Arrow Function

```javascript
// Arrow Function
const sayHelloWithNameArrow = (name) => {
    return 'Hello ' + name;
}

// Regular Function
function sayHelloWithNameFunction(name) {
    return 'Hello ' + name;
}

let nameArrow = sayHelloWithNameArrow('Pála');
console.log(nameArrow); // Hello Pála

let nameFunction = sayHelloWithNameFunction('Pála');
console.log(nameFunction); // Hello Pála
```

---

## Tip
Make functions single purpose for readable code.

---

## Scope ??

---

## 07/ Excercise





/// Maybe

### String template literal

```javascript
const name = "Alice";
const greeting = `Hello, ${name}`

console.log(greetinr); // Output: Hello, Alice
```

---

### Array operations, filter, map, ...