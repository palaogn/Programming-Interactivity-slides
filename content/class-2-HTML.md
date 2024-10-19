# Class 2

HTML foundation

Programming Interactivity

 ----

Harbour Space

---

## Agenda
<!-- .slide: text-align="left" -->
01/ What is HTML?

02/ Basic HTML structure

03/ Common HTML Tags and Elements

04/ Attributes and nesting

05/ Links, Images and Multimedia

06/ Forms and User Interaction

07/ Best Practises for HTML

////

02/ Semantics

03/ HTML Elements

04/ Images

---

## 01/ What is HTML?

---

## 02/ Basic HTML structure

---

## 03/ Common HTML Tags and Elements

---

## 04/ Attributes and nesting

---

## 05/ Links, Images and Multimedia

---

## 06/ Forms and User Interaction

---

## 07/ Best Practises for HTML

---

## Excercise 1

---

## 01/ HTML Intro

---

### About

HTML (HyperText Markup Language) is the most basic building block of the Web.


It defines te maning and structure of web content.

---

#@ Basic HTML example

``` html
<!DOCTYPE html>
<html>
<head>
    <title>My First Web Page</title>
</head>
<body>
    <h1>Hello, World!</h1>
    <p>This is my first web page.</p>
</body>
</html>
```

---

## HTML is not a programming language. It's a markup language.

---

## Roles

***HTML*** - What it says

***CSS*** - How it looks

***Javascript*** - How it behaves

---

## 02/ Semantics

---

## What are semantics?
 The maning of elements

 Most HTML elements clearly define their contents. Other elements are non-semantic.

---

### Semantic elements
``` hmtl
<header>, <footer>, <nan>, <article>, <section>, 
<h1>, <h2>, <h3>, <p>, <a>, <form>, <inout>, <img>
... more
```

### Non-semantic
``` html
<div>
<span>
```

---

## 03/ Basic HTML

---

## Why semantics matter?

Tells search engines the meaning and importance of elements (SEO)

Tells browsers and screen readers about meaning for accessibility.

Tells developers the purpose of the content. It's more professional!

---

## Web Crawlers

---

## Google

---

## Search engine ranking

Popularity - You get traffic when other established sites link to your site and by how people interact.

#### Content
The copywriting and images on your site.

#### Technical
The semantics on your site.

#### Design and experience
This is becoming even more important.

---

## Bottom line - Semantics on your side matter


--- 

## 03/ HTML Elements

---

## Headings

....

---

## Paragraph

...

---

## Anchor

...

---

## Image

...

---

## Header, Nav, Main, Aside, Footer

...

---

## Article

...

---

## Division

...

---

## Forms

``` html [1-13|1|3|4|11|1-13]
<form> 
    <div>
     <label for="name">Name</label>
     <input id="name" name="name" type="text" />
    </div>
  <div>
    <label for="email">Email:</label>
    <input id="email" name="email" type="email"/> 
  </div>
  <div>
    <input type="submit" />
  </div>
</form>
```

---

## HTML Elements - There are many, many more...

---

## 04/ Images

---

### Image

...

---

#### JPG
- Bitmap image format
- Fit well for "real" multi-color images.

#### SVG
- Vector format (scales well).
- Fit well for logos and illustrations.

#### PNG
- Bitmap image format.
- Files for images with few colors.
- Allows transparent backgrounds.

---

### SVG
``` html

```

---

### Inline SVG

``` html
<div class="wrapper">
 <svg width="300" height="200">
   <polygon points="100,10 40,198 190,78 10,78
     160,198" style="fill:lime;stroke:purple;
     stroke-width:5;fill-rule:evenodd;" />
 </svg>
</div>
```



