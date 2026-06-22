# DOM (Document Object Model) in JavaScript

## 1. Introduction

**DOM** stands for **Document Object Model**.

The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents a web page as a tree-like structure of objects, where every HTML element becomes an object that JavaScript can access and manipulate.

Using the DOM, JavaScript can:

* Change HTML content dynamically.
* Change HTML attributes.
* Modify CSS styles.
* Add new elements.
* Remove existing elements.
* Handle user events dynamically.

---

## 2. Definition

**Definition:**

The Document Object Model (DOM) is a tree representation of an HTML document where each node represents an element, attribute, or piece of text.

The browser automatically creates the DOM when an HTML page is loaded.

---

## 3. Why DOM is Important

DOM is used because it allows JavaScript to:

1. Access HTML elements.
2. Change the content of web pages.
3. Change CSS properties dynamically.
4. Add or delete elements.
5. React to user interactions.
6. Create dynamic and interactive websites.

---

## 4. HTML Example

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title>JS</title>
</head>

<body>

    <p>Hello</p>

    <a href="https://www.kodnest.com">
        Visit KodNest
    </a>

</body>
</html>
```

---

## 5. DOM Tree Structure

The above HTML page is represented internally by the browser as:

```text
Document
   |
   html
   |
   ├── head
   |      |
   |      └── title
   |              |
   |              └── "JS"
   |
   └── body
          |
          ├── p
          |    |
          |    └── "Hello"
          |
          └── a
               |
               ├── href="https://www.kodnest.com"
               |
               └── "Visit KodNest"
```

This structure is called the **DOM Tree**.

---

## 6. Understanding DOM Nodes

The DOM contains different types of nodes.

### 1. Document Node

The entire HTML document.

```text
document
```

---

### 2. Element Node

HTML tags are called Element Nodes.

Examples:

```html
<html>
<head>
<body>
<p>
<a>
```

---

### 3. Attribute Node

Attributes of HTML elements.

Example:

```html
<a href="https://www.kodnest.com">
```

Attribute:

```text
href
```

---

### 4. Text Node

The text inside an element.

Example:

```html
<p>Hello</p>
```

Text Node:

```text
Hello
```

---

## 7. Leaf Nodes

A node that does not have any child nodes is called a **Leaf Node**.

Examples:

```text
"Hello"

"Visit KodNest"

href attribute
```

These are terminal nodes of the DOM Tree.

---

## 8. Accessing DOM Elements

JavaScript provides several methods to access HTML elements.

### getElementById()

Syntax:

```javascript
document.getElementById("id")
```

Example:

```html
<p id="demo">Hello</p>

<script>

document.getElementById("demo").innerHTML =
"Welcome to JavaScript";

</script>
```

Output:

```text
Welcome to JavaScript
```

---

### getElementsByTagName()

Selects elements using tag names.

Example:

```javascript
document.getElementsByTagName("p")
```

Returns:

```text
Collection of paragraph tags
```

---

### getElementsByClassName()

Selects elements by class name.

Example:

```javascript
document.getElementsByClassName("course")
```

---

### querySelector()

Selects the first matching element.

Example:

```javascript
document.querySelector("#demo")
```

---

### querySelectorAll()

Selects all matching elements.

Example:

```javascript
document.querySelectorAll(".course")
```

---

## 9. Changing HTML Content

Example:

```html
<p id="demo">Hello</p>

<script>

document.getElementById("demo").innerHTML =
"Welcome to DOM";

</script>
```

Output:

Before:

```text
Hello
```

After:

```text
Welcome to DOM
```

---

## 10. Changing CSS Styles

Example:

```html
<p id="demo">Hello</p>

<script>

document.getElementById("demo").style.color =
"red";

</script>
```

Output:

```text
Hello
```

Color:

```text
Red
```

---

## 11. Changing Attributes

Example:

```html
<a id="link"
href="https://google.com">

Google

</a>

<script>

document.getElementById("link")
.href =
"https://kodnest.com";

</script>
```

Output:

```text
The link now redirects to:

https://kodnest.com
```

---

## 12. Creating New Elements

Example:

```javascript
var p =
document.createElement("p");

p.innerHTML =
"New Paragraph";

document.body.appendChild(p);
```

Output:

```text
New Paragraph
```

A new paragraph is dynamically created.

---

## 13. Removing Elements

Example:

```javascript
var ele =
document.getElementById("demo");

ele.remove();
```

The element is removed from the webpage.

---

## 14. DOM Properties

| Property  | Purpose               |
| --------- | --------------------- |
| innerHTML | Change HTML content   |
| innerText | Change only text      |
| style     | Modify CSS            |
| value     | Read input values     |
| href      | Get or set link URL   |
| src       | Get or set image path |

---

## 15. DOM Methods

| Method                   | Purpose                |
| ------------------------ | ---------------------- |
| getElementById()         | Select element by ID   |
| getElementsByClassName() | Select by class        |
| getElementsByTagName()   | Select by tag          |
| querySelector()          | First matching element |
| querySelectorAll()       | All matching elements  |
| createElement()          | Create element         |
| appendChild()            | Add element            |
| remove()                 | Delete element         |

---

## 16. Interview Questions

### Q1. What is DOM?

**Answer:**

DOM stands for **Document Object Model**.

It is a tree representation of an HTML document that allows JavaScript to access and manipulate web pages dynamically.

---

### Q2. Who creates the DOM?

**Answer:**

The Browser creates the DOM automatically when the HTML page loads.

---

### Q3. What is a DOM Tree?

**Answer:**

The hierarchical tree representation of HTML elements is called the DOM Tree.

---

### Q4. What is a Leaf Node?

**Answer:**

A node without any child nodes is called a Leaf Node.

Examples:

* Text Nodes
* Attribute Nodes

---

### Q5. Which method selects an element using ID?

**Answer:**

```javascript
document.getElementById("id")
```

---

### Q6. What is innerHTML?

**Answer:**

`innerHTML` is used to read or modify HTML content inside an element.

Example:

```javascript
element.innerHTML = "Hello";
```

---

### Q7. What is querySelector()?

**Answer:**

It returns the first element matching a CSS selector.

Example:

```javascript
document.querySelector("#demo")
```

---

### Q8. Which DOM method creates a new element?

**Answer:**

```javascript
document.createElement()
```

---

### Q9. Which DOM method removes an element?

**Answer:**

```javascript
element.remove()
```

---

### Q10. What is appendChild()?

**Answer:**

It adds a child element to a parent element.

---

## 17. Important Points

1. DOM stands for Document Object Model.
2. The browser creates the DOM automatically.
3. HTML is represented as a Tree Structure.
4. Every HTML element becomes an Object.
5. JavaScript uses DOM to manipulate HTML dynamically.
6. `innerHTML` changes content.
7. `style` changes CSS.
8. `createElement()` creates new elements.
9. `appendChild()` adds elements.
10. `remove()` deletes elements.

---

## 18. Summary

The Document Object Model (DOM) is one of the most important concepts in JavaScript. It acts as a bridge between HTML and JavaScript, allowing developers to access, modify, create, and remove webpage elements dynamically. Understanding DOM manipulation is essential for building interactive websites, handling events, validating forms, and developing modern web applications.
