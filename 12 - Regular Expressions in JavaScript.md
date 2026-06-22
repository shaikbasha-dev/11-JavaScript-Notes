# Regular Expressions in JavaScript (Very Very Important)

## Introduction

Regular Expressions (RegEx) are special patterns used to search, match, validate, and manipulate strings in JavaScript.

They are widely used for:

* Form Validation
* Email Validation
* Password Validation
* Mobile Number Validation
* Search Operations
* Replace Operations
* Pattern Matching

Regular Expressions are one of the most important topics in JavaScript and are frequently asked in interviews.

---

# Definition

A **Regular Expression** is a sequence of characters that forms a search pattern.

It is used to:

* Search text
* Match patterns
* Validate user input
* Replace characters
* Extract information from strings

---

# Syntax

```javascript
var regex = /pattern/;
```

Or

```javascript
var regex = new RegExp("pattern");
```

---

# Example 1: Matching "hello"

```javascript
var regex = /hello/;

var str = "hello world";

console.log(regex.test(str));
```

### Output

```text
true
```

### Explanation

* `/hello/` searches for the word "hello".
* The string contains "hello".
* Therefore `test()` returns:

```text
true
```

---

# Example 2: Matching "world"

```javascript
var regex = /world/;

var str = "hello world";

console.log(regex.test(str));
```

### Output

```text
true
```

### Explanation

The word **world** exists in the string.

Hence:

```text
true
```

---

# Example 3: Matching "hi"

```javascript
var regex = /hi/;

var str = "hello world";

console.log(regex.test(str));
```

### Output

```text
false
```

### Explanation

The word **hi** is not present inside the string.

Therefore:

```text
false
```

---

# test() Method

The `test()` method checks whether the given pattern exists in the string.

### Syntax

```javascript
regex.test(string)
```

### Return Type

* true → Pattern Found
* false → Pattern Not Found

---

# Special Characters in Regular Expressions

## 1. Dot (.)

The dot matches **any single character**.

### Example

```javascript
var regex = /h.llo/;

var str = "hello world";

console.log(regex.test(str));
```

### Output

```text
true
```

### Explanation

The dot (`.`) replaces one character.

```text
h . l l o

e replaces .
```

Hence:

```text
hello → Match Found
```

---

## 2. Asterisk (*)

The asterisk means:

```text
Zero or More Occurrences
```

### Example

```javascript
var regex = /h*llo/;

var str = "hllo world";

console.log(regex.test(str));
```

### Output

```text
true
```

### Explanation

`h*`

means:

```text
h → 0 times
h → 1 time
h → many times
```

So:

```text
hllo
hello
hhllo
hhhllo
```

All are valid matches.

---

## 3. Plus (+)

The plus means:

```text
One or More Occurrences
```

### Example

```javascript
var regex = /h+llo/;

var str = "hhllo world";

console.log(regex.test(str));
```

### Output

```text
true
```

### Explanation

`h+`

means:

```text
hllo
hhllo
hhhllo
hhhhllo
```

At least one **h** is mandatory.

---

# Regular Expression Modifiers

## 1. i Modifier (Case Insensitive)

### Example

```javascript
var regex = /hello/i;

console.log(regex.test("HELLO"));
```

### Output

```text
true
```

### Explanation

The `i` modifier ignores uppercase and lowercase differences.

---

## 2. g Modifier (Global Search)

### Example

```javascript
var str = "hello hello hello";

var regex = /hello/g;

console.log(str.match(regex));
```

### Output

```text
["hello","hello","hello"]
```

### Explanation

The global modifier searches all occurrences.

---

# Important RegEx Symbols

| Symbol | Meaning                  |
| ------ | ------------------------ |
| .      | Any one character        |
| *      | Zero or more occurrences |
| +      | One or more occurrences  |
| ?      | Zero or one occurrence   |
| ^      | Starts with              |
| $      | Ends with                |
| []     | Character set            |
| [a-z]  | Lowercase letters        |
| [A-Z]  | Uppercase letters        |
| [0-9]  | Digits                   |
| \d     | Any digit                |
| \D     | Non-digit                |
| \w     | Word character           |
| \W     | Non-word character       |
| \s     | White space              |
| \S     | Non white space          |

---

# Example: Email Validation

```javascript
var email = "abc@gmail.com";

var regex = /^[a-zA-Z0-9]+@[a-z]+\.[a-z]{2,3}$/;

console.log(regex.test(email));
```

### Output

```text
true
```

---

# Example: Mobile Number Validation

```javascript
var mobile = "9876543210";

var regex = /^[0-9]{10}$/;

console.log(regex.test(mobile));
```

### Output

```text
true
```

---

# Example: Password Validation

```javascript
var password = "Java@123";

var regex = /^(?=.*[A-Z])(?=.*[a-z])(?=.*[0-9]).{8,}$/;

console.log(regex.test(password));
```

### Output

```text
true
```

### Conditions

Password must contain:

* One Uppercase letter
* One Lowercase letter
* One Number
* Minimum 8 Characters

---

# Difference Between * and +

| * Operator           | + Operator                 |
| -------------------- | -------------------------- |
| Zero or More         | One or More                |
| Empty value allowed  | Empty value not allowed    |
| h*llo matches "llo"  | h+llo does not match "llo" |
| Optional occurrences | Minimum one occurrence     |

---

# Applications of Regular Expressions

Regular Expressions are used in:

1. Email Validation
2. Password Validation
3. Mobile Number Validation
4. Username Validation
5. Search Functionality
6. Find and Replace
7. Data Extraction
8. Form Validation
9. Parsing Text Files
10. Input Sanitization

---

# Interview Questions

### Q1. What is Regular Expression?

**Answer:**

Regular Expression is a sequence of characters used to create search patterns for matching, validating, and manipulating strings.

---

### Q2. Which method is commonly used for matching a pattern?

**Answer:**

```javascript
test()
```

It returns:

* true
* false

---

### Q3. What does "." represent in RegEx?

**Answer:**

It matches any one character.

Example:

```javascript
/h.llo/
```

Matches:

```text
hello
hallo
hxllo
```

---

### Q4. Difference between * and + ?

**Answer:**

* `*` → Zero or More Occurrences
* `+` → One or More Occurrences

---

### Q5. What does the i modifier do?

**Answer:**

It performs a case-insensitive search.

Example:

```javascript
/hello/i
```

Matches:

```text
HELLO
Hello
hello
```

---

# Summary

Regular Expressions are powerful tools used for pattern matching, validation, and string manipulation in JavaScript. They simplify complex searching operations and are extensively used in real-world applications such as form validation, email verification, password checking, and data extraction. Mastering Regular Expressions is an important skill for every JavaScript developer and a frequently asked topic in technical interviews.
