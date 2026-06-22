# Animations in JavaScript

## 1. Introduction

Animation is the process of creating movement or visual effects on web pages by continuously changing the properties of HTML elements over a period of time.

JavaScript provides several ways to create animations:

1. CSS Animations
2. JavaScript Animation Libraries
3. requestAnimationFrame()
4. setInterval() and setTimeout()

Animations are widely used to create:

* Sliding menus
* Loading indicators
* Moving objects
* Image sliders
* Interactive games
* Modern UI effects

---

# 2. CSS Animations

CSS animations allow developers to animate HTML elements without writing JavaScript.

### Example

```html
<style>

@keyframes slideIn {

    from{
        transform: translateX(-100%);
    }

    to{
        transform: translateX(0);
    }

}

.animated{

    animation: slideIn 1s ease-in-out;

}

</style>

<div class="animated">
    This is an animated element.
</div>
```

### Explanation

`@keyframes`

Defines animation stages.

```css
from
```

Starting position.

```css
to
```

Ending position.

```css
animation
```

Applies the animation to the element.

---

# Output

The element moves smoothly from the left side to its original position.

---

# 3. JavaScript Animation Libraries

JavaScript libraries simplify animation development.

Popular Libraries:

1. GSAP (GreenSock)
2. Anime.js
3. Velocity.js

Example using GSAP:

```javascript
gsap.to(".animated",
{
    duration:1,
    x:100,
    ease:"power1.inOut"
});
```

### Explanation

* duration → Animation duration
* x → Move horizontally by 100px
* ease → Controls speed curve

---

# 4. requestAnimationFrame()

`requestAnimationFrame()` is a built-in browser method used for smooth animations.

It synchronizes animation with the browser refresh rate.

---

### Syntax

```javascript
requestAnimationFrame(functionName)
```

---

### Example

```javascript
function animate(){

    const element =
    document.querySelector(".animated");

    let position = 0;

    function frame(){

        position++;

        element.style.transform =
        `translateX(${position}px)`;

        if(position < 100){

            requestAnimationFrame(frame);

        }

    }

    requestAnimationFrame(frame);

}

animate();
```

---

### Explanation

Step 1:

```javascript
let position = 0;
```

Stores current position.

---

Step 2:

```javascript
position++;
```

Increases position.

---

Step 3:

```javascript
element.style.transform
```

Moves the element.

---

Step 4:

```javascript
requestAnimationFrame(frame)
```

Requests the browser to render the next frame.

---

# Output

The element moves smoothly from left to right.

---

# 5. Animation using setInterval()

JavaScript also allows animations using:

```javascript
setInterval()
```

This repeatedly executes a function after a fixed interval.

---

## Syntax

```javascript
setInterval(function, milliseconds)
```

Example:

```javascript
setInterval(fun,1000)
```

Calls:

```javascript
fun()
```

Every:

```text
1000 milliseconds
=
1 second
```

---

# Complete Program

```html
<!DOCTYPE html>

<html>

<head>

<title>Animation</title>

<style>

#box{

    background-color:gray;

    width:350px;

    height:350px;

    position:relative;

}

#circle{

    background-color:yellowgreen;

    width:50px;

    height:50px;

    border-radius:40%;

    position:absolute;

}

</style>

</head>

<body>

<h1>Animation</h1>

<button onclick="ani()">

Click

</button>

<div id="box">

<div id="circle"></div>

</div>

<script>

function ani(){

var c =
document.getElementById("circle");

var c1 = 0;

var id =

setInterval(Animate,5);

function Animate(){

if(c1 == 300){

clearInterval(id);

}

else{

c1++;

c.style.top = c1 + "px";

c.style.left = c1 + "px";

}

}

}

</script>

</body>

</html>
```

---

# Step-by-Step Explanation

## Step 1

```javascript
function ani()
```

Creates an animation function.

This function runs when:

```html
<button onclick="ani()">
```

is clicked.

---

