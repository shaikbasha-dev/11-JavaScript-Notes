# Phone Number Validation in JavaScript

## Introduction

**Phone Number Validation** is the process of verifying whether the phone number entered by the user satisfies the required conditions before submitting the form.

JavaScript performs this validation on the **client side**, allowing users to correct mistakes immediately without sending invalid data to the server.

---

## Why Phone Number Validation is Required

Phone Number Validation is used to:

1. Ensure the field is not empty.
2. Accept only numeric values.
3. Restrict the phone number length.
4. Prevent invalid data submission.
5. Improve user experience.
6. Reduce unnecessary server requests.

---

## Program: Phone Number Validation

### File Name

**phone.html**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Phone Number Validation</title>

    <script>

        function validate() {

            var res =
            document.getElementById("phone").value;

            if(res.length == 0) {

                document.getElementById("msg").innerHTML =
                "Phone number is required";

                return false;
            }

            else if(isNaN(res)) {

                document.getElementById("msg").innerHTML =
                "Phone number must be numeric";

                return false;
            }

            else if(res.length > 10) {

                document.getElementById("msg").innerHTML =
                "Phone number must be less than or equal to 10 digits";

                return false;
            }

            else {

                return true;
            }
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

## Step-by-Step Explanation

### Step 1

```javascript
function validate()
```

Creates a validation function.

This function executes whenever the user clicks the Submit button.

---

### Step 2

```javascript
var res =
document.getElementById("phone").value;
```

Retrieves the value entered by the user.

Example:

```text
9876543210
```

The value is stored in variable:

```javascript
res
```

---

### Step 3

```javascript
if(res.length == 0)
```

Checks whether the phone number field is empty.

If true:

```javascript
document.getElementById("msg").innerHTML =
"Phone number is required";
```

Output:

```text
Phone number is required
```

---

### Step 4

```javascript
isNaN(res)
```

**isNaN()** stands for:

```text
is Not a Number
```

It checks whether the entered value is numeric.

Example:

```text
987ABC
```

Output:

```text
Phone number must be numeric
```

---

### Step 5

```javascript
res.length > 10
```

Checks whether the entered phone number exceeds 10 digits.

Example:

```text
987654321012
```

Output:

```text
Phone number must be less than or equal to 10 digits
```

---

### Step 6

```javascript
return false;
```

Stops form submission.

The browser remains on the same page until valid data is entered.

---

### Step 7

```javascript
return true;
```

Allows the form to submit successfully.

---

# Understanding isNaN()

### Syntax

```javascript
isNaN(value)
```

Returns:

| Input    | Output |
| -------- | ------ |
| "123"    | false  |
| "98765"  | false  |
| "ABC"    | true   |
| "123ABC" | true   |
| ""       | false  |

Example:

```javascript
console.log(isNaN("123"));
```

Output:

```text
false
```

Example:

```javascript
console.log(isNaN("Hello"));
```

Output:

```text
true
```

---

# Understanding onsubmit Event

```html
<form onsubmit="return validate()">
```

Explanation:

1. User clicks Submit.
2. validate() function is called.
3. If:

```javascript
return true
```

Form submits.

If:

```javascript
return false
```

Submission stops.

---

# DOM Methods Used

## 1. getElementById()

Used to access HTML elements.

Example:

```javascript
document.getElementById("phone")
```

---

## 2. value

Returns user entered data.

Example:

```javascript
document.getElementById("phone").value
```

---

## 3. innerHTML

Displays dynamic messages.

Example:

```javascript
document.getElementById("msg").innerHTML =
"Invalid Phone Number";
```

---

# Output Cases

### Case 1: Empty Field

Input:

```text
(empty)
```

Output:

```text
Phone number is required
```

---

### Case 2: Alphabetic Input

Input:

```text
abcde
```

Output:

```text
Phone number must be numeric
```

---

### Case 3: Alphanumeric Input

Input:

```text
9876abc123
```

Output:

```text
Phone number must be numeric
```

---

### Case 4: More Than 10 Digits

Input:

```text
987654321012
```

Output:

```text
Phone number must be less than or equal to 10 digits
```

---

### Case 5: Valid Input

Input:

```text
9876543210
```

Output:

```text
Form Submitted Successfully
```

---

# Interview Questions

### Q1. What is Form Validation?

**Answer:**

Form Validation is the process of checking user inputs before sending them to the server.

---

### Q2. What is Client-Side Validation?

**Answer:**

Validation performed in the browser using JavaScript is called Client-Side Validation.

---

### Q3. What is isNaN() in JavaScript?

**Answer:**

`isNaN()` checks whether a value is **Not a Number**.

Syntax:

```javascript
isNaN(value)
```

---

### Q4. What does return false do in a form?

**Answer:**

It prevents the form from being submitted.

---

### Q5. Which event is commonly used in form validation?

**Answer:**

```javascript
onsubmit
```

---

### Q6. Which DOM method is used to access HTML elements?

**Answer:**

```javascript
document.getElementById()
```

---

### Q7. Which property is used to get user input?

**Answer:**

```javascript
value
```

---

# Important Points

1. JavaScript performs Client-Side Validation.
2. Phone numbers are usually validated using `isNaN()`.
3. `return false` prevents form submission.
4. `return true` allows form submission.
5. `getElementById()` accesses HTML elements.
6. `innerHTML` displays dynamic error messages.
7. Validation improves user experience.
8. Server-side validation is still necessary for security.

---

# Summary

Phone Number Validation is one of the most common applications of JavaScript Form Validation. It ensures that the user enters valid numeric data with the required length before submitting the form. By combining DOM methods such as `getElementById()`, `value`, `innerHTML`, and functions like `isNaN()`, developers can build responsive and user-friendly validation systems for modern web applications.
