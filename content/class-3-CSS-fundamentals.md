# Class 3

CSS Fundamentals

Programming Interactivity

 ----

Harbour Space

---

## Agenda

01/ CSS intro

02/ CSS Selectors

03/ CSS Rules

04/ Basic styling

05/ Box model

06/ Excersice

---

## CSS intro

---

## About CSS

***CSS*** stands fir Cascading Style Sheet

***CSS*** describes how HTML elements are to be displayed in screen

***CSS*** can control the layout of multiple web pages all at once

---

## Basic CSS

``` css
body { 
  background-color: black; 
  color: white;
} 

h1 { 
  font-size: 40px;
  text-align: center; 
} 

p { 
  font-family: verdana, sans-serif; 
  font-size: 20px; 
}
```

---

## HTML Reference

``` hmtl
<link rel="stylesheet" href="/styles.css">
```

---

## CSS - Hard to do well

---

# CSS Selectors

---

## Selectors

- Element selector (body)
- Class selector (.class_name)
- ID selector (#id_name)

---

## Element Selector

```
h1 {
    color: blue;
}

<h1>Heading 1</h1>
```

---

## Class selector

```
.caption {
    color: red;
}

<span class="caption">Some text</span>
```

---

## ID selector

```
#about {
    background-color: pink;
}

<section id="about">
  ...
</section>
```

---

## Class selectors are the most common. Use element selector when changing styles to all elements of that type

---

## Only use ID selectors if you have a single element of that type. IDs also serve a functional purpose.

---

### Combining selectors

How it's possible to combone selectors.

---

### Combining selectors

``` css
/* style multiple elements at once */
h1,
h2,
h3,
h4 {
    color: blue;
}
```

Note:
- This is how we can combine selectors

---

### Nested selectors

``` css
/* select h1 elements with .title class */
h1.title {
    color: blue;
}

/* select all anchors under p */
p a {
    color: blue;
}

/* select all direct childs of div */
div > * {
    color: blue;
}

```

---

### TIP for simplicity — 
Avoid nested styles as it makes harder to read and reuse the CSS. Rather put classes on all elements that needs styling. 

---

## Psaudo classes

Providing different states for elements

---

## Pseudo classes (on links)

``` css
/* unvisited link */
a:link {
  color: #FF0000;
}

/* visited link */
a:visited {
  color: #00FF00;
}

/* mouse over link */
a:hover {
  color: #FF00FF;
}

/* selected link */
a:active {
  color: #0000FF;
}

<a href="https://cnn.com">CNN</a>
```

---

## Pseudo classes (on elements)

``` css
/* generic styles */
.item {
  width: 100px;
  height: 100px;
  background-color: hotpink;
}
/* style first element */
.item:first-child {
  background-color: hotpink;
}

/* style last element */
.item:last-child {
  background-color: aqua;
}

<div class="item"></div>
<div class="item"></div>
<div class="item"></div>
<div class="item"></div>
```

---

# CSS Rules

---

## The cascade

The order of CSS rules matter

The one that comes last in the CSS is the one that will be used

---

## The cascade

``` [1-6,4-6]
h1 { 
    color: red; 
}
h1 { 
    color: blue; 
}
```

Note: the later one will be selected

---

## Specificity

The selector with highest specificity wins.

1. ID selector (#id_name)
2. Class selector (.class_name)
3. Element selector (body)

---

## Specificity [1-9,3-5]

``` css
<h1 id=“id” class=“title”>Heading 1</h1>

.title { 
    color: red; 
}
        
h1 { 
    color: blue; 
}
```

Note: .title class will win because that has a higher specification.

---

## Inheritance

CSS property values set on parent elements are inherited by their child elements, and some aren't.

---

## Inheritance

``` css
body {
    color: blue;
}

span {
    color: black;
}

<p>As the body has been set to have a color of blue this is inherited through the descendants.</p>

<p>We can change the color by targetting the element with a selector, such as this <span>span</span></p>
```

---

# Basic styling

---

## Colors

---

<img src="attachment/pixels.png">

---

## Named colors

``` css
h1 {
    color: hotpink;
}
```

<img src="attachment/c1/css-colour-names.png">

---

## HEX colors

``` css
h1 {
    color: #FF69B4;
}
```

---

## RGB/RGBA Colors

```
h1 {
    color: rgb(255, 105, 180);
}
```

---

## Units

---

## Pixels

An absolute unit representing a "dot" on the display

---

<img src="attachment/c2/pixel-single.png">

---

## Pixels

``` css
div {
  width: 400px;
  height: 400px;
}
```
---

## Percentage

A unit relative to the width or height of it's parent container.

---

## Percentage

``` css
div {
  width: 50%;
  height: 50%;
}
```

Note: Relative to the size of the container

---

## Typography

---

## Font family

---

## Font family

<div style="text-align: left;">

- Specifies the font.

- Includes fallback fonts in order after comma.

-See common font families

- Custom fonts are outside of th escope of this course, but you're free to dive into it by yourself.

- Google fonts is an example library of free custom fonts.

---

## Font family

``` css
h1 {
  font-family: Times New Roman, Georgia, serif;
  font-size: 20px;
}
```

---

## Font size


---

## Font size

``` css
h1 {
  font-size: 36px;
}

h2 {
  font-size: 32px;
}

h3 {
  font-size: 26px;
}
```

---

## Font weight

Weights are both numerical and named

Examples:
- 200: light
- 400: normal
- 700P bold

---

## Font weight

``` css
h1 {
  font-size: 36px;
  font-weight: bold;
}

h2 {
  font-size: 32px;
  font-weight: normal;
}

h3 {
  font-size: 26px;
  font-weight: 200; /* Light */
}
```

---

## Type styles

- text-align
- line-height
- line-spacing
- text-transform
- text-decoration
- more ...

---

## Line height

``` css
body {
	line-height: 1.5;
}
```

---

## Set defaults on body

``` css
body {
	font-family: georgia, sans-serif;
	font-size: 18px; // normal for <p>
}
```

Note:
- Default styles you want to use across the whole page can be set to the body tag. 
- As that should surround the whole content of the page.
---

## Backgrounds

---

## Background color

``` css
div {
  background-color: hotpink;
}
```

---

## Background image

``` css
div {
  background-image: url('/myimage.jpg');
}
```

---

## Box model

---

## Box Model

<img src="attachment/box_model.png" />

---

## Box Model Example

``` css
div {
  width: 300px;
  height: 100px;
  border: 20px solid green;
  padding: 20px;
  margin: 20px;
}
```

---

## Long

``` css
div { 
  width: 300px;
  height: 100px;

  border-style: solid;
  border-color: green;  border-top: 20px;  
  border-right: 20px;
  border-bottom: 20px;
  border-left: 20px;  padding-top: 20px;
  padding-right: 20px;
  padding-bottom: 20px;
  padding-left: 20px;

  margin-top: 20px;
  margin-right: 20px;
  margin-bottom: 20px;
  margin-left: 20px;
}
```

---

## Long

![margin](attachment/margin.png)

---

## Short, long, longest

``` css [1-4| ]
div {  
  margin: 20px;
  /* all sides */
}

div {
  margin: 20px auto; 
  /* top/bottom left/right */
}

div {
  margin: 20px 30px 20px 30px;   
  /* top, right, bottom, left */
}
```

---

<img src="attachment/c2/inline-block-block.png">

---

## Recommended Defaults

``` css
* {
	margin: 0;
	padding: 0;
  box-sizing: border-box;
}
```

---

## Excercise