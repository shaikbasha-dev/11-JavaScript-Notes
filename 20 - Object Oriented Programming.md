# Object Oriented Programming (OOP) in JavaScript

## 1. Introduction

Object Oriented Programming (OOP) is a programming paradigm that organizes code into objects and classes.

OOP helps developers:

* Reuse code
* Improve maintainability
* Achieve modularity
* Implement real-world entities
* Reduce code duplication

JavaScript supports Object Oriented Programming using:

1. Class
2. Constructor
3. Object
4. Inheritance
5. Exception Handling

---

## 2. Class in JavaScript

A **Class** is a blueprint used to create objects.

Syntax:

```javascript
class ClassName {

}
```

Example:

```javascript
class Details {

}
```

---

## 3. Constructor in JavaScript

A constructor is a special method used to initialize object properties.

Syntax:

```javascript
constructor(parameters){

}
```

The constructor executes automatically whenever an object is created.

---

## 4. Object in JavaScript

An Object is an instance of a class.

Syntax:

```javascript
var obj = new ClassName();
```

Example:

```javascript
var student = new Details();
```

---

## 5. Example 1: Class, Constructor and Object

### oop.html

```html
<!DOCTYPE html>
<html>
<head>
    <title>Object Oriented Programming in JavaScript</title>
</head>

<body>

<p id="cls"></p>

<script>

class Details {

    constructor(fname,lname) {

        this.fname = fname;
        this.lname = lname;
    }

    gender() {

        return "Male";
    }

}

var mydetails = new Details("Sachin","Tendulkar");

var r = mydetails.gender();

document.getElementById("cls").innerHTML =
mydetails.fname + " " +
mydetails.lname + " " +
r;

console.log(mydetails);

</script>

</body>
</html>
```

---

## Step-by-Step Explanation

### Class Details

```javascript
class Details
```

Creates a class named:

```text
Details
```

---

### Constructor

```javascript
constructor(fname,lname)
```

Receives:

* fname
* lname

and stores them using:

```javascript
this.fname = fname;

this.lname = lname;
```

---

### Method

```javascript
gender(){

return "Male";

}
```

Returns:

```text
Male
```

---

### Creating Object

```javascript
var mydetails =
new Details("Sachin","Tendulkar");
```

Creates:

```text
Object of Details Class
```

---

### Calling Method

```javascript
mydetails.gender();
```

Output:

```text
Male
```

---

### Output

```text
Sachin Tendulkar Male
```

---

## 6. Inheritance in JavaScript

Inheritance means:

```text
Acquiring properties and methods of one class into another class.
```

JavaScript uses:

```javascript
extends
```

keyword.

---

## Example 2: Inheritance

### inh.html

```html
<!DOCTYPE html>

<html>

<head>

<title>Inheritance in JavaScript</title>

</head>

<body>

<script>

class Parent {

constructor(drink){

this.normalWater = drink;

}

display(){

return "I will have normal " + this.normalWater;

}

}

class Child extends Parent {

constructor(drink,food){

super(drink);

this.eat = food;

}

outfun(){

return this.display()

+ " I will eat "

+ this.eat;

}

}

var fam = new Child("Water","Bread");

console.log(fam.outfun());

</script>

</body>

</html>
```

---

## Explanation

### Parent Class

```javascript
class Parent
```

Contains:

* constructor()
* display()

---

### Child Class

```javascript
class Child extends Parent
```

The Child class inherits:

* normalWater property
* display() method

from Parent class.

---

### super()

```javascript
super(drink);
```

Calls parent class constructor.

---

### Object Creation

```javascript
var fam =
new Child("Water","Bread");
```

Creates Child object.

---

### Output

```text
I will have normal Water I will eat Bread
```

---

## OOP Concepts

### 1. Encapsulation

Wrapping variables and methods together inside a class.

Example:

```javascript
class Student {

constructor(name){

this.name=name;

}

}
```

