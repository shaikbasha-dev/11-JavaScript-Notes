# Arrays in JavaScript

## Introduction

An **Array** is a data structure that can store multiple values in a single variable.

In JavaScript, arrays are created using square brackets `[]` and can store:

* Numbers
* Strings
* Boolean values
* Objects
* Arrays
* Mixed Data Types

Arrays are **Zero Indexed**, which means:

* First element → Index 0
* Second element → Index 1
* Third element → Index 2

and so on.

---

## Creating Arrays in JavaScript

### Example 1

```javascript
var numbers = [1, 2, 3, 4, 5];

console.log(numbers);

console.log(typeof(numbers));
```

### Output

```text
[1, 2, 3, 4, 5]

object
```

### Explanation

* `numbers` is an array containing five numeric values.
* Arrays are special types of objects in JavaScript.
* Therefore:

```javascript
typeof(numbers)
```

returns

```text
object
```

---

## Mixed Array

JavaScript arrays can store different types of values.

### Example

```javascript
var mixedArray = [

    1,

    "hello",

    true,

    {name : "John"},

    [1, 2, 3]

];

console.log(mixedArray);

console.log(typeof(mixedArray));
```

### Output

```text
[
1,
"hello",
true,
{name:"John"},
[1,2,3]
]

object
```

---

## Common Array Methods

JavaScript provides many built-in methods to manipulate arrays.

Some important methods are:

1. push()
2. pop()
3. unshift()
4. shift()
5. slice()
6. splice()
7. delete

---

# 1. push()

The `push()` method adds one or more elements at the end of the array.

### Example

```javascript
var fruits = ["apple", "banana", "orange"];

fruits.push("grape");

console.log(fruits);
```

### Output

```text
["apple", "banana", "orange", "grape"]
```

---

# 2. pop()

The `pop()` method removes the last element from the array.

### Example

```javascript
fruits.pop();

console.log(fruits);
```

### Output

```text
["apple", "banana", "orange"]
```

---

# 3. unshift()

The `unshift()` method adds elements at the beginning of the array.

### Example

```javascript
fruits.unshift("kiwi");

console.log(fruits);
```

### Output

```text
["kiwi", "apple", "banana", "orange"]
```

---

# 4. shift()

The `shift()` method removes the first element from the array.

### Example

```javascript
fruits.shift();

console.log(fruits);
```

### Output

```text
["apple", "banana", "orange"]
```

---

# 5. slice()

The `slice()` method creates a new array from the selected portion of an existing array.

### Syntax

```javascript
array.slice(startIndex, endIndex)
```

Note:

* Start Index → Included
* End Index → Excluded

### Example

```javascript
var slicedFruits = fruits.slice(1, 3);

console.log(slicedFruits);
```

### Output

```text
["banana", "orange"]
```

---

# 6. splice()

The `splice()` method is used to:

* Add elements
* Remove elements
* Replace elements

### Example

```javascript
fruits.splice(1, 1, "grapefruit");

console.log(fruits);
```

### Output

```text
["apple", "grapefruit", "orange"]
```

### Explanation

```javascript
splice(1,1,"grapefruit")
```

means:

* Start from index 1
* Remove 1 element
* Insert "grapefruit"

---

# 7. delete Operator

The delete operator removes the value at a specific index.

### Example

```javascript
delete fruits[2];

console.log(fruits);
```

### Output

```text
["apple", "grapefruit", empty]
```

or

```text
["apple", "grapefruit", undefined]
```

### Note

The delete operator:

* Does not change array length.
* Only removes the value.
* Creates an empty slot.

---

## Replacing Deleted Value

### Example

```javascript
fruits[2] = "melon";

console.log(fruits);
```

### Output

```text
["apple", "grapefruit", "melon"]
```

---

# Complete Program

## HTML File

### Common.html

```html
<!DOCTYPE html>
<html lang="en">

<head>

    <title>Arrays in JavaScript</title>

</head>

<body>

    <h1 id="data"></h1>

    <script src="Arrays.js"></script>

</body>

</html>
```

---

## JavaScript File

### Arrays.js

```javascript
var ar = [1, 2, 3, 4, 5];

document.getElementById("data").innerHTML = ar;
```

---

## Important Array Properties

### length

Returns the number of elements in the array.

Example:

```javascript
var ar = [10, 20, 30, 40];

console.log(ar.length);
```

Output:

```text
4
```

---

## Important Notes

1. Arrays are zero indexed.
2. Arrays can store different data types.
3. Arrays are special types of Objects.
4. `typeof(array)` returns `"object"`.
5. `push()` adds elements at the end.
6. `pop()` removes the last element.
7. `unshift()` adds elements at the beginning.
8. `shift()` removes the first element.
9. `slice()` creates a new array.
10. `splice()` modifies the original array.
11. `delete` removes the value but not the index.

---

## Summary

Arrays are one of the most important data structures in JavaScript.

They are used to:

* Store multiple values
* Manage collections of data
* Process lists of records
* Manipulate dynamic data efficiently

JavaScript provides many built-in methods such as:

* push()
* pop()
* shift()
* unshift()
* slice()
* splice()

Mastering arrays is essential for learning advanced JavaScript concepts like Objects, DOM Manipulation, ES6 Features, and Frameworks such as React and Angular.