## Step 2

```javascript
var c =
document.getElementById("circle");
```

Selects:

```html
<div id="circle">
```

from HTML.

---

## Step 3

```javascript
var c1 = 0;
```

Stores the current position.

Initially:

```text
c1 = 0
```

---

## Step 4

```javascript
setInterval(Animate,5);
```

Calls:

```javascript
Animate()
```

every:

```text
5 milliseconds
```

---

## Step 5

```javascript
if(c1 == 300)
```

Checks whether the circle reaches:

```text
300 pixels
```

---

## Step 6

```javascript
clearInterval(id)
```

Stops the animation.

---

## Step 7

```javascript
c1++;
```

Increases the position.

Example:

```text
0

1

2

3

4

.....

300
```

---

## Step 8

```javascript
c.style.top =
c1 + "px";
```

Moves vertically.

---

## Step 9

```javascript
c.style.left =
c1 + "px";
```

Moves horizontally.

---

## Combined Effect

```text
(0,0)

↓

(50,50)

↓

(100,100)

↓

(150,150)

↓

(300,300)
```

The circle moves diagonally.

---

# Understanding clearInterval()

### Syntax

```javascript
clearInterval(id)
```

Purpose:

Stops the timer created by:

```javascript
setInterval()
```

Example:

```javascript
var id =

setInterval(fun,1000);

clearInterval(id);
```

The timer stops immediately.

---

# DOM Methods Used

### getElementById()

```javascript
document.getElementById("circle")
```

Returns:

```text
HTML element object
```

---

### style.top

Moves an element vertically.

Example:

```javascript
element.style.top="100px"
```

---

### style.left

Moves an element horizontally.

Example:

```javascript
element.style.left="100px"
```

---

# Position Property

Two CSS properties are important here:

### position: relative

```css
#box{

position:relative;

}
```

Creates a reference container.

---

### position: absolute

```css
#circle{

position:absolute;

}
```

Allows the circle to move inside the box.

---

# Output

When the page loads:

```text
+----------------------+

      Yellow Circle

+----------------------+
```

When user clicks:

```text
Button Click

↓

Circle moves

↘

Diagonally

↓

Stops at

(300px,300px)
```

---

# Interview Questions

### Q1. What is Animation in JavaScript?

**Answer:**

Animation is the process of changing an element's properties continuously to create movement or visual effects.

---

### Q2. Which methods are used for animation?

**Answer:**

1. CSS Animation
2. requestAnimationFrame()
3. setInterval()
4. setTimeout()
5. Animation Libraries

---

### Q3. What is requestAnimationFrame()?

**Answer:**

It requests the browser to execute an animation before the next repaint for smoother animations.

---

### Q4. What is setInterval()?

**Answer:**

It repeatedly executes a function after a fixed time interval.

Syntax:

```javascript
setInterval(function,milliseconds)
```

---

### Q5. What is clearInterval()?

**Answer:**

It stops the timer created using:

```javascript
setInterval()
```

---

### Q6. Why is position:absolute used?

**Answer:**

It allows the element to move freely inside its parent container.

---

### Q7. Which DOM method is used to access an HTML element?

**Answer:**

```javascript
document.getElementById()
```

---

### Q8. Which properties move an element?

**Answer:**

```javascript
style.top

style.left
```

---

# Important Points

1. Animations create visual movement.
2. CSS animations are simple and fast.
3. requestAnimationFrame() provides smooth animations.
4. setInterval() repeatedly executes functions.
5. clearInterval() stops animations.
6. position:absolute is used for movable elements.
7. style.top changes vertical position.
8. style.left changes horizontal position.

---

# Summary

Animations in JavaScript make web applications interactive and visually appealing. Developers can create animations using CSS, JavaScript libraries, requestAnimationFrame(), or timer functions like setInterval(). The combination of DOM manipulation and animation techniques enables developers to build modern user interfaces, games, loaders, sliders, and dynamic web applications efficiently.
