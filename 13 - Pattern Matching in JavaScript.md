# Pattern Matching in JavaScript

## Introduction

Pattern Matching in JavaScript is performed using **Regular Expressions (RegEx)**. It is used to search, match, replace, and validate strings based on predefined patterns.

Pattern matching is commonly used in:

* Email Validation
* Password Validation
* Mobile Number Validation
* Search Operations
* Replace Operations
* Form Validation
* Text Processing

---

# Syntax

```javascript
/Pattern/OptionalIdentifiers
```

### General Syntax

```javascript
var regex = /pattern/flags;
```

Example:

```javascript
var regex = /hello/i;
```

Here:

* hello → Pattern
* i → Identifier (Flag)

---

# Identifiers (Flags)

JavaScript provides several identifiers to modify the behavior of regular expressions.

| Identifier | Meaning                        |
| ---------- | ------------------------------ |
| g          | Global Search                  |
| i          | Case Insensitive Search        |
| m          | Multi-line Search              |
| s          | Dot matches newline characters |
| u          | Unicode matching               |
| y          | Sticky matching                |

---

## 1. g - Global Search

Searches for all occurrences of a pattern.

### Example

```javascript
var str = "hello hello hello";

var result = str.match(/hello/g);

console.log(result);
```

### Output

```text
["hello","hello","hello"]
```

---

## 2. i - Case Insensitive Search

Ignores uppercase and lowercase differences.

### Example

```javascript
var str = "HELLO";

console.log(/hello/i.test(str));
```

### Output

```text
true
```

---

## 3. m - Multi-line Search

Matches patterns across multiple lines.

### Example

```javascript
var str = `Java
Script`;

console.log(/^Script/m.test(str));
```

### Output

```text
true
```

---

## 4. s - Dot All Modifier

Allows dot (.) to match newline characters.

### Example

```javascript
var str = "Hello\nWorld";

console.log(/Hello.World/s.test(str));
```

### Output

```text
true
```

---

## 5. u - Unicode Flag

Treats the pattern as Unicode characters.

### Example

```javascript
var str = "😊";

console.log(/^.$/u.test(str));
```

### Output

```text
true
```

---

## 6. y - Sticky Flag

Matches only from the last matched position.

### Example

```javascript
var regex = /hello/y;

regex.lastIndex = 0;

console.log(regex.test("hello world"));
```

### Output

```text
true
```

---

# Methods Used in Pattern Matching

There are three important methods:

1. search()
2. replace()
3. match()

---

# 1. search() Method

The `search()` method searches for a pattern inside a string and returns the index position of the first match.

### Syntax

```javascript
string.search(regex)
```

---

### Example

**Common.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Regular Expressions in JavaScript</title>
</head>
<body>

    <p id="res"></p>

    <script>

        var str = "KodNest Technologies";

        var n = str.search(/T/i);

        document.getElementById("res").innerHTML = n;

    </script>

</body>
</html>
```

### Output

```text
8
```

### Explanation

```javascript
var str = "KodNest Technologies";

var n = str.search(/T/i);
```

* `/T/` searches for T
* `i` ignores uppercase/lowercase
* search() returns:

```text
8
```

because T is found at index 8.

---

# 2. replace() Method

The `replace()` method replaces the matched text with a new value.

### Syntax

```javascript
string.replace(regex,newValue)
```

---

### Example

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Regular Expressions in JavaScript</title>
</head>

<body>

    <p id="res"></p>

    <script>

        var str = "KodNest Technologies";

        var newStr = str.replace(/T/i,"X");

        document.getElementById("res").innerHTML = newStr;

    </script>

</body>
</html>
```

### Output

```text
KodNest Xechnologies
```

### Explanation

```javascript
var newStr = str.replace(/T/i,"X");
```

* Searches T
* Replaces T with X

Result:

```text
KodNest Xechnologies
```

---

# 3. match() Method

The `match()` method returns the matched value as an array.

### Syntax

```javascript
string.match(regex)
```

---

### Example

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Regular Expressions in JavaScript</title>
</head>

<body>

    <p id="res"></p>

    <script>

        var str = "KodNest Technologies";

        var result = str.match(/T/i);

        document.getElementById("res").innerHTML = result;

    </script>

</body>
</html>
```

### Output

```text
T
```

or

```text
["T"]
```

### Explanation

The match() method returns:

```javascript
["T"]
```

because the character T is matched.

---

# Difference Between search(), replace(), and match()

| Method    | Purpose               | Return Type  |
| --------- | --------------------- | ------------ |
| search()  | Finds position        | Index Number |
| replace() | Replaces matched text | New String   |
| match()   | Finds matched pattern | Array        |

---

# Example Using All Three Methods

```javascript
var str = "KodNest Technologies";

console.log(str.search(/T/i));

console.log(str.replace(/T/i,"X"));

console.log(str.match(/T/i));
```

### Output

```text
8
KodNest Xechnologies
["T"]
```

---

# Real Time Applications

Pattern Matching is used in:

1. Email Validation
2. Password Validation
3. Mobile Number Validation
4. PAN Card Validation
5. Aadhaar Number Validation
6. Search Engines
7. Text Editors
8. Find and Replace Features
9. Form Validation
10. Data Extraction

---

# Frequently Asked Interview Questions

### Q1. What is Pattern Matching in JavaScript?

**Answer:**

Pattern Matching is the process of searching and manipulating strings using Regular Expressions.

---

### Q2. What is the syntax of Regular Expression?

**Answer:**

```javascript
/pattern/flags
```

Example:

```javascript
/hello/i
```

---

### Q3. What does the i flag do?

**Answer:**

It performs case-insensitive matching.

Example:

```javascript
/hello/i
```

Matches:

```text
hello
HELLO
Hello
```

---

### Q4. What does search() return?

**Answer:**

It returns the index position of the first matched character.

---

### Q5. What does replace() return?

**Answer:**

It returns a new string after replacing the matched text.

---

### Q6. What does match() return?

**Answer:**

It returns an array containing the matched values.

---

# Summary

Pattern Matching is one of the most important applications of Regular Expressions in JavaScript. By using identifiers (flags) and methods such as `search()`, `replace()`, and `match()`, developers can efficiently search, validate, replace, and manipulate strings. These concepts are widely used in real-world applications such as form validations, search engines, data extraction, and text processing systems.
