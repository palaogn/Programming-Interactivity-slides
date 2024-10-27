# Class 8

CSS User Interactions

Programming Interactivity

 ----

Harbour Space

---

## Agenda

01/ CSS Transitions

02/ Easing functions

03/ CSS 2D Transforms

04/ CSS Animations

05/ Excercise

---

## 01/ CSS Transitions

---

CSS transitions allows you to change property values smoothly, over a given duration.

---

### CSS Transitions

![alt text](attachment/transition.png)

---

### CSS Transitions

``` javascript
.color {
  transition: background-color 500ms;
  background-color: black;
}

.color:hover {
  background-color: hotpink;
}
```

---

### Fade Transition

``` css
.fade {
  transition: opacity 500ms;
  opacity: 1;
}

.fade:hover {
  opacity: 0.1;
}
```


---

## 02/ Easing functions

---

## Easing functions

Easing functions let you vary the transitions's speed over the course of its duration.

---

### Build-in easing functions

![alt text](attachment/easing-functions.png)

ease is default

---

### Easing

``` css
.width {
  transition: width 3s ease-in-out;
  width: 150px;
}

.width:hover {
  width: 1000px;
}
```

---

### Custom easing functions

![alt text](attachment/custom-easing-functions.png)

easings.net

---

### Custom Easings

``` css
.width {
  transition: width 3s cubic-bezier(0.22, 1, 0.36, 1);
  width: 150px;
}

.width:hover {
  width: 1000px;
}
```

---

## 03/ CSS 2D Transforms

---

### CSS Transforms

CSS transforms allow you to move, rotate, scale, and skew elements.

---

### Translate X Transform

``` css
.translate {
  transition: transform 2s;
}

.translate.active {
  transform: translateX(300px); 
}
```

---

## 04/ CSS Animations

---

### CSS Animations

CSS animations allow you to gradually change elements over a number of keyframes.

---

### Swing animation

``` css
@keyframes animationName {
  0% {
    transform: translateX(0)
  }
  25%  {
    transform: translateX(300%)
  }
  50%  {
    transform: translateX(-300%)
  }
  100% {
    transform: translateX(0)
  }
}

.swing.clicked {
  animation-name: animationName;
  animation-duration: 4s;
}
```

---

### ADditional Properties

``` css
.swing.clicked {
  animation-name: animationName;
  animation-duration: 1s;
  animation-timing-function: ease-in-out;
  
  /* repeat endless amount of times */
  animation-iteration-count: infinite;

  /* delay before start */
  animation-delay: 100ms;

  /* reverse the animation */
  animation-direction: reverse;
}
```

---

## 05/ Excercise