# Variables and Keywords in JavaScript

## Introduction

JavaScript is a **Dynamically Typed Language**.

This means:

* The programmer does not need to specify the data type while declaring a variable.
* The datatype is assigned automatically at runtime based on the value stored in the variable.

Example:

```javascript
let age = 25;          // Number
let name = "Basha";    // String
let status = true;     // Boolean
```

---

## Keywords Used to Declare Variables

JavaScript provides three keywords for declaring variables:

1. `var`
2. `let`
3. `const`

---

## 1. var Keyword

The `var` keyword is used to declare variables in JavaScript.

### Features of var

* Function Scoped
* Can be re-declared
* Can be re-assigned
* Does not support block scope
* Older way of declaring variables

### Example

```javascript
{
    var firstName = "Apple";
    console.log(firstName);

    var firstName = "Banana";
    console.log(firstName);
}

console.log(firstName);
```

### Output

```text
Apple
Banana
Banana
```

### Explanation

* `var` allows re-declaration.
* Variables declared with `var` inside a block are accessible outside the block.
* Therefore, `console.log(firstName)` works outside the braces.

---

## 2. let Keyword

The `let` keyword is used to declare block-scoped variables.

### Features of let

* Block Scoped
* Cannot be re-declared in the same scope
* Can be re-assigned
* Introduced in ES6 (ECMAScript 2015)

### Example

```javascript
{
    let age = 26;

    console.log(age);

    age = 30;

    console.log(age);
}

// console.log(age); // Error
```

### Output

```text
26
30
ReferenceError: age is not defined
```

### Explanation

* `let` variables exist only inside the block.
* They can be reassigned.
* They cannot be accessed outside the block.

---

## 3. const Keyword

The `const` keyword is used to declare constants.

### Features of const

* Block Scoped
* Must be initialized while declaration
* Cannot be re-assigned
* Cannot be re-declared

### Example

```javascript
{
    const isMarried = true;

    console.log(isMarried);

    // isMarried = false; // Error
}

// console.log(isMarried); // Error
```

### Output

```text
true

TypeError: Assignment to constant variable.
ReferenceError: isMarried is not defined
```

### Explanation

* A `const` variable cannot be reassigned.
* It is accessible only inside the block.
* Attempting to change its value causes an error.

---

## HTML File

### Variables.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Variables in JavaScript</title>

    <script src="demo.js"></script>
</head>

<body>

</body>

</html>
```

---

## JavaScript File

### demo.js

```javascript
// var keyword

{
    var firstName = "Apple";

    console.log(firstName);

    var firstName = "Banana";

    console.log(firstName);
}

console.log(firstName);


// let keyword

{
    let age = 26;

    console.log(age);

    age = 30;

    console.log(age);
}

// console.log(age);


// const keyword

{
    const isMarried = true;

    console.log(isMarried);

    // isMarried = false;
}

// console.log(isMarried);
```

---

## Difference Between var, let and const

| Feature       | var            | let         | const       |
| ------------- | -------------- | ----------- | ----------- |
| Scope         | Function Scope | Block Scope | Block Scope |
| Re-declare    | Yes            | No          | No          |
| Re-assign     | Yes            | Yes         | No          |
| Hoisting      | Yes            | Yes (TDZ)   | Yes (TDZ)   |
| Introduced In | ES5            | ES6         | ES6         |

---

## Important Notes

1. JavaScript is a Dynamically Typed Language.
2. `var` is function scoped.
3. `let` is block scoped.
4. `const` is block scoped and immutable.
5. Modern JavaScript development prefers `let` and `const`.
6. Use `const` by default and `let` only when reassignment is required.

---

## Summary

JavaScript variables are declared using `var`, `let`, and `const`.

* `var` → Old way, function scoped.
* `let` → Block scoped and re-assignable.
* `const` → Block scoped and cannot be re-assigned.

For modern JavaScript development, `let` and `const` are recommended because they provide better scope management and help avoid bugs.
