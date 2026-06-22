# Functions in JavaScript (User Defined Functions)

## Introduction

A **Function** is a reusable block of code that performs a specific task. Functions help developers avoid code repetition and improve code reusability.

Functions can:

* Accept input values called **Parameters**
* Perform calculations or operations
* Return a value
* Be called multiple times

---

# Types of User Defined Functions in JavaScript

1. Function Declaration
2. Function Expression
3. Anonymous Function
4. Constructor Function
5. Arrow Function

---

## 1. Function Declaration

A Function Declaration is created using the `function` keyword followed by a function name.

### Syntax

```javascript
function functionName(){

    // Statements

}
```

### Example

**function.js**

```javascript
function addition(){

    var a = 10;
    var b = 20;

    console.log(a+b);

}

addition();
```

### Output

```text
30
```

### Explanation

* `function` → Keyword used to declare a function.
* `addition()` → Function Name.
* The function contains two variables:

  * a = 10
  * b = 20
* `console.log(a+b)` prints their sum.
* `addition();` calls the function.

---

## 2. Function Expression

A Function Expression is a function assigned to a variable.

### Syntax

```javascript
var variableName = function(){

    // Statements

}
```

### Example

**functionExpression.js**

```javascript
var disp = function sub(){

    var a = 10;
    var b = 20;

    console.log(a-b);

}

disp();
```

### Output

```text
-10
```

### Explanation

* Function is assigned to variable `disp`.
* `sub` is the internal function name.
* The function can be called using:

```javascript
disp();
```

---

## 3. Anonymous Function

An Anonymous Function is a function without a name.

### Syntax

```javascript
var variableName = function(){

}
```

### Example

**anonymousFunction.js**

```javascript
var disp = function(a,b){

    console.log(a/b);

}

disp(10,20);
```

### Output

```text
0.5
```

### Explanation

* The function has no name.
* It accepts two parameters:

  * a
  * b
* `10/20` gives:

```text
0.5
```

---

## 4. Constructor Function

A Constructor Function is used to create objects.

It is called using the **new** keyword.

### Syntax

```javascript
function Student(name,age){

    this.name = name;
    this.age = age;

}

var obj = new Student("John",25);
```

---

### Example

**constructorFunction.js**

```javascript
var a=0;
var b=0;
var c=0;

var disp = function example(a,b,c){

    this.a=a;
    this.b=b;
    this.c=c;

}

var res = new disp(10,20,30);

console.log(res.a);
console.log(res.b);
console.log(res.c);
```

### Output

```text
10
20
30
```

### Explanation

* `this.a=a` stores values inside the object.
* `new disp()` creates a new object.
* `res.a`, `res.b`, and `res.c` access object properties.

---

## 5. Arrow Function

Arrow Function was introduced in **ES6 (ECMAScript 2015)**.

It provides a shorter syntax for writing functions.

### Syntax

```javascript
var disp = ()=>{

    Statements

}
```

---

### Example 1

```javascript
var disp = ()=>console.log("Arrow Function");

disp();
```

### Output

```text
Arrow Function
```

---

### Example 2

**arrowFunction.js**

```javascript
var mul = (a,b,c)=>{

    var res = a*b*c;

    return res;

}

var disp = mul(10,20,30);

console.log(disp);
```

### Output

```text
6000
```

### Explanation

* Arrow function accepts three parameters:

  * a
  * b
  * c

Calculation:

```text
10 × 20 × 30 = 6000
```

The value is returned and stored in:

```javascript
var disp
```

---

# Difference Between Function Declaration and Function Expression

| Function Declaration             | Function Expression                 |
| -------------------------------- | ----------------------------------- |
| Declared using function name     | Assigned to a variable              |
| Can be called before declaration | Cannot be called before declaration |
| Has a function name              | May be anonymous                    |
| Hoisted completely               | Partially hoisted                   |

---

# Difference Between Normal Function and Arrow Function

| Normal Function       | Arrow Function                |
| --------------------- | ----------------------------- |
| Uses function keyword | Uses => operator              |
| Has its own this      | Does not have its own this    |
| Supports constructor  | Cannot be used as constructor |
| More verbose          | Short and concise             |

---

# Important Points

1. Functions improve code reusability.
2. A function can accept parameters and return values.
3. Function Expressions are assigned to variables.
4. Anonymous Functions do not have names.
5. Constructor Functions create objects using `new`.
6. Arrow Functions were introduced in ES6.
7. Arrow Functions provide shorter syntax.
8. Arrow Functions do not have their own `this`.

---

# Summary

Functions are one of the most important building blocks of JavaScript. They allow developers to organize code into reusable blocks, improve maintainability, and reduce code duplication. JavaScript supports multiple types of functions including Function Declaration, Function Expression, Anonymous Function, Constructor Function, and Arrow Function. Understanding these functions is essential for DOM Manipulation, Event Handling, Object-Oriented Programming, and modern JavaScript development.