---

### 2. Inheritance

Acquiring properties of parent class.

Example:

```javascript
class Child extends Parent
```

---

### 3. Polymorphism

Same method behaves differently.

Example:

```javascript
class Animal{

sound(){

console.log("Animal Sound");

}

}
```

---

### 4. Abstraction

Hiding internal implementation details.

Users only use methods without knowing internal logic.

---

## 7. Exception Handling

Exception handling is used to handle runtime errors.

JavaScript uses:

```text
try

catch

finally
```

---

## Syntax

```javascript
try{

// risky code

}

catch(e){

// handle exception

}

finally{

// always executed

}
```

---

## Example 3: Exception Handling

### excep.html

```html
<!DOCTYPE html>

<html>

<head>

<title>Exception Handling</title>

<script>

function fun(){

var str="Sachin";

try{

var low=str.toLowerCase();

alert(low);

}

catch(e){

alert("Exception is handled");

}

finally{

alert("Finally block is executed");

}

}

</script>

</head>

<body>

<h1>Exception Handling</h1>

<input type="button"

value="Click"

onclick="fun()">

</body>

</html>
```

---

## Explanation

### try Block

```javascript
try{

var low=str.toLowerCase();

}
```

Executes risky code.

---

### catch Block

```javascript
catch(e)
```

Handles exception if error occurs.

---

### finally Block

```javascript
finally{

alert("Finally block is executed");

}
```

Always executes.

Whether:

* Error occurs OR
* Error does not occur

---

## Output

First Alert:

```text
sachin
```

Second Alert:

```text
Finally block is executed
```

---

## Difference Between Class and Object

| Class                  | Object             |
| ---------------------- | ------------------ |
| Blueprint              | Instance           |
| Logical entity         | Physical entity    |
| No memory allocated    | Memory allocated   |
| Used to create objects | Created from class |

---

## Difference Between Constructor and Method

| Constructor            | Method                   |
| ---------------------- | ------------------------ |
| Special function       | Normal function          |
| Executes automatically | Called manually          |
| Initializes object     | Performs operation       |
| Only one constructor   | Multiple methods allowed |

---

## Interview Questions

### Q1. What is OOP?

**Answer:**

Object Oriented Programming is a programming paradigm that organizes code into classes and objects.

---

### Q2. What are the four pillars of OOP?

**Answer:**

1. Encapsulation
2. Inheritance
3. Polymorphism
4. Abstraction

---

### Q3. What is a class?

**Answer:**

A class is a blueprint used to create objects.

---

### Q4. What is an object?

**Answer:**

An object is an instance of a class.

Example:

```javascript
var obj = new Student();
```

---

### Q5. Which keyword is used for inheritance?

**Answer:**

```javascript
extends
```

Example:

```javascript
class Child extends Parent
```

---

### Q6. Why do we use super()?

**Answer:**

super() calls the constructor of the parent class.

---

### Q7. What is exception handling?

**Answer:**

Exception handling is a mechanism used to handle runtime errors gracefully using:

```text
try

catch

finally
```

---

### Q8. Does finally always execute?

**Answer:**

Yes.

The finally block always executes whether an exception occurs or not.

---

## Important Points

1. JavaScript supports OOP.
2. Class is a blueprint.
3. Object is an instance of a class.
4. Constructor initializes objects.
5. extends is used for inheritance.
6. super() calls parent constructor.
7. try handles risky code.
8. catch handles exceptions.
9. finally always executes.
10. Classes were introduced in ES6 (2015).

---

## Summary

Object Oriented Programming in JavaScript provides a structured way to organize code using classes and objects. JavaScript supports constructors, inheritance, encapsulation, and exception handling, enabling developers to build reusable, modular, and maintainable applications. Modern JavaScript uses ES6 classes, making OOP syntax simpler and easier to understand while still relying on JavaScript's prototype-based inheritance internally.
