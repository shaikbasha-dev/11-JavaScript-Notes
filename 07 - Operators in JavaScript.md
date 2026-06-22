# Operators in JavaScript

## Introduction

In JavaScript, **Operators** are special symbols used to perform operations on variables and values.

Operators are used to:

* Perform arithmetic calculations
* Compare values
* Combine conditions
* Assign values
* Concatenate strings
* Make decisions using conditions

---

## Types of Operators in JavaScript

JavaScript provides the following major types of operators:

1. Arithmetic Operators
2. Comparison Operators
3. Logical Operators
4. Ternary Operator
5. String Operators

---

# 1. Arithmetic Operators

Arithmetic operators are used to perform mathematical calculations.

| Operator | Description         | Example |
| -------- | ------------------- | ------- |
| +        | Addition            | a + b   |
| -        | Subtraction         | a - b   |
| *        | Multiplication      | a * b   |
| /        | Division            | a / b   |
| %        | Modulus (Remainder) | a % b   |
| ++       | Increment           | a++     |
| --       | Decrement           | a--     |

### Example

```javascript
var a = 10;
var b = 5;

console.log(a + b); // 15
console.log(a - b); // 5
console.log(a * b); // 50
console.log(a / b); // 2
console.log(a % b); // 0
```

### Increment Operator

```javascript
var a = 10;

console.log(a++); // 10
console.log(a);   // 11

console.log(++a); // 12
```

**Explanation:**

* `a++` → Post Increment
  First returns the value, then increments.

* `++a` → Pre Increment
  First increments the value, then returns it.

---

### Decrement Operator

```javascript
var b = 5;

console.log(b--); // 5
console.log(b);   // 4

console.log(--b); // 3
```

**Explanation:**

* `b--` → Post Decrement
* `--b` → Pre Decrement

---

# 2. Comparison Operators

Comparison operators compare two values and return either:

```javascript
true
```

or

```javascript
false
```

| Operator | Meaning               |
| -------- | --------------------- |
| ==       | Equal to              |
| !=       | Not Equal to          |
| ===      | Strict Equal          |
| !==      | Strict Not Equal      |
| >        | Greater Than          |
| <        | Less Than             |
| >=       | Greater Than or Equal |
| <=       | Less Than or Equal    |

---

### Example 1

```javascript
var x = 10;
var y = "10";

console.log(x == y);
```

Output:

```text
true
```

**Reason:**

`==` checks only values.

---

### Example 2

```javascript
var x = 10;
var y = "10";

console.log(x === y);
```

Output:

```text
false
```

**Reason:**

`===` checks:

* Value
* Data Type

`10` → Number

`"10"` → String

Hence false.

---

### More Examples

```javascript
var x = 10;
var y = 20;

console.log(x != y);   // true

console.log(x !== y);  // true

console.log(x == y);   // false

console.log(x === y);  // false

console.log(x <= y);   // true

console.log(x >= y);   // false
```

---

# 3. Logical Operators

Logical operators are used to combine conditions.

| Operator | Meaning     |
| -------- | ----------- |
| &&       | Logical AND |
| ||       | Logical OR  |
| !        | Logical NOT |

---

## Logical AND (&&)

Returns true only when all conditions are true.

```javascript
var a = 10;
var b = 20;

var c = (a < b && b > a);

console.log(c);
```

Output:

```text
true
```

---

```javascript
var a = 10;
var b = 20;

var c = (a > b && b > a);

console.log(c);
```

Output:

```text
false
```

---

## Logical OR (||)

Returns true if at least one condition is true.

```javascript
var a = 10;
var b = 20;

var c = (a > b || b > a);

console.log(c);
```

Output:

```text
true
```

---

```javascript
var a = 10;
var b = 20;

var c = (a > b || b < a);

console.log(c);
```

Output:

```text
false
```

---

## Logical NOT (!)

Reverses the result.

```javascript
var a = true;

console.log(!a);
```

Output:

```text
false
```

---

# 4. Ternary Operator

The Ternary Operator is a shorthand form of an if-else statement.

### Syntax

```javascript
condition ? valueIfTrue : valueIfFalse;
```

---

### Example

```javascript
var n1 = 5;
var n2 = 10;

var result = n1 > n2 ? n1 : n2;

console.log(result);
```

Output:

```text
10
```

**Explanation:**

If `n1 > n2`

return `n1`

Else

return `n2`

---

### Another Example

```javascript
var age = 20;

var status = age >= 18 ? "Eligible to Vote" : "Not Eligible";

console.log(status);
```

Output:

```text
Eligible to Vote
```

---

# 5. String Operators

The `+` operator is also used for string concatenation.

It combines two or more strings.

---

### Example

```javascript
var str1 = "Hello ";
var str2 = "World";

var result = str1 + str2;

console.log(result);
```

Output:

```text
Hello World
```

---

### Example

```javascript
var fname = "Shaik";

var lname = "Basha";

console.log(fname + " " + lname);
```

Output:

```text
Shaik Basha
```

---

# Difference Between == and ===

| ==                       | ===                       |
| ------------------------ | ------------------------- |
| Checks only value        | Checks value and datatype |
| Performs type conversion | No type conversion        |
| 10 == "10" → true        | 10 === "10" → false       |

---

# Important Points

1. Operators are symbols used to perform operations.
2. Arithmetic operators perform calculations.
3. Comparison operators return true or false.
4. Logical operators combine multiple conditions.
5. Ternary operator is a shorthand for if-else.
6. The + operator can be used for both:

   * Addition
   * String Concatenation
7. `===` is preferred over `==` because it checks both value and datatype.

---

# Summary

JavaScript Operators are one of the fundamental concepts of programming. They are used to perform calculations, compare values, combine conditions, make decisions, and manipulate strings. Understanding operators is essential because they are used throughout JavaScript applications, from basic programs to advanced web development and frameworks such as React, Angular, and Node.js.
