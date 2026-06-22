# Data Types in JavaScript

## Introduction

Data Types specify the type of value that a variable can hold.

JavaScript is a **Dynamically Typed Language**, which means the data type of a variable is determined automatically at runtime based on the value assigned to it.

Example:

```javascript
let name = "Basha";   // String
let age = 25;         // Number
let status = true;    // Boolean
```

---

## Types of Data Types in JavaScript

JavaScript Data Types are classified into two categories:

1. Primitive Data Types
2. Non-Primitive Data Types

---

## 1. Primitive Data Types

Primitive data types are simple data types that store a single value.

The Primitive Data Types are:

* String
* Number
* Boolean
* Undefined
* Null

---

### a. String Data Type

A String is a sequence of characters enclosed within:

* Double Quotes `" "`
* Single Quotes `' '`
* Backticks `` ` ` ``

#### Example

```javascript
var firstName = "John";

console.log(firstName);
console.log(typeof(firstName));

var middleName = 'Doe';

console.log(middleName);
console.log(typeof(middleName));
```

#### Output

```text
John
string

Doe
string
```

---

### b. Number Data Type

The Number data type stores:

* Integer values
* Floating-point values

#### Example

```javascript
var age = 30;

console.log(age);
console.log(typeof(age));

var percentage = 85.5;

console.log(percentage);
console.log(typeof(percentage));
```

#### Output

```text
30
number

85.5
number
```

---

### c. Boolean Data Type

Boolean stores only two values:

* true
* false

#### Example

```javascript
var isMarried = true;

console.log(isMarried);
console.log(typeof(isMarried));

var pass = false;

console.log(pass);
console.log(typeof(pass));
```

#### Output

```text
true
boolean

false
boolean
```

---

### d. Undefined Data Type

A variable that is declared but not assigned any value is called **Undefined**.

#### Example

```javascript
var myVariable;

console.log(myVariable);
console.log(typeof(myVariable));

var anotherVariable = undefined;

console.log(anotherVariable);
console.log(typeof(anotherVariable));
```

#### Output

```text
undefined
undefined

undefined
undefined
```

---

### e. Null Data Type

Null represents the intentional absence of a value.

#### Example

```javascript
var emptyValue = null;

console.log(emptyValue);
console.log(typeof(emptyValue));

var anotherEmptyValue = null;

console.log(anotherEmptyValue);
console.log(typeof(anotherEmptyValue));
```

#### Output

```text
null
object

null
object
```

> **Important Note:**
>
> In JavaScript, `typeof null` returns `"object"`.
>
> This is a historical bug in JavaScript that has been kept for backward compatibility.

---

## 2. Non-Primitive Data Types

Non-Primitive Data Types are complex data structures that can store multiple values.

The Non-Primitive Data Types are:

* Object
* Array

---

### a. Object Data Type

An Object is a collection of key-value pairs.

#### Example

```javascript
var person = {

    name: "John",
    age: 30,
    isMarried: true

};

console.log(person);

console.log(typeof(person));
```

#### Output

```text
{
 name: 'John',
 age: 30,
 isMarried: true
}

object
```

---

#### Another Example

```javascript
var anotherPerson = {

    name: "Jane",
    age: 25,
    isMarried: false

};

console.log(anotherPerson);

console.log(typeof(anotherPerson));
```

#### Output

```text
{
 name: 'Jane',
 age: 25,
 isMarried: false
}

object
```

---

### b. Array Data Type

An Array is an ordered collection of values.

Arrays can store:

* Numbers
* Strings
* Booleans
* Objects
* Mixed Data Types

#### Example

```javascript
var numbers = [1, 2, 3, 4, 5];

console.log(numbers);

console.log(typeof(numbers));
```

#### Output

```text
[1, 2, 3, 4, 5]

object
```

---

#### Another Example

```javascript
var fruits = ["apple", "banana", "orange"];

console.log(fruits);

console.log(typeof(fruits));
```

#### Output

```text
['apple', 'banana', 'orange']

object
```

---

## Primitive vs Non-Primitive Data Types

| Primitive                         | Non-Primitive           |
| --------------------------------- | ----------------------- |
| Stores Single Value               | Stores Multiple Values  |
| Immutable                         | Mutable                 |
| Stored by Value                   | Stored by Reference     |
| Faster Access                     | Comparatively Slower    |
| Examples: String, Number, Boolean | Examples: Object, Array |

---

## Complete List of JavaScript Data Types

### Primitive Data Types

1. String
2. Number
3. Boolean
4. Undefined
5. Null

### Non-Primitive Data Types

1. Object
2. Array

---

## Important Notes

1. JavaScript is a Dynamically Typed Language.
2. `typeof()` is used to determine the data type of a variable.
3. Arrays are special types of Objects.
4. `typeof null` returns `"object"` because of a historical JavaScript bug.
5. Primitive values are stored by value.
6. Objects and Arrays are stored by reference.

---

## Summary

JavaScript supports two categories of data types:

* Primitive Data Types

  * String
  * Number
  * Boolean
  * Undefined
  * Null

* Non-Primitive Data Types

  * Object
  * Array

Understanding data types is fundamental for learning variables, operators, functions, objects, arrays, DOM manipulation, and advanced JavaScript concepts.
