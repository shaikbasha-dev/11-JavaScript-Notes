# BOM (Browser Object Model)

## 1. Introduction

The **Browser Object Model (BOM)** is a collection of objects provided by the browser that allows JavaScript to communicate with and control the browser window.

Unlike the DOM, which deals with the HTML document, the BOM deals with the browser environment itself.

The BOM allows developers to:

* Open new browser windows
* Resize browser windows
* Get screen information
* Access browser history
* Obtain browser details
* Display popup messages
* Navigate to different URLs

---

## 2. Definition

**BOM (Browser Object Model)** is a collection of browser-provided objects that enables JavaScript to interact with the browser and its components.

It acts as a bridge between:

```text
JavaScript  <------>  Browser
```

---

## 3. Main BOM Objects

### 1. Window Object

The `window` object is the root object of BOM.

It represents:

```text
Browser Window
```

It is automatically created by the browser.

Example:

```javascript
window.alert("Welcome");
```

or simply

```javascript
alert("Welcome");
```

because every BOM object belongs to the window object.

---

### 2. Navigator Object

The navigator object contains information about:

* Browser name
* Browser version
* Platform
* User Agent

Example:

```javascript
console.log(navigator.appName);

console.log(navigator.platform);

console.log(navigator.userAgent);
```

---

### 3. Screen Object

The screen object provides information about the user's display screen.

Properties:

```javascript
screen.width

screen.height

screen.availWidth

screen.availHeight
```

---

### 4. History Object

The history object stores the browser history.

Methods:

```javascript
history.back()

history.forward()

history.go()
```

Example:

```javascript
history.back();
```

Moves to previous page.

---

### 5. Location Object

The location object contains information about the current URL.

Example:

```javascript
console.log(location.href);

console.log(location.hostname);

console.log(location.protocol);
```

---

## 4. Hierarchy of BOM

```text
                 Window
        _______________________

       |          |            |

 Navigator     Screen       History

       |

    Location

       |

     Document (DOM)
```

The Window object is the top-most object.

---

## 5. Why BOM is Used

BOM is used to:

1. Communicate with browser
2. Get screen size
3. Navigate pages
4. Display alerts
5. Open new windows
6. Access browser information
7. Control browser history

---

## 6. Example Program

```html
<!DOCTYPE html>

<html>

<head>

<title>BOM Example</title>

</head>

<body>

<p id="Wid"></p>

<script>

document.getElementById("Wid").innerHTML =

"The width of browser window is : "

+ screen.width;

document.getElementById("Wid").innerHTML +=

"<br>The height of browser window is : "

+ screen.height;

</script>

</body>

</html>
```

---

## 7. Step-by-Step Explanation

### Line 1

```html
<!DOCTYPE html>
```

Declares HTML5 document.

---

### Line 2

```html
<html>
```

Root element.

---

### Line 3

```html
<head>
```

Contains metadata.

---

### Line 4

```html
<title>BOM Example</title>
```

Sets browser tab title.

---

### Line 5

```html
<body>
```

Contains webpage content.

---

### Line 6

```html
<p id="Wid"></p>
```

Creates an empty paragraph with id:

```text
Wid
```

The screen details will be displayed here.

---

### Line 7

```javascript
document.getElementById("Wid")
```

Selects the paragraph element.

---

### Line 8

```javascript
screen.width
```

Returns:

```text
Browser Screen Width
```

Example:

```text
1920
```

---

### Line 9

```javascript
screen.height
```

Returns:

```text
Browser Screen Height
```

Example:

```text
1080
```

---

### Line 10

```javascript
innerHTML
```

Displays the data inside the HTML element.

---

## Output

Suppose your monitor resolution is:

```text
1920 × 1080
```

Output:

```text
The width of browser window is : 1920

The height of browser window is : 1080
```

---

## 8. Alert Box Example

```javascript
alert("Welcome to JavaScript");
```

Output:

```text
-----------------------

Welcome to JavaScript

         OK

-----------------------
```

---

## 9. Confirm Box Example

```javascript
confirm("Are you sure?");
```

Output:

```text
--------------------

Are you sure?

 OK     Cancel

--------------------
```

Returns:

```text
true  -> OK

false -> Cancel
```

---

## 10. Prompt Box Example

```javascript
prompt("Enter Your Name");
```

Output:

```text
-------------------------

Enter Your Name

_____________

      OK

-------------------------
```

Returns the value entered by the user.

---

## 11. Window Methods

### Open a New Window

```javascript
window.open();
```

---

### Close Current Window

```javascript
window.close();
```

---

### Print Current Page

```javascript
window.print();
```

---

## 12. Navigator Properties

```javascript
navigator.appName

navigator.appVersion

navigator.platform

navigator.userAgent

navigator.language
```

Example:

```javascript
console.log(navigator.platform);
```

Output:

```text
Win32
```

---

## 13. Location Properties

```javascript
location.href

location.hostname

location.protocol

location.pathname
```

Example:

```javascript
console.log(location.href);
```

Output:

```text
https://www.example.com/index.html
```

---

## 14. History Methods

### Back

```javascript
history.back();
```

Moves:

```text
Current Page

↓

Previous Page
```

---

### Forward

```javascript
history.forward();
```

Moves:

```text
Current Page

↓

Next Page
```

---

### Go

```javascript
history.go(-1)
```

Moves one page back.

---

## Difference Between DOM and BOM

| DOM                       | BOM                       |
| ------------------------- | ------------------------- |
| Document Object Model     | Browser Object Model      |
| Represents HTML document  | Represents Browser        |
| Manipulates HTML elements | Manipulates Browser       |
| Root object is document   | Root object is window     |
| Changes webpage contents  | Controls browser behavior |

---

## Interview Questions

### Q1. What is BOM?

**Answer:**

BOM stands for Browser Object Model.

It allows JavaScript to communicate with and control the browser.

---

### Q2. What is the root object of BOM?

**Answer:**

```javascript
window
```

---

### Q3. Name important BOM objects.

**Answer:**

1. Window
2. Navigator
3. Screen
4. History
5. Location

---

### Q4. Which object provides screen dimensions?

**Answer:**

```javascript
screen
```

Example:

```javascript
screen.width

screen.height
```

---

### Q5. Which object stores browser history?

**Answer:**

```javascript
history
```

---

### Q6. Which object stores URL information?

**Answer:**

```javascript
location
```

---

### Q7. Difference between DOM and BOM?

**Answer:**

DOM manipulates HTML documents.

BOM manipulates browser components.

---

### Q8. What is window.alert()?

**Answer:**

Displays a popup alert message.

Example:

```javascript
alert("Hello");
```

---

## Important Points

1. BOM stands for Browser Object Model.
2. Window is the root object.
3. DOM is a part of BOM.
4. screen object gives screen information.
5. navigator object gives browser details.
6. history object manages browser history.
7. location object manages URL information.
8. alert(), confirm(), and prompt() are window methods.

---

## Summary

The Browser Object Model (BOM) is a browser-provided interface that enables JavaScript to interact with browser components such as the window, screen, navigator, history, and location objects. Using BOM, developers can obtain browser information, manage navigation, display dialogs, access screen properties, and build dynamic and interactive web applications efficiently.
