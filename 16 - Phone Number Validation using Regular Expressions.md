# Phone Number Validation using Regular Expressions in JavaScript

## Introduction

Phone Number Validation is the process of verifying whether the phone number entered by the user follows a predefined format before submitting the form.

In JavaScript, **Regular Expressions (RegEx)** provide an efficient and powerful way to validate phone numbers by matching user input against a specific pattern.

---

## Why Use Regular Expressions for Validation?

Regular Expressions are used because they:

1. Validate input quickly.
2. Reduce lengthy conditional statements.
3. Check complex patterns with a single expression.
4. Improve code readability.
5. Provide accurate input validation.

---

## Program: Phone Number Validation using Regular Expressions

### File Name

**phone_regex.html**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Phone Number Validation using Regular Expressions</title>

    <script>

        function validate() {

            var res =
            document.getElementById("phone").value;

            var t =
            /^[6-9]{1}[0-9]{9}$/.test(res);

            if(t == false) {

                document.getElementById("msg").innerHTML =
                "Invalid phone number";

                document.getElementById("phone").style.border =
                "2px solid red";

                return false;
            }

            return true;
        }

    </script>

</head>

<body>

    <form onsubmit="return validate()">

        <label>Phone Number</label>

        <input type="text"
               id="phone"
               name="phone">

        <span id="msg"
              style="color:red"></span>

        <br><br>

        <input type="submit"
               value="Submit">

    </form>

</body>
</html>
```

---

# Understanding the Regular Expression

```javascript
/^[6-9]{1}[0-9]{9}$/
```

This is the heart of the program.

Let us break it down:

### 1. `^`

```text
Beginning of the string
```

The phone number must start from here.

---

### 2. `[6-9]{1}`

```text
First digit should be 6, 7, 8 or 9
```

Examples:

✔ 9876543210

✔ 8123456789

✘ 5123456789

---

### 3. `[0-9]{9}`

```text
Followed by exactly 9 digits
```

Examples:

✔ 9876543210

✘ 98765432

✘ 987654321012

---

### 4. `$`

```text
End of the string
```

Ensures there are no extra characters after 10 digits.

---

## Complete Meaning

```javascript
/^[6-9]{1}[0-9]{9}$/
```

Means:

```text
The number must:

Start with 6,7,8 or 9

AND

Contain exactly 10 digits

AND

Contain only numbers
```

---

# test() Method

### Syntax

```javascript
regex.test(string)
```

Returns:

```text
true  -> Pattern matched

false -> Pattern not matched
```

Example:

```javascript
var exp = /^[6-9]{1}[0-9]{9}$/;

console.log(exp.test("9876543210"));
```

Output:

```text
true
```

Example:

```javascript
console.log(exp.test("1234567890"));
```

Output:

```text
false
```

---

# Step-by-Step Explanation

### Step 1

```javascript
var res =
document.getElementById("phone").value;
```

Gets the user entered phone number.

---

### Step 2

```javascript
var t =
/^[6-9]{1}[0-9]{9}$/.test(res);
```

Checks whether the phone number matches the regular expression.

If matched:

```text
t = true
```

Else:

```text
t = false
```

---

### Step 3

```javascript
if(t == false)
```

Checks whether the input is invalid.

---

### Step 4

```javascript
document.getElementById("msg").innerHTML =
"Invalid phone number";
```

Displays:

```text
Invalid phone number
```

---

### Step 5

```javascript
document.getElementById("phone").style.border =
"2px solid red";
```

Changes the border color to red.

Output:

```text
+-------------------+
| Invalid Input     |
+-------------------+

Border becomes RED
```

---

### Step 6

```javascript
return false;
```

Stops form submission.

---

### Step 7

```javascript
return true;
```

Allows form submission.

---

# Output Cases

### Case 1

Input:

```text
9876543210
```

Output:

```text
Valid Phone Number
```

Form Submitted Successfully.

---

### Case 2

Input:

```text
5876543210
```

Output:

```text
Invalid phone number
```

Reason:

```text
Starts with 5
```

---

### Case 3

Input:

```text
98765432
```

Output:

```text
Invalid phone number
```

Reason:

```text
Less than 10 digits
```

---

### Case 4

Input:

```text
987654321012
```

Output:

```text
Invalid phone number
```

Reason:

```text
More than 10 digits
```

---

### Case 5

Input:

```text
98ABC43210
```

Output:

```text
Invalid phone number
```

Reason:

```text
Contains alphabets
```

---

# Important Regular Expression Symbols

| Symbol | Meaning                  |
| ------ | ------------------------ |
| ^      | Start of string          |
| $      | End of string            |
| []     | Range of characters      |
| {}     | Number of occurrences    |
| .      | Any single character     |
| *      | Zero or more occurrences |
| +      | One or more occurrences  |
| ?      | Optional character       |

---

# Interview Questions

### Q1. What is Regular Expression?

**Answer:**

A Regular Expression is a sequence of characters used to define a search pattern for matching, validating, and manipulating strings.

---

### Q2. Which method is used to test a regular expression?

**Answer:**

```javascript
test()
```

Example:

```javascript
regex.test(str)
```

---

### Q3. What does `^` mean in RegEx?

**Answer:**

It indicates:

```text
Start of the string
```

---

### Q4. What does `$` mean in RegEx?

**Answer:**

It indicates:

```text
End of the string
```

---

### Q5. Explain:

```javascript
/^[6-9]{1}[0-9]{9}$/
```

**Answer:**

The phone number:

* Must start with 6, 7, 8, or 9.
* Must contain exactly 10 digits.
* Must contain only numbers.

---

### Q6. What does test() return?

**Answer:**

```text
true  -> if pattern matches

false -> if pattern does not match
```

---

### Q7. Which DOM property is used to change border color?

**Answer:**

```javascript
element.style.border
```

Example:

```javascript
document.getElementById("phone").style.border =
"2px solid red";
```

---

# Important Points

1. Regular Expressions are used for pattern matching.
2. `test()` checks whether input matches a pattern.
3. `^` indicates the beginning of the string.
4. `$` indicates the end of the string.
5. Indian mobile numbers generally start with 6, 7, 8, or 9.
6. Client-side validation improves user experience.
7. Server-side validation should also be implemented for security.

---

# Summary

Phone Number Validation using Regular Expressions is one of the most important applications of JavaScript form validation. Using the expression:

```javascript
/^[6-9]{1}[0-9]{9}$/
```

developers can efficiently validate Indian mobile numbers with minimal code. Regular Expressions provide fast, flexible, and reliable validation techniques that are widely used in modern web applications for validating phone numbers, emails, passwords, and other user inputs.
