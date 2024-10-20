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

## TIP - Class selectors are the most common. Use element selector when possible

---

## TIP - Avoid ID selectors as they're not reusable within a page. IDs also serve a functional purpose.

---

## Combining selectors

How it's possible to combone selectors.

---

## Combining selectors

```
/* style multiple elements at once */
h1,
h2,
h3,
h4 {
    color: blue;
}
```

---

## Psaudo classes

Providing different states for elements

---

## Pseudo classes (on links)

```
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

```
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

---

## Specificity

The selector with highest specificity wins.

1. ID selector (#id_name)
2. Class selector (.class_name)
3. Element selector (body)

---

## Specificity [1-9,3-5]

```
<h1 id=“id” class=“title”>Heading 1</h1>

.title { 
    color: red; 
}
        
h1 { 
    color: blue; 
}
```

---

## Inheritance

CSS property values set on parent elements are inherited by their child elements, and some aren't.

---

## Inheritance

```
body {
    color: blue;
}

span {
    color: black;
}

<p>As the body has been set to have a color of blue this is inherited through the descendants.</p>

<p>We can change the color by targetting the element with a selector, such as this <span>span</span>.</p>
```

---

# Basic styling

---

## Colors

---

... image

---

## Named colors

```
h1 {
    color: hotpink;
}
```

... gif of all color names

---

## HEX colors

```
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

## Pixels

```
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

```
div {
  width: 50%;
  height: 50%;
}
```

Relative to the size of the container

---

## Typography

---

## Font family

---

## Font family

Specifies the font.

Includes fallback fonts in order after comma.

See common font families

Custom fonts are outside of th escope of this course, but you're free to dive into it by yourself.

Google fonts is an example library of free custom fonts.

---

## Font family

```
h1 {
  font-family: Times New Roman, Georgia, serif;
  font-size: 20px;
}
```

---

## Font size


---

## Font size

```
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

```
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

```
body {
	line-height: 1.5;
}
```

---

## Set defaults on body

```
body {
	font-family: georgia, sans-serif;
	font-size: 18px; // normal for <p>
}
```

---

## Backgrounds

---

## Background color

```
div {
  background-color: hotpink;
}
```

---

## Background image

```
div {
  background-image: url('/myimage.jpg');
}
```

---

## Box model

---

## Box Model

![Box model](attachment/box_model.png)

---

## Box Model Example

```
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

```
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

```
div {  /* all sides */
  margin: 20px;
}

div {
  margin: 20px auto;   /* top/bottom left/right */
}

div {
  margin: 20px 30px 20px 30px;   /* top, right, bottom, left */
}
```

---

## inline, inline-block, block

---

## Inline

```
p {
    display: inline;
}
```

Adjusts to size of text

Does not break into new line

---

## inline-block

```
div {
    display: inline-block;
}
```

Allows to set width and height.

Does not break into new line.

---

## block

```
div {
    display: block;
}
```

Allows to set width and height

Breaks int oa new line

---

## Recommended Defaults

```
* {
	margin: 0;
	padding: 0;
  box-sizing: border-box;
}
```

---

## Excercise