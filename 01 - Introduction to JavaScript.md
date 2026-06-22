# Introduction to JavaScript

## What is JavaScript?

JavaScript is a high-level, interpreted programming language that is commonly used to create interactive and dynamic web pages.

It is one of the core technologies of web development along with:

* HTML → Structure of the webpage
* CSS → Styling of the webpage
* JavaScript → Behaviour and Interactivity of the webpage

JavaScript is a versatile language that can be used for:

* Client-side development
* Server-side development
* Form validation
* Event handling
* DOM manipulation
* Animations
* AJAX communication
* Building modern web applications

---

## Features of JavaScript

1. JavaScript is a high-level interpreted programming language.
2. It supports object-oriented programming.
3. It supports functional programming.
4. It supports event-driven programming.
5. It is a lightweight scripting language.
6. It is case-sensitive.
7. It can be executed directly in the browser.
8. It works together with HTML and CSS.
9. It is used to validate user input before submitting forms.
10. It is widely used in modern frameworks like React, Angular, and Vue.js.

---

## History of JavaScript

1. JavaScript was created by **Brendan Eich** in **1995** at Netscape Communications Corporation.
2. It was developed in just **10 days**.
3. Initially, it was named **Mocha**.
4. Later, it was renamed to **LiveScript**.
5. Finally, it was renamed to **JavaScript**.
6. In 1996, Netscape submitted JavaScript to **ECMA** for standardization.
7. ECMA stands for **European Computer Manufacturers Association**.
8. In 1997, JavaScript became an ECMA standard.
9. ES6 (ECMAScript 2015) was introduced in 2015 with many new features.

---

## Syntax of JavaScript

JavaScript code can be written inside the `<script>` tag.

```html
<script>

    // JavaScript Code

</script>
```

JavaScript can be written in three ways:

1. Inside `<head></head>`
2. Inside `<body></body>`
3. In an external `.js` file

---

## Important Notes

1. `.` (Dot Operator) → Used to access properties and methods.

Example:

```javascript
document.write("Hello");
```

2. `write()` is a method of the document object.

3. JavaScript is a Case Sensitive Language.

Example:

```javascript
var name;
var Name;
```

Both are different variables.

4. Always run the HTML file, not the `.js` file directly.

Because JavaScript is executed within an HTML document by the browser.

5. `name` is an internal predefined property in JavaScript and browsers.

---

## Way 1: JavaScript inside Body Tag

### Program

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title>JavaScript</title>
</head>

<body>

    <h1>Welcome to HTML</h1>

    <h2>Welcome to KodNest</h2>

    <script>

        document.write("Welcome to JavaScript");

    </script>

</body>

</html>
```

### Output

```text
Welcome to HTML

Welcome to KodNest

Welcome to JavaScript
```

---

## Way 2: JavaScript inside Head Tag

### Program

```html
<!DOCTYPE html>
<html lang="en">

<head>

    <title>JavaScript</title>

    <script>

        document.write("Welcome to JavaScript");

    </script>

</head>

<body>

    <h1>Welcome to HTML</h1>

    <h2>Welcome to KodNest</h2>

</body>

</html>
```

### Explanation

* JavaScript code is written inside the `<head>` section.
* It executes when the page loads.
* `document.write()` writes content directly to the webpage.

---

## Way 3: External JavaScript File

### HTML File

```html
<!DOCTYPE html>
<html lang="en">

<head>

    <title>JavaScript</title>

    <script src="Demo1.js"></script>

</head>

<body>

    <h1>Welcome to HTML</h1>

    <h2>Welcome to KodNest</h2>

</body>

</html>
```

### External JavaScript File

```javascript
document.write("Welcome to JavaScript");
```

### Advantages of External JavaScript

* Reusable code
* Easy maintenance
* Cleaner HTML code
* Better organization
* Used in real-world projects

---

## Best Practices

1. Prefer External JavaScript files.
2. Place JavaScript before the closing `</body>` tag.
3. Avoid excessive use of `document.write()`.
4. Use DOM methods such as:

```javascript
getElementById()

querySelector()

innerHTML

createElement()

appendChild()
```

---

## Summary

JavaScript is one of the most important programming languages for web development.

It helps developers:

* Create interactive webpages
* Validate forms
* Handle events
* Manipulate HTML elements
* Build dynamic web applications
* Develop modern front-end and back-end applications

JavaScript, along with HTML and CSS, forms the foundation of modern web development.
