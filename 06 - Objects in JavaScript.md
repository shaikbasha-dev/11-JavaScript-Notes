# Objects in JavaScript

## Introduction

An **Object** in JavaScript is a collection of properties stored in the form of **key-value pairs**.

Objects are used to represent real-world entities such as:

* Student
* Employee
* Car
* Product
* Bank Account

Each property of an object consists of:

```javascript
key : value
```

Example:

```javascript
firstname : "John"
age : 30
```

Here,

* `firstname` is the key.
* `"John"` is the value.

---

## Ways to Create Objects in JavaScript

Objects can be created in three different ways:

1. Literal Way
2. Constructor Function Way
3. Using new Keyword

---

# 1. Literal Way

This is the simplest and most commonly used method for creating objects.

### Syntax

```javascript
var objectName = {

    key1 : value1,

    key2 : value2

}
```

### Example

```javascript
var details = {

    firstname : "John",

    lastname : "Doe",

    age : 30

}

console.log(details);

console.log(details.firstname);
```

### Output

```text
{ firstname: "John", lastname: "Doe", age: 30 }

John
```

### Explanation

* `details` is an object.
* `firstname`, `lastname`, and `age` are properties.
* We can access properties using:

```javascript
details.firstname
```

or

```javascript
details["firstname"]
```

---

# 2. Constructor Function Way

A function can also be used to create objects.

### Example

```javascript
var fun = function(Wish){

    console.log(Wish);

}

fun("Good Morning");
```

### Output

```text
Good Morning
```

### Explanation

* `fun` is a function expression.
* `"Good Morning"` is passed as an argument.
* The function prints the value using `console.log()`.

> Note:
>
> This example demonstrates a function.
>
> It is not creating an object yet.
>
> Constructor functions are generally used with the `new` keyword.

---

# 3. Using new Keyword

The `new` keyword creates a new object from a constructor function.

### Example

```javascript
var fullname = function(fname, lname){

    this.fname = fname;

    this.lname = lname;

}

var res = new fullname("John", "Doe");

console.log(res);
```

### Output

```text
fullname { fname: 'John', lname: 'Doe' }
```

### Explanation

* `this.fname = fname`

Stores the first name inside the object.

* `this.lname = lname`

Stores the last name inside the object.

* `new fullname("John","Doe")`

Creates a new object.

---

## Accessing Object Properties

Properties can be accessed in two ways.

### Dot Notation

```javascript
console.log(res.fname);
```

Output:

```text
John
```

---

### Bracket Notation

```javascript
console.log(res["lname"]);
```

Output:

```text
Doe
```

---

## Adding New Properties

Properties can be added after object creation.

Example:

```javascript
res.age = 25;

console.log(res);
```

Output:

```text
fullname {

fname: "John",

lname: "Doe",

age: 25

}
```

---

## Modifying Properties

Example:

```javascript
res.age = 30;

console.log(res.age);
```

Output:

```text
30
```

---

## Deleting Properties

Example:

```javascript
delete res.age;

console.log(res);
```

Output:

```text
fullname {

fname: "John",

lname: "Doe"

}
```

---

## typeof Operator with Objects

Example:

```javascript
console.log(typeof(res));
```

Output:

```text
object
```

---

## Complete Program

### HTML File

**Common.html**

```html
<!DOCTYPE html>
<html lang="en">

<head>

    <title>Objects in JavaScript</title>

    <script src="Objects.js"></script>

</head>

<body>

</body>

</html>
```

---

### JavaScript File

**Objects.js**

```javascript
var details = {

    firstname : "John",

    lastname : "Doe",

    age : 30

}

console.log(details);

console.log(details.firstname);


var fullname = function(fname, lname){

    this.fname = fname;

    this.lname = lname;

}

var res = new fullname("John","Doe");

console.log(res);

console.log(res.fname);

console.log(res.lname);
```

---

## Important Points

1. Objects store data in key-value pairs.
2. Objects are mutable.
3. Properties can be added, modified, and deleted.
4. Objects can contain:

   * Strings
   * Numbers
   * Boolean values
   * Arrays
   * Functions
   * Other Objects
5. `typeof(object)` returns `"object"`.

---

## Summary

Objects are one of the most important features of JavaScript.

They are used to:

* Store related data together.
* Represent real-world entities.
* Build complex applications.
* Work with JSON data.
* Create classes and objects in Object-Oriented Programming.

Understanding objects is essential because JavaScript is an Object-Oriented Programming language, and most modern frameworks such as React, Angular, and Node.js heavily rely on objects.
