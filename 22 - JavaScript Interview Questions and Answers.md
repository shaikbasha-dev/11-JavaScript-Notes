# Part 1: Introduction to JavaScript - Interview Questions and Answers

## Introduction to JavaScript - Interview Questions and Answers

### Q1. What is JavaScript?

**Answer:**
JavaScript is a high-level, interpreted, dynamically typed programming language used to create dynamic and interactive web applications.

---

### Q2. Who developed JavaScript?

**Answer:**
Brendan Eich developed JavaScript in 1995 while working at Netscape Communications Corporation.

---

### Q3. In how many days was JavaScript created?

**Answer:**
JavaScript was created in just **10 days** by Brendan Eich.

---

### Q4. What were the previous names of JavaScript?

**Answer:**
1. Mocha
2. LiveScript
3. JavaScript

---

### Q5. What is ECMAScript?

**Answer:**
ECMAScript (ECMA) is the standard specification of JavaScript maintained by ECMA International.

---

### Q6. What does ECMA stand for?

**Answer:**
European Computer Manufacturers Association.

---

### Q7. What is ES6?

**Answer:**
ES6 (ECMAScript 2015) is a major version of JavaScript that introduced:

- let
- const
- Arrow Functions
- Classes
- Template Literals
- Promises

---

### Q8. Is JavaScript a compiled or interpreted language?

**Answer:**
JavaScript is primarily an interpreted language.

Modern browsers use Just-In-Time (JIT) compilation for better performance.

---

### Q9. Is JavaScript case-sensitive?

**Answer:**
Yes.

Example:

```javascript
var age = 20;
var Age = 30;

console.log(age); //20
console.log(Age); //30
````

Both variables are different.

---

### Q10. Is JavaScript client-side or server-side?

**Answer:**
JavaScript can be used for:

1. Client-side development
2. Server-side development using Node.js

---

### Q11. What is client-side JavaScript?

**Answer:**
JavaScript executed inside the browser is called client-side JavaScript.

Examples:

* Form validation
* DOM manipulation
* Animations
* Event handling

---

### Q12. What is server-side JavaScript?

**Answer:**
JavaScript executed on the server using Node.js is called server-side JavaScript.

It is used for:

* APIs
* Database operations
* Authentication
* Backend development

---

### Q13. What are the features of JavaScript?

**Answer:**

1. Lightweight
2. Interpreted
3. Dynamically typed
4. Object-oriented
5. Functional programming support
6. Event-driven
7. Platform independent

---

### Q14. Why is JavaScript called a dynamically typed language?

**Answer:**

Because the data type is decided at runtime.

Example:

```javascript
var a = 10;       // Number

a = "Hello";      // String

a = true;         // Boolean
```

The same variable can hold different data types.

---

### Q15. Which extension is used for JavaScript files?

**Answer:**

```text
.js
```

Example:

```text
demo.js
```

---

### Q16. In how many ways can JavaScript be included in HTML?

**Answer:**

Three ways:

1. Inside `<head>`

```html
<head>
<script>
document.write("Hello");
</script>
</head>
```

---

2. Inside `<body>`

```html
<body>

<script>
document.write("Hello");
</script>

</body>
```

---

3. External File

```html
<script src="demo.js"></script>
```

---

### Q17. Which is the preferred way to include JavaScript?

**Answer:**

External JavaScript file.

Example:

```html
<script src="demo.js"></script>
```

Advantages:

* Reusability
* Better maintenance
* Cleaner code
* Faster loading

---

### Q18. Why should we run HTML files instead of JS files directly?

**Answer:**

Because JavaScript executes within the context of an HTML document.

The browser:

1. Loads HTML
2. Parses HTML
3. Executes JavaScript
4. Renders the page

---

### Q19. What does document.write() do?

**Answer:**

It writes content directly to the HTML document.

Example:

```javascript
document.write("Welcome to JavaScript");
```

Output:

```text
Welcome to JavaScript
```

---

### Q20. Why is document.write() not recommended nowadays?

**Answer:**

Because:

1. It can overwrite the page after loading.
2. It affects performance.
3. DOM methods are better alternatives.

Modern alternatives:

```javascript
innerHTML

textContent

createElement()

appendChild()
```

---

## Important Viva Questions

### Q21. Is JavaScript an object-oriented language?

**Answer:**
Yes.

JavaScript supports:

* Object-Oriented Programming
* Functional Programming
* Event-Driven Programming

---

### Q22. Is JavaScript synchronous or asynchronous?

**Answer:**

By default:

```text
Synchronous
```

But it also supports:

```text
Asynchronous Programming
```

using:

* Callbacks
* Promises
* Async/Await

---

### Q23. Can JavaScript run without a browser?

**Answer:**

Yes.

Using:

```text
Node.js
```

---

### Q24. Which browsers support JavaScript?

**Answer:**

All modern browsers:

* Google Chrome
* Firefox
* Microsoft Edge
* Safari
* Opera

---

### Q25. What are popular JavaScript frameworks and libraries?

**Answer:**

Libraries:

* jQuery
* React

Frameworks:

* Angular
* Vue.js
* Express.js

---

## Frequently Asked Fresher Interview Question

### Q26. Why is JavaScript important in Web Development?

**Answer:**

JavaScript is important because it provides:

* Dynamic webpages
* Form validation
* Event handling
* DOM manipulation
* Animations
* AJAX calls
* Interactive UI
* Frontend and Backend development

JavaScript is considered one of the three core technologies of web development:

1. HTML → Structure
2. CSS → Styling
3. JavaScript → Behavior

---

# Part 2: Variables & Keywords in JavaScript - Interview Questions and Answers

## Variables & Keywords in JavaScript - Interview Questions and Answers

### Q1. What is a variable in JavaScript?

**Answer:**
A variable is a container used to store data values in memory.

Example:

```javascript
var age = 25;
````

---

### Q2. Which keywords are used to declare variables in JavaScript?

**Answer:**

There are three keywords:

1. var
2. let
3. const

Example:

```javascript
var name = "John";

let age = 25;

const PI = 3.14;
```

---

### Q3. What is var in JavaScript?

**Answer:**

`var` is used to declare variables.

Characteristics:

* Function Scoped
* Can be redeclared
* Can be reassigned

Example:

```javascript
var a = 10;

var a = 20;

a = 30;
```

---

### Q4. What is let in JavaScript?

**Answer:**

`let` is used to declare block-scoped variables.

Characteristics:

* Block Scoped
* Cannot redeclare
* Can reassign

Example:

```javascript
let age = 25;

age = 30;
```

---

### Q5. What is const in JavaScript?

**Answer:**

`const` is used to declare constants.

Characteristics:

* Block Scoped
* Cannot redeclare
* Cannot reassign

Example:

```javascript
const PI = 3.14;
```

---

### Q6. What is the difference between var, let and const?

| var            | let         | const       |
| -------------- | ----------- | ----------- |
| Function Scope | Block Scope | Block Scope |
| Redeclare ✓    | Redeclare ✗ | Redeclare ✗ |
| Reassign ✓     | Reassign ✓  | Reassign ✗  |

---

### Q7. What is block scope?

**Answer:**

A variable declared inside `{ }` can be accessed only inside that block.

Example:

```javascript
{
let age = 20;
}

console.log(age);
```

Output:

```text
ReferenceError
```

---

### Q8. What is function scope?

**Answer:**

A variable declared using `var` inside a function is accessible throughout that function.

Example:

```javascript
function demo(){

var a=10;

console.log(a);

}

demo();
```

---

### Q9. Can var be redeclared?

**Answer:**

Yes.

```javascript
var a=10;

var a=20;
```

Valid.

---

### Q10. Can let be redeclared?

**Answer:**

No.

```javascript
let a=10;

let a=20;
```

Output:

```text
SyntaxError
```

---

### Q11. Can const be redeclared?

**Answer:**

No.

```javascript
const PI=3.14;

const PI=22/7;
```

Output:

```text
SyntaxError
```

---

### Q12. Can var be reassigned?

**Answer:**

Yes.

```javascript
var age=25;

age=30;
```

---

### Q13. Can let be reassigned?

**Answer:**

Yes.

```javascript
let age=25;

age=35;
```

---

### Q14. Can const be reassigned?

**Answer:**

No.

```javascript
const PI=3.14;

PI=22/7;
```

Output:

```text
TypeError
```

---

### Q15. Is JavaScript statically typed?

**Answer:**

No.

JavaScript is dynamically typed.

---

### Q16. What is dynamically typed language?

**Answer:**

A language where datatype is assigned during runtime.

Example:

```javascript
var x=10;

x="Hello";

x=true;
```

---

### Q17. Is datatype compulsory during variable declaration?

**Answer:**

No.

Example:

```javascript
var age=25;

let name="John";

const status=true;
```

No datatype is specified.

---

### Q18. What will be the output?

```javascript
var x;

console.log(x);
```

Answer:

```text
undefined
```

---

### Q19. What will be the output?

```javascript
var a=10;

var a=20;

console.log(a);
```

Answer:

```text
20
```

---

### Q20. What will be the output?

```javascript
{
var x=100;
}

console.log(x);
```

Answer:

```text
100
```

Because var is not block scoped.

---

### Q21. What will be the output?

```javascript
{
let x=100;
}

console.log(x);
```

Answer:

```text
ReferenceError
```

---

### Q22. What will be the output?

```javascript
{
const PI=3.14;
}

console.log(PI);
```

Answer:

```text
ReferenceError
```

---

### Q23. Which variable keyword is recommended in modern JavaScript?

**Answer:**

Preference order:

```text
1. const
2. let
3. var
```

---

### Q24. When should we use let?

**Answer:**

Use `let` when:

* Value changes later
* Loop counters
* Temporary variables

Example:

```javascript
let count=0;

count++;
```

---

### Q25. When should we use const?

**Answer:**

Use const when value should remain constant.

Examples:

```javascript
const PI=3.14;

const country="India";

const company="OpenAI";
```

---

### Q26. Why is var not preferred in modern JavaScript?

**Answer:**

Because:

* No block scope
* Allows redeclaration
* Can create bugs
* Hoisting confusion

Hence developers prefer:

```text
const → First Choice

let → Second Choice

var → Avoid whenever possible
```

---

### Frequently Asked Fresher Interview Question

### Q27. Explain var, let and const with one example.

```javascript
var a=10;
var a=20;       // Allowed

let b=30;
// let b=40;    // Error

b=50;           // Allowed

const PI=3.14;

// PI=22/7;     // Error
```

**Conclusion:**

* var → Function Scope
* let → Block Scope + Reassignable
* const → Block Scope + Constant

---

# Part 3: Data Types in JavaScript - Interview Questions and Answers

## Data Types in JavaScript - Interview Questions and Answers

### Q1. What is a Data Type?

**Answer:**
A data type specifies the type of value that a variable can store.

Examples:

- String
- Number
- Boolean
- Null
- Undefined
- Object
- Array

---

### Q2. How many types of data types are available in JavaScript?

**Answer:**

There are two categories:

1. Primitive Data Types
2. Non-Primitive Data Types

---

### Q3. What are Primitive Data Types?

**Answer:**

Primitive Data Types are basic data types that store a single value.

They are:

1. String
2. Number
3. Boolean
4. Null
5. Undefined

---

### Q4. What are Non-Primitive Data Types?

**Answer:**

Non-Primitive Data Types store collections of values.

They are:

1. Object
2. Array

---

### Q5. What is a String in JavaScript?

**Answer:**

A String is a sequence of characters enclosed in:

- Double Quotes ""
- Single Quotes ''
- Backticks ``

Example:

```javascript
var name = "John";

var city = 'Hyderabad';

var company = `OpenAI`;
````

---

### Q6. What is the output?

```javascript
var name="John";

console.log(typeof(name));
```

**Answer**

```text
string
```

---

### Q7. What is Number data type?

**Answer:**

The Number datatype stores:

* Integers

```javascript
10
```

* Floating Point Numbers

```javascript
99.99
```

Example:

```javascript
var age=25;

var marks=95.5;
```

---

### Q8. What is the output?

```javascript
var age=25;

console.log(typeof(age));
```

**Answer**

```text
number
```

---

### Q9. What is Boolean datatype?

**Answer:**

Boolean stores only two values:

```javascript
true

false
```

Example:

```javascript
var isMarried=true;

var pass=false;
```

---

### Q10. What is the output?

```javascript
var pass=true;

console.log(typeof(pass));
```

**Answer**

```text
boolean
```

---

### Q11. What is Undefined?

**Answer:**

A variable declared but not assigned any value is called Undefined.

Example:

```javascript
var a;

console.log(a);
```

Output:

```text
undefined
```

---

### Q12. What is Null?

**Answer:**

Null represents an intentional absence of value.

Example:

```javascript
var x=null;
```

---

### Q13. What is the output?

```javascript
console.log(typeof(null));
```

**Answer**

```text
object
```

**Note:**

This is a historical bug in JavaScript.

---

### Q14. Difference between null and undefined?

| null                   | undefined              |
| ---------------------- | ---------------------- |
| Intentionally empty    | Not assigned           |
| Object type            | Undefined type         |
| Assigned by programmer | Assigned by JavaScript |

---

### Q15. What is an Object?

**Answer:**

An object stores data in key-value pairs.

Example:

```javascript
var person={

name:"John",

age:25,

city:"Mumbai"

};
```

---

### Q16. What is the output?

```javascript
var person={

name:"John",

age:25

}

console.log(typeof(person));
```

**Answer**

```text
object
```

---

### Q17. What is an Array?

**Answer:**

An array stores multiple values in a single variable.

Example:

```javascript
var arr=[10,20,30,40];
```

---

### Q18. What is the output?

```javascript
var arr=[1,2,3];

console.log(typeof(arr));
```

**Answer**

```text
object
```

Arrays are internally objects in JavaScript.

---

### Q19. Can JavaScript arrays store mixed datatypes?

**Answer:**

Yes.

Example:

```javascript
var arr=[

1,

"Hello",

true,

{age:25},

[10,20]

];
```

---

### Q20. What is typeof operator?

**Answer:**

typeof returns the datatype of a variable.

Example:

```javascript
typeof("Hello")
```

Output

```text
string
```

---

### Q21. Output?

```javascript
console.log(typeof(100));
```

Answer:

```text
number
```

---

### Q22. Output?

```javascript
console.log(typeof(true));
```

Answer:

```text
boolean
```

---

### Q23. Output?

```javascript
console.log(typeof(undefined));
```

Answer:

```text
undefined
```

---

### Q24. Output?

```javascript
console.log(typeof([]));
```

Answer:

```text
object
```

---

### Q25. Output?

```javascript
console.log(typeof({}));
```

Answer:

```text
object
```

---

### Q26. Is JavaScript strongly typed or weakly typed?

**Answer:**

JavaScript is:

```text
Weakly Typed Language
```

Because automatic type conversion is possible.

Example:

```javascript
console.log("10"+20);
```

Output:

```text
1020
```

---

### Q27. Why is JavaScript called dynamically typed?

**Answer:**

Because a variable can hold different data types at different times.

Example:

```javascript
var x=10;

x="Hello";

x=true;
```

The same variable stores:

* Number
* String
* Boolean

---

### Frequently Asked Fresher Interview Question

### Q28. List all JavaScript data types.

**Answer**

Primitive:

1. String

2. Number

3. Boolean

4. Null

5. Undefined

Non-Primitive:

6. Object

7. Array

---

### Q29. Which datatype is most commonly used in JavaScript?

**Answer**

Most commonly used datatypes are:

* String
* Number
* Boolean
* Object
* Array

---

### Q30. Which datatype is returned by typeof for arrays?

**Answer**

```javascript
typeof([1,2,3])
```

Output:

```text
object
```

Even though it is an Array, typeof returns object.

---


# Part 4: Type Casting in JavaScript - Interview Questions and Answers

## Type Casting in JavaScript - Interview Questions and Answers

### Q1. What is Type Casting in JavaScript?

**Answer:**

Type Casting (Type Conversion) is the process of converting one data type into another data type.

Example:

```javascript
var str="123";

var num=Number(str);

console.log(num);
````

Output:

```text
123
```

---

### Q2. How many types of Type Casting are available in JavaScript?

**Answer:**

There are two types:

1. Implicit Type Casting
2. Explicit Type Casting

---

### Q3. What is Implicit Type Casting?

**Answer:**

Implicit Type Casting means JavaScript automatically converts one datatype into another.

Example:

```javascript
var result="Age : "+25;

console.log(result);
```

Output:

```text
Age : 25
```

Here 25 is automatically converted into String.

---

### Q4. What is Explicit Type Casting?

**Answer:**

Explicit Type Casting means programmer manually converts datatype.

Example:

```javascript
var str="100";

var num=Number(str);

console.log(num);
```

Output:

```text
100
```

---

### Q5. Which functions are used for Explicit Type Casting?

**Answer:**

1. Number()

2. String()

3. Boolean()

4. parseInt()

5. parseFloat()

---

### Q6. How do you convert String to Number?

**Answer:**

Using Number()

Example:

```javascript
var str="500";

var num=Number(str);

console.log(num);
```

Output:

```text
500
```

---

### Q7. Output?

```javascript
console.log(Number("100"));
```

Answer:

```text
100
```

---

### Q8. Output?

```javascript
console.log(Number("Virat"));
```

Answer:

```text
NaN
```

NaN means:

```text
Not a Number
```

---

### Q9. Output?

```javascript
console.log(Number(""));
```

Answer:

```text
0
```

---

### Q10. Output?

```javascript
console.log(Number(" "));
```

Answer:

```text
0
```

---

### Q11. What is NaN?

**Answer**

NaN stands for:

```text
Not a Number
```

It is returned when a value cannot be converted into a valid number.

Example:

```javascript
Number("Hello")
```

Output:

```text
NaN
```

---

### Q12. What is the datatype of NaN?

```javascript
console.log(typeof(NaN));
```

Answer:

```text
number
```

---

### Q13. How do you convert Number to String?

**Answer**

Using:

1. String()

2. toString()

Example:

```javascript
var age=35;

var str=String(age);

console.log(str);
```

Output:

```text
"35"
```

---

### Q14. Output?

```javascript
console.log(String(100));
```

Answer:

```text
"100"
```

---

### Q15. Output?

```javascript
console.log(typeof(String(100)));
```

Answer:

```text
string
```

---

### Q16. How do you convert String to Boolean?

**Answer**

Using Boolean()

Example:

```javascript
Boolean("Sachin")
```

Output:

```text
true
```

---

### Q17. Output?

```javascript
console.log(Boolean(""));
```

Answer:

```text
false
```

Because empty string is falsy.

---

### Q18. Output?

```javascript
console.log(Boolean("JavaScript"));
```

Answer:

```text
true
```

Because non-empty strings are truthy.

---

### Q19. How do you convert Boolean to String?

**Answer**

Using:

```javascript
String(true)
```

Output:

```text
"true"
```

---

### Q20. Output?

```javascript
console.log(String(false));
```

Answer:

```text
"false"
```

---

### Q21. How do you convert Boolean to Number?

**Answer**

Using Number()

Example:

```javascript
Number(true)
```

Output:

```text
1
```

---

### Q22. Output?

```javascript
console.log(Number(false));
```

Answer:

```text
0
```

---

### Q23. How do you convert Number to Boolean?

**Answer**

Using Boolean()

Example:

```javascript
Boolean(10)
```

Output:

```text
true
```

---

### Q24. Output?

```javascript
console.log(Boolean(0));
```

Answer:

```text
false
```

Because zero is falsy.

---

### Q25. Output?

```javascript
console.log(Boolean(-10));
```

Answer:

```text
true
```

Because any non-zero number is truthy.

---

### Q26. What are Falsy Values in JavaScript?

**Answer**

Falsy values are:

```javascript
false

0

""

null

undefined

NaN
```

---

### Q27. What are Truthy Values in JavaScript?

**Answer**

Everything except falsy values.

Examples:

```javascript
"Hello"

100

-10

[]

{}

true
```

---

### Q28. What is parseInt()?

**Answer**

parseInt() converts string to integer.

Example:

```javascript
parseInt("123")
```

Output:

```text
123
```

---

### Q29. What is parseFloat()?

**Answer**

parseFloat() converts string into decimal number.

Example:

```javascript
parseFloat("99.99")
```

Output:

```text
99.99
```

---

### Q30. Difference between Number() and parseInt()?

| Number()                       | parseInt()            |
| ------------------------------ | --------------------- |
| Converts entire string         | Converts integer only |
| Returns NaN for invalid values | Reads numeric part    |
| Supports decimal               | Removes decimal       |

Example:

```javascript
Number("123abc")
```

Output:

```text
NaN
```

```javascript
parseInt("123abc")
```

Output:

```text
123
```

---

### Frequently Asked Fresher Interview Question

### Q31. Explain Type Casting with examples.

**Answer**

Type Casting is conversion of one datatype to another.

Two types:

1. Implicit

```javascript
"Age :"+25
```

Output:

```text
Age :25
```

2. Explicit

```javascript
Number("100")
```

Output:

```text
100
```

JavaScript provides:

* Number()
* String()
* Boolean()
* parseInt()
* parseFloat()

for explicit type conversion.

---


# Part 5: Arrays in JavaScript - Interview Questions and Answers

## Arrays in JavaScript - Interview Questions and Answers

### Q1. What is an Array in JavaScript?

**Answer:**

An Array is a collection of multiple values stored in a single variable.

Example:

```javascript
var arr = [10,20,30,40];
````

---

### Q2. Why do we use Arrays?

**Answer:**

Arrays are used to:

* Store multiple values
* Reduce number of variables
* Access values using index
* Perform searching and sorting

---

### Q3. Are JavaScript Arrays homogeneous or heterogeneous?

**Answer:**

JavaScript arrays are **heterogeneous**, meaning they can store different datatypes.

Example:

```javascript
var arr=[

100,

"Hello",

true,

{name:"John"},

[1,2,3]

];
```

---

### Q4. Is JavaScript Array zero indexed?

**Answer:**

Yes.

First element:

```javascript
arr[0]
```

Second element:

```javascript
arr[1]
```

---

### Q5. What is the output?

```javascript
var arr=[10,20,30];

console.log(arr[0]);
```

Answer:

```text
10
```

---

### Q6. What is the output?

```javascript
var arr=[10,20,30];

console.log(arr[2]);
```

Answer:

```text
30
```

---

### Q7. What is typeof(Array)?

Example:

```javascript
var arr=[1,2,3];

console.log(typeof(arr));
```

Answer:

```text
object
```

---

### Q8. How do you create an Array?

**Answer**

Three ways:

1.

```javascript
var arr=[1,2,3];
```

2.

```javascript
var arr=new Array();
```

3.

```javascript
var arr=new Array(1,2,3);
```

---

### Q9. How do you find Array length?

**Answer**

Using:

```javascript
length
```

Example:

```javascript
var arr=[1,2,3,4];

console.log(arr.length);
```

Output:

```text
4
```

---

### Q10. What is push()?

**Answer**

push() adds an element at the end.

Example:

```javascript
var arr=[10,20];

arr.push(30);

console.log(arr);
```

Output:

```text
[10,20,30]
```

---

### Q11. What is pop()?

**Answer**

pop() removes the last element.

Example:

```javascript
var arr=[10,20,30];

arr.pop();
```

Output:

```text
[10,20]
```

---

### Q12. What is shift()?

**Answer**

shift() removes first element.

Example:

```javascript
var arr=[10,20,30];

arr.shift();
```

Output:

```text
[20,30]
```

---

### Q13. What is unshift()?

**Answer**

unshift() inserts element at beginning.

Example:

```javascript
var arr=[20,30];

arr.unshift(10);
```

Output:

```text
[10,20,30]
```

---

### Q14. What is slice()?

**Answer**

slice() returns a new array without modifying original array.

Example:

```javascript
var arr=[10,20,30,40];

arr.slice(1,3);
```

Output:

```text
[20,30]
```

---

### Q15. Does slice() modify original array?

**Answer**

No.

---

### Q16. What is splice()?

**Answer**

splice() adds/removes elements and modifies original array.

Example:

```javascript
var arr=[10,20,30];

arr.splice(1,1,100);
```

Output:

```text
[10,100,30]
```

---

### Q17. Difference between slice() and splice()?

| slice()           | splice()                    |
| ----------------- | --------------------------- |
| Returns new array | Changes original            |
| Doesn't modify    | Modifies                    |
| Used for copying  | Used for insertion/deletion |

---

### Q18. What is delete operator?

Example:

```javascript
var arr=[10,20,30];

delete arr[1];
```

Output:

```text
[10, empty, 30]
```

---

### Q19. Does delete reduce array length?

**Answer**

No.

It leaves empty slot.

---

### Q20. How to replace element in Array?

Example:

```javascript
arr[1]=100;
```

---

### Q21. What is for...of loop?

**Answer**

Used to iterate values of array.

Example:

```javascript
var arr=[10,20,30];

for(var x of arr)

{

console.log(x);

}
```

Output:

```text
10

20

30
```

---

### Q22. Can Arrays store Objects?

**Answer**

Yes.

Example:

```javascript
var arr=[

{name:"John"},

{name:"Smith"}

];
```

---

### Q23. Can Arrays store Arrays?

**Answer**

Yes.

Example:

```javascript
var arr=[

[1,2],

[3,4]

];
```

---

### Q24. What is concat()?

**Answer**

concat() joins arrays.

Example:

```javascript
var a=[1,2];

var b=[3,4];

a.concat(b);
```

Output:

```text
[1,2,3,4]
```

---

### Q25. What is join()?

**Answer**

Converts array to string.

Example:

```javascript
var arr=[1,2,3];

arr.join("-");
```

Output:

```text
1-2-3
```

---

### Q26. What is reverse()?

Example:

```javascript
var arr=[1,2,3];

arr.reverse();
```

Output:

```text
[3,2,1]
```

---

### Q27. What is sort()?

Example:

```javascript
var arr=[5,1,4,2];

arr.sort();
```

Output:

```text
[1,2,4,5]
```

---

### Q28. What is indexOf()?

**Answer**

Returns index of element.

Example:

```javascript
var arr=[10,20,30];

arr.indexOf(20);
```

Output:

```text
1
```

---

### Q29. What is includes()?

Example:

```javascript
arr.includes(20)
```

Output:

```text
true
```

---

### Q30. Output?

```javascript
var arr=[];

console.log(arr.length);
```

Answer:

```text
0
```

---

### Q31. Output?

```javascript
var arr=[10];

arr.push(20);

console.log(arr);
```

Answer:

```text
[10,20]
```

---

### Q32. Output?

```javascript
var arr=[10,20];

arr.pop();

console.log(arr);
```

Answer:

```text
[10]
```

---

### Q33. Output?

```javascript
var arr=[10,20];

arr.shift();

console.log(arr);
```

Answer:

```text
[20]
```

---

### Q34. Output?

```javascript
var arr=[20];

arr.unshift(10);

console.log(arr);
```

Answer:

```text
[10,20]
```

---

### Q35. Which method adds element at end?

**Answer**

```javascript
push()
```

---

### Q36. Which method removes element from end?

**Answer**

```javascript
pop()
```

---

### Q37. Which method adds element at beginning?

**Answer**

```javascript
unshift()
```

---

### Q38. Which method removes element from beginning?

**Answer**

```javascript
shift()
```

---

### Q39. What is multidimensional array?

**Answer**

Array inside another array.

Example:

```javascript
var arr=[

[1,2],

[3,4]

];
```

---

### Q40. Explain Arrays in JavaScript.

**Answer**

Arrays are:

* Zero indexed
* Dynamic in size
* Heterogeneous
* Object type
* Store multiple values
* Support many built-in methods

Important methods:

* push()
* pop()
* shift()
* unshift()
* slice()
* splice()
* sort()
* reverse()
* concat()
* join()

---

### Frequently Asked Fresher Interview Question

### Q41. Why Arrays are called Objects in JavaScript?

**Answer**

Because internally JavaScript Arrays are implemented as Objects.

Example:

```javascript
typeof([1,2,3])
```

Output:

```text
object
```

Therefore:

```text
Every Array is an Object

But every Object is not an Array
```

---

```

# Part 6: Objects in JavaScript - Interview Questions and Answers

# Objects in JavaScript - Interview Questions and Answers
``` 
### Q1. What is an Object in JavaScript?

**Answer:**

An Object is a collection of key-value pairs.

Example:

```javascript
var person = {
    name: "John",
    age: 25
};
```

### Q2. Why do we use Objects?

**Answer:**

Objects are used to:

* Store related data together
* Represent real-world entities
* Store properties and methods
* Organize complex data

---

### Q3. How many ways can we create Objects in JavaScript?

**Answer:**

There are 3 ways:

1. Literal Way
2. Constructor Function Way
3. Using new Keyword

---

### Q4. What is Literal Object Creation?

**Answer:**

Creating an object directly using curly braces `{}`.

Example:

```javascript
var details = {
    firstname: "John",
    lastname: "Doe",
    age: 30
};
```

---

### Q5. How do you access object properties?

**Answer**

Two ways:

1. Dot Notation

```javascript
details.firstname
```

2. Bracket Notation

```javascript
details["firstname"]
```

---

### Q6. What is the output?

```javascript
var obj = {
    name:"Sachin"
};

console.log(obj.name);
```

Answer:

```text
Sachin
```

---

### Q7. What is the output?

```javascript
var obj = {
    age:30
};

console.log(obj["age"]);
```

Answer:

```text
30
```

---

### Q8. Can Object store different data types?

**Answer**

Yes.

Example:

```javascript
var student = {

name:"John",

age:22,

isPlaced:true,

marks:[90,95,85]

};
```

---

### Q9. What is typeof Object?

Example:

```javascript
var obj={};

console.log(typeof(obj));
```

Answer:

```text
object
```

---

### Q10. Can Object contain Array?

**Answer**

Yes.

Example:

```javascript
var emp={

name:"John",

skills:["Java","SQL","JS"]

};
```

---

### Q11. Can Object contain another Object?

**Answer**

Yes.

Example:

```javascript
var student={

name:"Ram",

address:{

city:"Hyderabad",

state:"Telangana"

}

};
```

---

### Q12. What is Constructor Function?

**Answer**

Constructor Function is used to create multiple objects with same structure.

Example:

```javascript
function Student(name,age)

{

this.name=name;

this.age=age;

}
```

---

### Q13. What is 'this' keyword?

**Answer**

this refers to the current object.

Example:

```javascript
this.name="John";
```

---

### Q14. Why do we use new keyword?

**Answer**

new creates a new object instance.

Example:

```javascript
var obj=new Student("John",25);
```

---

### Q15. What is output?

```javascript
function Person(name)

{

this.name=name;

}

var p=new Person("Sachin");

console.log(p.name);
```

Answer:

```text
Sachin
```

---

### Q16. What is output?

```javascript
var details={

firstname:"John",

lastname:"Doe"

};

console.log(details.firstname);
```

Answer:

```text
John
```

---

### Q17. What is Function Constructor Way?

Example:

```javascript
var fun=function(msg)

{

console.log(msg);

}

fun("Good Morning");
```

Output:

```text
Good Morning
```

---

### Q18. Can Functions be stored inside Objects?

**Answer**

Yes.

Example:

```javascript
var emp={

name:"John",

display:function()

{

console.log("Hello");

}

};
```

---

### Q19. How do you call Object Method?

Example:

```javascript
emp.display();
```

---

### Q20. Difference between Array and Object?

| Array           | Object          |
| --------------- | --------------- |
| Indexed         | Key-value pairs |
| Uses []         | Uses {}         |
| Access by index | Access by key   |
| Ordered         | Unordered       |

---

### Q21. What is Object.create()?

**Answer**

It creates a new object.

Example:

```javascript
var obj=Object.create({});
```

---

### Q22. Can we add properties dynamically?

**Answer**

Yes.

Example:

```javascript
var person={};

person.name="Virat";

person.age=36;
```

---

### Q23. Can we delete object property?

**Answer**

Yes.

Example:

```javascript
delete person.age;
```

---

### Q24. What is Object.keys()?

**Answer**

Returns all keys of object.

Example:

```javascript
Object.keys(person)
```

Output:

```text
["name","age"]
```

---

### Q25. What is Object.values()?

**Answer**

Returns all values.

Example:

```javascript
Object.values(person)
```

Output:

```text
["Virat",36]
```

---

### Q26. What is Object.entries()?

**Answer**

Returns key-value pairs.

Example:

```javascript
Object.entries(person)
```

Output:

```text
[
["name","Virat"],

["age",36]

]
```

---

### Q27. How do you iterate Objects?

**Answer**

Using for...in loop.

Example:

```javascript
var obj={

name:"John",

age:30

};

for(var x in obj)

{

console.log(x);

console.log(obj[x]);

}
```

---

### Q28. Output?

```javascript
var obj={

name:"KodNest"

};

console.log(typeof(obj));
```

Answer:

```text
object
```

---

### Q29. Output?

```javascript
var obj={};

obj.city="Bangalore";

console.log(obj.city);
```

Answer:

```text
Bangalore
```

---

### Q30. Explain Objects in JavaScript.

**Answer**

Objects are:

* Collection of key-value pairs
* Dynamic in nature
* Store properties and methods
* Created using {}, constructor or new keyword
* typeof object returns "object"
* Fundamental building block of JavaScript

```
```

# Part 7: Operators in JavaScript - Interview Questions and Answers

# Operators in JavaScript - Interview Questions and Answers


## Q1. What are Operators in JavaScript?

**Answer:**

Operators are special symbols used to perform operations on operands (variables and values).

Example:

```javascript
var a = 10;
var b = 20;
console.log(a + b);
```

Output:

```text
30
```

---

## Q2. How many types of Operators are available in JavaScript?

**Answer:**

There are mainly:

1. Arithmetic Operators
2. Comparison Operators
3. Logical Operators
4. Ternary Operator
5. String Operators

---

## Q3. What are Arithmetic Operators?

**Answer:**

Arithmetic operators perform mathematical calculations.

Operators:

```text
+
-
*
/
%
++
--
```

---

## Q4. Explain Addition Operator (+)

Example:

```javascript
var a = 10;
var b = 20;

console.log(a+b);
```

Output:

```text
30
```

---

## Q5. Explain Subtraction Operator (-)

Example:

```javascript
var a = 20;
var b = 10;

console.log(a-b);
```

Output:

```text
10
```

---

## Q6. Explain Multiplication Operator (*)

Example:

```javascript
var a=5;
var b=6;

console.log(a*b);
```

Output:

```text
30
```

---

## Q7. Explain Division Operator (/)

Example:

```javascript
var a=20;
var b=4;

console.log(a/b);
```

Output:

```text
5
```

---

## Q8. Explain Modulus Operator (%)

Example:

```javascript
var a=10;
var b=3;

console.log(a%b);
```

Output:

```text
1
```

---

## Q9. What is Increment Operator (++)

**Answer:**

It increases the value by 1.

Example:

```javascript
var a=10;

a++;

console.log(a);
```

Output:

```text
11
```

---

## Q10. Difference between Post Increment and Pre Increment?

**Answer:**

### Post Increment

```javascript
var a=10;

console.log(a++);
```

Output:

```text
10
```

Then a becomes:

```text
11
```

---

### Pre Increment

```javascript
var a=10;

console.log(++a);
```

Output:

```text
11
```

---

## Q11. What is Decrement Operator (--)

Example:

```javascript
var a=10;

a--;

console.log(a);
```

Output:

```text
9
```

---

## Q12. Difference between Post Decrement and Pre Decrement?

Example:

```javascript
var a=10;

console.log(a--);
```

Output:

```text
10
```

Then:

```text
a = 9
```

---

```javascript
var a=10;

console.log(--a);
```

Output:

```text
9
```

---

## Q13. What are Comparison Operators?

**Answer:**

Comparison operators compare two values and return Boolean value.

```text
==
!=
===
!==
>
<
>=
<=
```

---

## Q14. Difference between == and === ?

**Answer:**

### ==

Checks value only.

Example:

```javascript
10 == "10"
```

Output:

```text
true
```

---

### ===

Checks value and datatype.

Example:

```javascript
10 === "10"
```

Output:

```text
false
```

---

## Q15. What is != operator?

Example:

```javascript
10 != 20
```

Output:

```text
true
```

---

## Q16. What is !== operator?

Example:

```javascript
10 !== "10"
```

Output:

```text
true
```

Because:

- Values are same
- Datatypes are different

---

## Q17. Explain Greater Than (>)

Example:

```javascript
10 > 5
```

Output:

```text
true
```

---

## Q18. Explain Less Than (<)

Example:

```javascript
10 < 5
```

Output:

```text
false
```

---

## Q19. Explain >= Operator

Example:

```javascript
10 >= 10
```

Output:

```text
true
```

---

## Q20. Explain <= Operator

Example:

```javascript
10 <= 5
```

Output:

```text
false
```

---

## Q21. What are Logical Operators?

**Answer**

Logical operators combine multiple conditions.

They are:

```text
&&
||
!
```

---

## Q22. Explain Logical AND (&&)

Example:

```javascript
var a=10;
var b=20;

console.log(a<b && b>a);
```

Output:

```text
true
```

---

## Q23. AND Truth Table

| Condition1 | Condition2 | Result |
|-----------|-----------|--------|
| true | true | true |
| true | false | false |
| false | true | false |
| false | false | false |

---

## Q24. Explain Logical OR (||)

Example:

```javascript
var a=10;
var b=20;

console.log(a>b || b>a);
```

Output:

```text
true
```

---

## Q25. OR Truth Table

| Condition1 | Condition2 | Result |
|-----------|-----------|--------|
| true | true | true |
| true | false | true |
| false | true | true |
| false | false | false |

---

## Q26. Explain Logical NOT (!)

Example:

```javascript
console.log(!(10>5));
```

Output:

```text
false
```

---

## Q27. What is Ternary Operator?

**Answer:**

Ternary Operator is shorthand form of if-else.

Syntax:

```javascript
condition ? statement1 : statement2;
```

---

## Q28. Example of Ternary Operator

```javascript
var age=20;

age>=18 ?

console.log("Eligible")

:

console.log("Not Eligible");
```

Output:

```text
Eligible
```

---

## Q29. What are String Operators?

**Answer**

String Operator is used to concatenate strings.

Example:

```javascript
var s1="Hello";

var s2="World";

console.log(s1+" "+s2);
```

Output:

```text
Hello World
```

---

## Q30. What is the output?

```javascript
console.log("10"+20);
```

Output:

```text
1020
```

Because:

20 becomes string.

---

## Q31. What is the output?

```javascript
console.log(10+20+"30");
```

Output:

```text
3030
```

Explanation:

```text
10+20 = 30

30+"30" = "3030"
```

---

## Q32. What is the output?

```javascript
console.log("10"+20+30);
```

Output:

```text
102030
```

Explanation:

```text
"10"+20 = "1020"

"1020"+30 = "102030"
```

---

## Q33. What is Operator Precedence?

**Answer**

Operator precedence determines:

Which operator is evaluated first.

Example:

```javascript
console.log(10+5*2);
```

Output:

```text
20
```

Because:

```text
5*2 =10

10+10=20
```

---

## Q34. Which operator has higher precedence?

**Answer**

```text
()
++
--
*
/
%
+
-
Comparison
Logical
Ternary
Assignment
```

---

## Q35. Explain Operators in JavaScript.

**Answer**

Operators are symbols used to perform:

- Mathematical operations
- Comparisons
- Logical operations
- String concatenation
- Conditional operations

Major categories:

1. Arithmetic
2. Comparison
3. Logical
4. Ternary
5. String Operators

Operators are one of the most important interview topics in JavaScript.

````
````
# Part 8: Conditional Statements in JavaScript - Interview Questions and Answers


# Conditional Statements in JavaScript - Interview Questions and Answers

---

## Q1. What are Conditional Statements in JavaScript?

**Answer:**

Conditional statements are used to execute different blocks of code based on different conditions.

JavaScript provides:

1. if statement
2. if...else statement
3. if...else if...else statement
4. switch statement
5. Ternary operator

---

## Q2. What is an if statement?

**Answer:**

The if statement executes a block of code only when the condition is true.

Syntax:

```javascript
if(condition)
{
    // code
}
```

---

## Q3. Example of if statement

```javascript
var age = 18;

if(age >= 18)
{
    console.log("Eligible to Vote");
}
```

Output:

```text
Eligible to Vote
```

---

## Q4. What happens if the condition is false in if statement?

**Answer:**

The code inside the if block will not execute.

Example:

```javascript
var age = 15;

if(age >= 18)
{
    console.log("Eligible");
}
```

Output:

```text
No Output
```

---

## Q5. What is if...else statement?

**Answer:**

if...else provides two execution paths.

- if block → when condition is true
- else block → when condition is false

Syntax:

```javascript
if(condition)
{
   // true block
}
else
{
   // false block
}
```

---

## Q6. Example of if...else

```javascript
var age = 16;

if(age>=18)
{
    console.log("Eligible");
}
else
{
    console.log("Not Eligible");
}
```

Output:

```text
Not Eligible
```

---

## Q7. What is else if statement?

**Answer:**

else if is used to check multiple conditions.

Syntax:

```javascript
if(condition1)
{

}
else if(condition2)
{

}
else
{

}
```

---

## Q8. Example of else if

```javascript
var age = 16;

if(age>=18)
{
    console.log("Vote");
}
else if(age>=16)
{
    console.log("Learner License");
}
else
{
    console.log("Not Eligible");
}
```

Output:

```text
Learner License
```

---

## Q9. Can we use multiple else if blocks?

**Answer:**

Yes.

Example:

```javascript
var marks=75;

if(marks>=90)
{
console.log("A");
}
else if(marks>=80)
{
console.log("B");
}
else if(marks>=70)
{
console.log("C");
}
else
{
console.log("Fail");
}
```

Output:

```text
C
```

---

## Q10. Which block executes first?

**Answer:**

Conditions are checked from top to bottom.

The first true condition executes.

Remaining blocks are ignored.

---

## Q11. What is nested if?

**Answer:**

An if statement inside another if statement is called nested if.

Example:

```javascript
var age=20;

var citizen=true;

if(age>=18)
{
    if(citizen)
    {
        console.log("Eligible");
    }
}
```

Output:

```text
Eligible
```

---

## Q12. What is switch statement?

**Answer:**

switch statement is used to select one block from many blocks.

Syntax:

```javascript
switch(expression)
{

case value1:

break;

case value2:

break;

default:

}
```

---

## Q13. Example of switch

```javascript
var day="Monday";

switch(day)
{

case "Monday":

console.log("Today is Monday");

break;

case "Tuesday":

console.log("Today is Tuesday");

break;

default:

console.log("Invalid");

}
```

Output:

```text
Today is Monday
```

---

## Q14. Why do we use break in switch?

**Answer:**

break terminates the switch block.

Without break, execution continues to next cases.

---

## Q15. What is default in switch?

**Answer:**

default executes when none of the cases match.

Example:

```javascript
var n=5;

switch(n)
{

case 1:

console.log("One");

break;

default:

console.log("Invalid");

}
```

Output:

```text
Invalid
```

---

## Q16. What happens if break is omitted?

Example:

```javascript
var n=1;

switch(n)
{

case 1:

console.log("One");

case 2:

console.log("Two");

default:

console.log("Done");

}
```

Output:

```text
One

Two

Done
```

This is called:

```text
Fall Through
```

---

## Q17. Difference between if and switch?

| if | switch |
|-----|--------|
| Used for ranges | Used for fixed values |
| More flexible | Faster for many options |
| Complex conditions | Exact matching |
| Uses boolean expressions | Uses expression |

---

## Q18. Which is better: if or switch?

**Answer:**

Use:

- if → for ranges

Example:

```javascript
marks > 90
```

- switch → for fixed values

Example:

```javascript
Monday

Tuesday

Wednesday
```

---

## Q19. Can switch use strings?

**Answer:**

Yes.

Example:

```javascript
var city="Hyderabad";

switch(city)
{

case "Hyderabad":

console.log("Telangana");

break;

}
```

Output:

```text
Telangana
```

---

## Q20. Can switch use numbers?

**Answer:**

Yes.

Example:

```javascript
var n=2;

switch(n)
{

case 1:

console.log("One");

break;

case 2:

console.log("Two");

break;

}
```

Output:

```text
Two
```

---

## Q21. What is Ternary Operator?

**Answer**

Ternary Operator is shorthand form of if...else.

Syntax:

```javascript
condition ?

statement1

:

statement2;
```

---

## Q22. Example of Ternary Operator

```javascript
var age=20;

age>=18 ?

console.log("Eligible")

:

console.log("Not Eligible");
```

Output:

```text
Eligible
```

---

## Q23. Output?

```javascript
var a=10;

if(a>5)
{
console.log("Hello");
}
```

Output:

```text
Hello
```

---

## Q24. Output?

```javascript
var a=2;

if(a>5)
{
console.log("Hi");
}
else
{
console.log("Bye");
}
```

Output:

```text
Bye
```

---

## Q25. Explain Conditional Statements in JavaScript.

**Answer:**

Conditional statements are decision-making statements.

Types:

1. if
2. if else
3. if else if else
4. switch
5. ternary operator

They help:

- Execute code conditionally
- Validate data
- Make decisions
- Control program flow

Conditional Statements are one of the most frequently asked JavaScript interview topics.

````
````

# Part 9: Looping Statements in JavaScript - Interview Questions and Answers

# Looping Statements in JavaScript - Interview Questions and Answers

---

## Q1. What are Looping Statements in JavaScript?

**Answer:**

Looping statements are used to execute a block of code repeatedly until a condition becomes false.

JavaScript provides:

1. for loop
2. while loop
3. do...while loop
4. for...of loop
5. for...in loop

---

## Q2. Why do we use loops?

**Answer:**

Loops are used to:

- Avoid writing repetitive code
- Iterate arrays
- Iterate objects
- Process collections of data
- Execute statements multiple times

---

## Q3. What is a for loop?

**Answer:**

for loop executes code repeatedly based on:

1. Initialization
2. Condition
3. Increment/Decrement

Syntax:

```javascript
for(initialization; condition; increment)
{

}
```

---

## Q4. Example of for loop

```javascript
for(var i=0;i<5;i++)
{
console.log(i);
}
```

Output:

```text
0
1
2
3
4
```

---

## Q5. Explain parts of for loop.

```javascript
for(var i=0;i<5;i++)
```

- var i=0 → Initialization
- i<5 → Condition
- i++ → Increment

---

## Q6. What is while loop?

**Answer:**

while loop executes code as long as condition is true.

Syntax:

```javascript
while(condition)
{

}
```

---

## Q7. Example of while loop

```javascript
var i=0;

while(i<5)
{
console.log(i);

i++;
}
```

Output:

```text
0
1
2
3
4
```

---

## Q8. What is do...while loop?

**Answer:**

do...while executes the block at least once.

Syntax:

```javascript
do
{

}
while(condition);
```

---

## Q9. Example of do...while

```javascript
var i=0;

do{

console.log(i);

i++;

}

while(i<5);
```

Output:

```text
0
1
2
3
4
```

---

## Q10. Difference between while and do...while?

| while | do...while |
|------|------|
| Condition checked first | Executes first |
| May execute zero times | Executes at least once |
| Entry controlled loop | Exit controlled loop |

---

## Q11. Example proving do...while executes once

```javascript
var i=10;

do{

console.log(i);

}

while(i<5);
```

Output:

```text
10
```

---

## Q12. Example proving while may not execute

```javascript
var i=10;

while(i<5)
{
console.log(i);
}
```

Output:

```text
No Output
```

---

## Q13. What is Infinite Loop?

**Answer**

A loop that never ends is called Infinite Loop.

Example:

```javascript
for(var i=0;i>=0;i++)
{
console.log(i);
}
```

This loop runs forever.

---

## Q14. Example of Infinite while loop

```javascript
var i=0;

while(i>=0)
{
console.log(i);

i++;
}
```

This loop never stops.

---

## Q15. How do you stop Infinite Loop?

**Answer**

Using:

```javascript
break;
```

Example:

```javascript
for(var i=0;i<100;i++)
{

if(i==5)

break;

console.log(i);

}
```

Output:

```text
0
1
2
3
4
```

---

## Q16. What is break statement?

**Answer**

break terminates the loop immediately.

Example:

```javascript
for(var i=1;i<=10;i++)
{

if(i==6)

break;

console.log(i);

}
```

Output:

```text
1
2
3
4
5
```

---

## Q17. What is continue statement?

**Answer**

continue skips current iteration.

Example:

```javascript
for(var i=1;i<=5;i++)
{

if(i==3)

continue;

console.log(i);

}
```

Output:

```text
1
2
4
5
```

---

## Q18. What is for...of loop?

**Answer**

for...of is used to iterate:

- Arrays
- Strings
- Iterable Objects

Syntax:

```javascript
for(var x of array)
{

}
```

---

## Q19. Example of for...of

```javascript
var arr=[1,2,3,4,5];

for(var x of arr)
{

console.log(x);

}
```

Output:

```text
1
2
3
4
5
```

---

## Q20. Can for...of iterate Objects?

**Answer**

No.

Objects are not iterable by default.

---

## Q21. What is for...in loop?

**Answer**

for...in is used to iterate Object properties.

Syntax:

```javascript
for(var x in object)
{

}
```

---

## Q22. Example of for...in

```javascript
var obj={

name:"John",

age:30,

city:"Delhi"

};

for(var x in obj)

{

console.log(x);

}
```

Output:

```text
name

age

city
```

---

## Q23. How to get values using for...in?

Example:

```javascript
var obj={

name:"John",

age:30

};

for(var x in obj)

{

console.log(obj[x]);

}
```

Output:

```text
John

30
```

---

## Q24. Difference between for...of and for...in?

| for...of | for...in |
|------|------|
| Iterates values | Iterates keys |
| Used for Arrays | Used for Objects |
| Iterable objects | Non-iterable objects |
| Returns element | Returns property |

---

## Q25. Output?

```javascript
var arr=["A","B","C"];

for(var x of arr)

{

console.log(x);

}
```

Output:

```text
A

B

C
```

---

## Q26. Output?

```javascript
var obj={

a:10,

b:20

};

for(var x in obj)

{

console.log(x);

}
```

Output:

```text
a

b
```

---

## Q27. Output?

```javascript
for(var i=1;i<=3;i++)

{

console.log(i);

}
```

Output:

```text
1

2

3
```

---

## Q28. Output?

```javascript
var i=1;

while(i<=3)

{

console.log(i);

i++;

}
```

Output:

```text
1

2

3
```

---

## Q29. Output?

```javascript
var i=1;

do{

console.log(i);

i++;

}

while(i<=3);
```

Output:

```text
1

2

3
```

---

## Q30. Which loop is best in JavaScript?

**Answer**

Depends on requirement:

- for → Fixed iterations
- while → Unknown iterations
- do...while → Execute at least once
- for...of → Arrays
- for...in → Objects

---

## Q31. Explain Looping Statements in JavaScript.

**Answer**

Looping statements execute code repeatedly.

Types:

1. for
2. while
3. do...while
4. for...of
5. for...in

Important concepts:

- break
- continue
- Infinite loops
- Array iteration
- Object iteration

Looping statements are one of the most important JavaScript interview topics.

````
````

# Part 10: Events in JavaScript - Interview Questions and Answers

# Events in JavaScript - Interview Questions and Answers

## Q1. What are Events in JavaScript?

**Answer:**

Events are actions or occurrences that happen in the browser.

Examples:

- Clicking a button
- Moving mouse over an element
- Pressing a key
- Submitting a form
- Loading a webpage

JavaScript can respond to these events using event handlers.

---

## Q2. Why are Events used in JavaScript?

**Answer:**

Events are used to:

- Make webpages interactive
- Respond to user actions
- Validate forms
- Display messages
- Create dynamic user interfaces

---

## Q3. What is an Event Handler?

**Answer:**

An Event Handler is a function that executes when an event occurs.

Example:

```html
<button onclick="fun()">Click</button>
```

```javascript
function fun()
{
    alert("Hello");
}
```

---

## Q4. What is onclick event?

**Answer:**

onclick executes when the user clicks an element.

Example:

```html
<button onclick="show()">Click Me</button>
```

```javascript
function show()
{
    alert("Button Clicked");
}
```

---

## Q5. What is onmouseover event?

**Answer:**

onmouseover executes when mouse pointer enters an element.

Example:

```html
<button onmouseover="fun()">Move Mouse</button>
```

```javascript
function fun()
{
    alert("Mouse Over");
}
```

---

## Q6. What is onmouseout event?

**Answer:**

onmouseout executes when mouse leaves an element.

Example:

```html
<button onmouseout="fun()">Mouse Out</button>
```

```javascript
function fun()
{
    alert("Mouse Left");
}
```

---

## Q7. Write a program using onclick event.

```html
<button onclick="msg()">Message</button>

<script>

function msg()
{
alert("Welcome to JavaScript");
}

</script>
```

Output:

```text
Welcome to JavaScript
```

---

## Q8. What is alert() in JavaScript?

**Answer**

alert() displays a popup message box.

Example:

```javascript
alert("Hello");
```

Output:

```text
Popup appears with Hello
```

---

## Q9. What is confirm()?

**Answer**

confirm() displays:

- OK button
- Cancel button

Example:

```javascript
confirm("Are you sure?");
```

Output:

```text
Popup with OK and Cancel
```

---

## Q10. Difference between alert() and confirm()

| alert() | confirm() |
|--------|--------|
| Displays message | Displays message with buttons |
| Only OK button | OK and Cancel |
| No return value | Returns true or false |

---

## Q11. What is prompt()?

**Answer**

prompt() accepts input from user.

Example:

```javascript
var name = prompt("Enter Name");

console.log(name);
```

---

## Q12. What are Mouse Events?

**Answer**

Mouse Events are:

1. onclick
2. ondblclick
3. onmouseover
4. onmouseout
5. onmousedown
6. onmouseup

---

## Q13. What are Keyboard Events?

**Answer**

Keyboard Events are:

1. onkeydown
2. onkeypress
3. onkeyup

---

## Q14. What are Form Events?

**Answer**

Form Events include:

1. onsubmit
2. onchange
3. onfocus
4. onblur
5. onreset

---

## Q15. What is onsubmit event?

**Answer**

onsubmit executes when form is submitted.

Example:

```html
<form onsubmit="return validate()">

<input type="submit">

</form>
```

---

## Q16. What is onchange event?

**Answer**

onchange executes when value changes.

Example:

```html
<select onchange="fun()">

<option>Java</option>

<option>Python</option>

</select>
```

---

## Q17. What is onfocus event?

**Answer**

onfocus occurs when an input receives focus.

Example:

```html
<input type="text" onfocus="fun()">
```

---

## Q18. What is onblur event?

**Answer**

onblur occurs when an element loses focus.

Example:

```html
<input type="text" onblur="fun()">
```

---

## Q19. Explain addEventListener()

**Answer**

addEventListener() attaches an event to an element.

Syntax:

```javascript
element.addEventListener("click",function);
```

Example:

```javascript
button.addEventListener("click",fun);
```

---

## Q20. Difference between onclick and addEventListener()

| onclick | addEventListener |
|--------|--------|
| Only one event | Multiple events |
| Old method | Modern method |
| Overwrites existing | Doesn't overwrite |
| Less flexible | More flexible |

---

## Q21. Example of addEventListener()

```html
<button id="btn">Click</button>

<script>

document.getElementById("btn")

.addEventListener("click",function(){

alert("Clicked");

});

</script>
```

Output:

```text
Clicked
```

---

## Q22. What is Event Object?

**Answer**

Event Object contains information about the event.

Example:

```javascript
function fun(event)
{
console.log(event.type);
}
```

Output:

```text
click
```

---

## Q23. What is preventDefault()?

**Answer**

preventDefault() stops default browser behavior.

Example:

```javascript
event.preventDefault();
```

Used in:

- Form submission
- Hyperlinks

---

## Q24. What is stopPropagation()?

**Answer**

It stops event bubbling.

Example:

```javascript
event.stopPropagation();
```

---

## Q25. What is Event Bubbling?

**Answer**

Event moves:

```text
Child → Parent → Grand Parent
```

Example:

```html
button → div → body
```

Clicking button triggers:

```text
button

div

body
```

---

## Q26. What is Event Capturing?

**Answer**

Event flows:

```text
Body

↓

Div

↓

Button
```

Parent to Child.

---

## Q27. Output?

```javascript
function fun()
{
alert("Hello");
}
```

```html
<button onclick="fun()">Click</button>
```

Output:

```text
Popup:

Hello
```

---

## Q28. Output?

```javascript
function enjoy()
{
confirm("Welcome");
}
```

Output:

```text
Confirmation Popup

OK

Cancel
```

---

## Q29. Which event occurs when mouse enters element?

**Answer**

```text
onmouseover
```

---

## Q30. Which event occurs when mouse leaves element?

**Answer**

```text
onmouseout
```

---

## Q31. Explain Events in JavaScript.

**Answer**

Events are browser actions handled using JavaScript.

Common Events:

- onclick
- onmouseover
- onmouseout
- onsubmit
- onchange
- onkeydown
- onkeyup

Methods:

- alert()
- confirm()
- prompt()
- addEventListener()

Events are one of the most important topics for JavaScript interviews because they are used heavily in DOM Manipulation and Form Validation.

````
````

# Part 11: Functions in JavaScript - Interview Questions and Answers

# Functions in JavaScript - Interview Questions and Answers

---

## Q1. What is a Function in JavaScript?

**Answer:**

A Function is a reusable block of code that performs a specific task.

It can:

- Accept input (Parameters)
- Process data
- Return output

---

## Q2. Why do we use Functions?

**Answer:**

Functions are used to:

1. Reuse code
2. Reduce code duplication
3. Improve readability
4. Improve maintainability
5. Divide large programs into smaller modules

---

## Q3. What is the syntax of a Function?

```javascript
function functionName()
{
    // code
}
```

Example:

```javascript
function display()
{
    console.log("Hello JavaScript");
}

display();
```

Output:

```text
Hello JavaScript
```

---

## Q4. What are the parts of a Function?

**Answer:**

A function has:

1. Function keyword
2. Function name
3. Parameters
4. Function body
5. Return statement (optional)

Example:

```javascript
function add(a,b)
{
    return a+b;
}
```

---

## Q5. How do you call a Function?

Example:

```javascript
function greet()
{
    console.log("Welcome");
}

greet();
```

Output:

```text
Welcome
```

---

## Q6. What is Function Declaration?

**Answer**

A normal function created using function keyword.

Example:

```javascript
function addition()
{
    var a=10;
    var b=20;

    console.log(a+b);
}

addition();
```

Output:

```text
30
```

---

## Q7. What is Function Expression?

**Answer**

When a function is assigned to a variable, it is called Function Expression.

Example:

```javascript
var disp = function()
{
    console.log("Hello");
}

disp();
```

Output:

```text
Hello
```

---

## Q8. Can Function Expression have a name?

**Answer**

Yes.

Example:

```javascript
var disp = function sub()
{
    console.log("Hello");
}
```

---

## Q9. What is Anonymous Function?

**Answer**

A function without a name is called Anonymous Function.

Example:

```javascript
var disp=function(a,b)
{
    console.log(a+b);
}

disp(10,20);
```

Output:

```text
30
```

---

## Q10. Why do we use Anonymous Functions?

**Answer**

Anonymous Functions are used:

- In callbacks
- In Event Handlers
- In Function Expressions
- Inside addEventListener()

---

## Q11. What is Constructor Function?

**Answer**

Constructor Function creates Objects.

Example:

```javascript
function Student(name,age)
{
    this.name=name;

    this.age=age;
}

var s1=new Student("John",25);

console.log(s1);
```

Output:

```text
Student

{

name:"John",

age:25

}
```

---

## Q12. Why do we use new keyword?

**Answer**

new:

- Creates Object
- Binds this
- Returns object automatically

---

## Q13. What is this keyword?

**Answer**

this refers to current object.

Example:

```javascript
function Student(name)
{
this.name=name;
}
```

---

## Q14. What is Arrow Function?

**Answer**

Arrow Function is shorter syntax introduced in ES6.

Syntax:

```javascript
()=>{}
```

Example:

```javascript
var disp=()=>console.log("Arrow Function");

disp();
```

Output:

```text
Arrow Function
```

---

## Q15. Arrow Function with Parameters

Example:

```javascript
var add=(a,b)=>
{

return a+b;

}

console.log(add(10,20));
```

Output:

```text
30
```

---

## Q16. Arrow Function without return

Example:

```javascript
var square=n=>n*n;

console.log(square(5));
```

Output:

```text
25
```

---

## Q17. Difference between Normal Function and Arrow Function?

| Normal Function | Arrow Function |
|-----------------|----------------|
| Uses function keyword | Uses => |
| Has own this | Doesn't have own this |
| Supports arguments | Doesn't have arguments |
| Constructor allowed | Constructor not allowed |

---

## Q18. Can Arrow Function be Constructor?

**Answer**

No.

Example:

```javascript
var fun=()=>{}

new fun();
```

Output:

```text
TypeError
```

---

## Q19. What is Return Statement?

**Answer**

return sends value back from function.

Example:

```javascript
function add(a,b)
{
return a+b;
}

console.log(add(10,20));
```

Output:

```text
30
```

---

## Q20. What happens if function has no return?

Example:

```javascript
function demo()
{

}

console.log(demo());
```

Output:

```text
undefined
```

---

## Q21. What are Parameters?

**Answer**

Parameters are variables inside function definition.

Example:

```javascript
function add(a,b)
{

}
```

a and b are parameters.

---

## Q22. What are Arguments?

**Answer**

Arguments are actual values passed to function.

Example:

```javascript
add(10,20);
```

10 and 20 are arguments.

---

## Q23. What is Default Parameter?

Example:

```javascript
function greet(name="Guest")
{
console.log(name);
}

greet();
```

Output:

```text
Guest
```

---

## Q24. Can Functions return Functions?

**Answer**

Yes.

Example:

```javascript
function outer()
{

return function()
{

console.log("Inner");

}

}

outer()();
```

Output:

```text
Inner
```

---

## Q25. Can Function be assigned to Variable?

**Answer**

Yes.

Example:

```javascript
var show=function()
{

console.log("Hello");

}
```

---

## Q26. Can Function be passed as Argument?

**Answer**

Yes.

Example:

```javascript
function greet(fun)
{

fun();

}

greet(function(){

console.log("Hello");

});
```

Output:

```text
Hello
```

---

## Q27. What is Callback Function?

**Answer**

Function passed as argument to another function.

Example:

```javascript
function display(fun)
{
fun();
}

display(function(){

console.log("Callback");

});
```

---

## Q28. What is Recursive Function?

**Answer**

A function calling itself is Recursive Function.

Example:

```javascript
function fun(n)
{

if(n==0)

return;

console.log(n);

fun(n-1);

}

fun(3);
```

Output:

```text
3

2

1
```

---

## Q29. What is IIFE?

**Answer**

Immediately Invoked Function Expression.

Example:

```javascript
(function(){

console.log("Hello");

})();
```

Output:

```text
Hello
```

---

## Q30. What is Function Hoisting?

**Answer**

Functions can be called before declaration.

Example:

```javascript
hello();

function hello()
{

console.log("Hi");

}
```

Output:

```text
Hi
```

---

## Q31. Output?

```javascript
function add(a,b)
{

return a+b;

}

console.log(add(5,10));
```

Output:

```text
15
```

---

## Q32. Output?

```javascript
var disp=()=>10+20;

console.log(disp());
```

Output:

```text
30
```

---

## Q33. Output?

```javascript
function demo()
{
console.log("Hello");
}

demo();
```

Output:

```text
Hello
```

---

## Q34. Output?

```javascript
var disp=function()
{

return "KodNest";

}

console.log(disp());
```

Output:

```text
KodNest
```

---

## Q35. Can one function call another function?

**Answer**

Yes.

Example:

```javascript
function one()
{
two();
}

function two()
{
console.log("Hello");
}

one();
```

Output:

```text
Hello
```

---

## Q36. What is Higher Order Function?

**Answer**

A function that:

- Takes function as parameter OR
- Returns a function

is called Higher Order Function.

---

## Q37. What is Pure Function?

**Answer**

A function that:

- Gives same output for same input
- Doesn't modify external data

Example:

```javascript
function add(a,b)
{
return a+b;
}
```

---

## Q38. What is Closure?

**Answer**

Closure means:

A function remembers variables from outer scope even after outer function finishes execution.

---

## Q39. Which Function type is introduced in ES6?

**Answer**

Arrow Function.

Syntax:

```javascript
()=>{}
```

---

## Q40. Explain Functions in JavaScript.

**Answer**

Functions are reusable blocks of code.

Types:

1. Function Declaration
2. Function Expression
3. Anonymous Function
4. Constructor Function
5. Arrow Function
6. Callback Function
7. Recursive Function
8. IIFE

Functions are one of the MOST IMPORTANT JavaScript interview topics and are asked in almost every fresher interview.

````
````

# Part 12: Regular Expressions in JavaScript - Interview Questions and Answers


# Regular Expressions in JavaScript - Interview Questions and Answers

---

## Q1. What is a Regular Expression in JavaScript?

**Answer:**

A Regular Expression (RegEx) is a pattern used to search, match, validate, or replace text inside strings.

Example:

```javascript
var regex = /hello/;

var str = "hello world";

console.log(regex.test(str));
```

Output:

```text
true
```

---

## Q2. Why do we use Regular Expressions?

**Answer:**

Regular Expressions are used for:

1. Form Validation
2. Email Validation
3. Phone Number Validation
4. Password Validation
5. Searching text
6. Replacing text
7. Pattern Matching

---

## Q3. How do you create a Regular Expression?

**Answer**

There are two ways:

### Method 1: Literal Notation

```javascript
var regex = /hello/;
```

### Method 2: RegExp Constructor

```javascript
var regex = new RegExp("hello");
```

---

## Q4. What is the test() method?

**Answer**

test() checks whether a pattern exists in a string.

Syntax:

```javascript
regex.test(string)
```

Example:

```javascript
var regex=/hello/;

var str="hello world";

console.log(regex.test(str));
```

Output:

```text
true
```

---

## Q5. What is the output?

```javascript
var regex=/world/;

var str="hello world";

console.log(regex.test(str));
```

Output:

```text
true
```

---

## Q6. What is the output?

```javascript
var regex=/hi/;

var str="hello world";

console.log(regex.test(str));
```

Output:

```text
false
```

---

## Q7. What does dot (.) mean in RegEx?

**Answer**

Dot (.) matches any single character.

Example:

```javascript
var regex=/h.llo/;

console.log(regex.test("hello"));
```

Output:

```text
true
```

Because:

```text
. = e
```

---

## Q8. What is * (asterisk) in Regular Expressions?

**Answer**

* means:

```text
Zero or More occurrences
```

Example:

```javascript
var regex=/h*llo/;

console.log(regex.test("hllo"));
```

Output:

```text
true
```

---

## Q9. What does + mean in RegEx?

**Answer**

+ means:

```text
One or More occurrences
```

Example:

```javascript
var regex=/h+llo/;

console.log(regex.test("hhllo"));
```

Output:

```text
true
```

---

## Q10. What does ? mean in Regular Expressions?

**Answer**

? means:

```text
Zero or One occurrence
```

Example:

```javascript
/colou?r/
```

Matches:

```text
color

colour
```

---

## Q11. What are Character Classes?

**Answer**

Character classes define sets of characters.

Examples:

```text
[abc]

[a-z]

[A-Z]

[0-9]
```

---

## Q12. What does [a-z] mean?

**Answer**

Matches:

```text
a to z
```

Lowercase alphabets.

Example:

```javascript
/[a-z]/
```

---

## Q13. What does [A-Z] mean?

**Answer**

Matches:

```text
A to Z
```

Uppercase letters.

---

## Q14. What does [0-9] mean?

**Answer**

Matches:

```text
Digits from 0 to 9
```

Example:

```javascript
/[0-9]/
```

---

## Q15. What is ^ in Regular Expressions?

**Answer**

^ indicates:

```text
Beginning of string
```

Example:

```javascript
/^hello/
```

Matches:

```text
hello world
```

---

## Q16. What is $ in Regular Expressions?

**Answer**

$ indicates:

```text
End of string
```

Example:

```javascript
/hello$/
```

Matches:

```text
say hello
```

---

## Q17. What does \d represent?

**Answer**

\d means:

```text
Any digit

0-9
```

Example:

```javascript
/\d/
```

Matches:

```text
5

7

9
```

---

## Q18. What does \D represent?

**Answer**

\D means:

```text
Non-digit
```

Example:

```javascript
/\D/
```

Matches:

```text
A

B

#
```

---

## Q19. What does \w represent?

**Answer**

\w means:

```text
Word Character

[a-zA-Z0-9_]
```

---

## Q20. What does \W represent?

**Answer**

\W means:

```text
Special Characters

@

#

$

%
```

---

## Q21. What does \s represent?

**Answer**

\s means:

```text
Whitespace Character
```

Matches:

```text
Space

Tab

New Line
```

---

## Q22. What does \S represent?

**Answer**

\S means:

```text
Non-whitespace Character
```

---

## Q23. What are Quantifiers?

**Answer**

Quantifiers specify repetitions.

Examples:

```text
*

+

?

{n}

{n,m}
```

---

## Q24. Explain {n} Quantifier

Example:

```javascript
/[0-9]{5}/
```

Matches:

```text
Exactly 5 digits
```

Example:

```text
12345
```

---

## Q25. Explain {n,m}

Example:

```javascript
/[a-z]{3,5}/
```

Matches:

```text
3 to 5 lowercase letters
```

---

## Q26. What is the output?

```javascript
var regex=/hello/;

console.log(regex.test("hello"));
```

Output:

```text
true
```

---

## Q27. Output?

```javascript
var regex=/abc/;

console.log(regex.test("xyz"));
```

Output:

```text
false
```

---

## Q28. Explain Email Regular Expression.

Example:

```javascript
/^[a-zA-Z0-9._]+@[a-z]+\.[a-z]{2,3}$/
```

Matches:

```text
abc@gmail.com

john@yahoo.com
```

---

## Q29. Explain Mobile Number Regular Expression.

Example:

```javascript
/^[6-9][0-9]{9}$/
```

Explanation:

```text
^[6-9]

First digit must be 6-9

[0-9]{9}

Remaining 9 digits

$

End of string
```

Valid:

```text
9876543210

8123456789
```

---

## Q30. Explain Regular Expressions in JavaScript.

**Answer**

Regular Expressions are patterns used for:

- Searching text
- Validating inputs
- Replacing strings
- Pattern matching

Important Methods:

1. test()
2. search()
3. replace()
4. match()

Important Symbols:

```text
.

*

+

?

^

$

\d

\w

\s
```

Regular Expressions are one of the **MOST IMPORTANT** JavaScript interview topics, especially for **Form Validation and DOM projects**.

````
````

# Part 13: Pattern Matching in JavaScript - Interview Questions and Answers

# Pattern Matching in JavaScript - Interview Questions and Answers

---

## Q1. What is Pattern Matching in JavaScript?

**Answer:**

Pattern Matching is the process of searching, matching, replacing, or validating text using Regular Expressions.

It is commonly used for:

- Searching text
- Replacing text
- Form validation
- Email validation
- Phone number validation

---

## Q2. What is the syntax of Pattern Matching?

**Answer:**

Syntax:

```javascript
/Pattern/OptionalFlags
```

Example:

```javascript
/hello/i
```

Where:

- hello → Pattern
- i → Identifier/Flag

---

## Q3. What are identifiers (flags) used in Regular Expressions?

**Answer:**

| Flag | Meaning |
|------|---------|
| g | Global Search |
| i | Ignore Case |
| m | Multiline Search |
| s | Dot matches newline |
| u | Unicode support |
| y | Sticky search |

---

## Q4. What is g flag?

**Answer**

g means:

```text
Global Search
```

It searches all occurrences.

Example:

```javascript
var str="Java Java Java";

console.log(str.match(/Java/g));
```

Output:

```text
["Java","Java","Java"]
```

---

## Q5. What is i flag?

**Answer**

i means:

```text
Ignore Case
```

Example:

```javascript
var str="KodNest";

console.log(/kodnest/i.test(str));
```

Output:

```text
true
```

---

## Q6. What is m flag?

**Answer**

m means:

```text
Multiline Search
```

It treats multiple lines separately.

---

## Q7. What is s flag?

**Answer**

s allows:

```text
Dot (.) to match newline characters.
```

---

## Q8. What is u flag?

**Answer**

u stands for:

```text
Unicode Search
```

It supports Unicode characters.

---

## Q9. What is y flag?

**Answer**

y stands for:

```text
Sticky Search
```

It searches only from the current position.

---

## Q10. Which methods are used for Pattern Matching?

**Answer**

There are mainly:

1. search()
2. replace()
3. match()
4. test()

---

## Q11. What is search() method?

**Answer**

search() returns:

```text
Position of first matched character
```

Syntax:

```javascript
string.search(regex)
```

---

## Q12. Example of search()

```javascript
var str="KodNest Technologies";

var n=str.search(/T/i);

console.log(n);
```

Output:

```text
8
```

---

## Q13. What does search() return if no match found?

Example:

```javascript
var str="JavaScript";

console.log(str.search(/z/));
```

Output:

```text
-1
```

---

## Q14. What is replace() method?

**Answer**

replace() replaces matched text with new text.

Syntax:

```javascript
string.replace(regex,newValue)
```

---

## Q15. Example of replace()

```javascript
var str="KodNest";

var res=str.replace(/K/,"M");

console.log(res);
```

Output:

```text
ModNest
```

---

## Q16. Example from your notes

```javascript
var str="KodNest Technologies";

var newStr=str.replace(/T/i,"X");

console.log(newStr);
```

Output:

```text
KodNest Xechnologies
```

---

## Q17. Does replace() change original string?

**Answer**

No.

Strings are immutable.

Example:

```javascript
var str="Java";

var s2=str.replace("J","K");

console.log(str);
```

Output:

```text
Java
```

---

## Q18. What is match() method?

**Answer**

match() returns:

```text
Matched character(s)
```

Syntax:

```javascript
string.match(regex)
```

---

## Q19. Example of match()

```javascript
var str="KodNest";

console.log(str.match(/N/));
```

Output:

```text
["N"]
```

---

## Q20. Example using global match

```javascript
var str="Java Java Java";

console.log(str.match(/Java/g));
```

Output:

```text
["Java","Java","Java"]
```

---

## Q21. What is test() method?

**Answer**

test() returns:

```text
true or false
```

Example:

```javascript
var regex=/hello/;

console.log(regex.test("hello world"));
```

Output:

```text
true
```

---

## Q22. Difference between search() and match()

| search() | match() |
|---------|---------|
| Returns position | Returns matched text |
| Returns integer | Returns array |
| Returns -1 if not found | Returns null if not found |

---

## Q23. Difference between match() and test()

| match() | test() |
|--------|-------|
| Returns array | Returns boolean |
| Gives matched value | Only checks existence |

---

## Q24. Output?

```javascript
var str="KodNest";

console.log(str.search(/N/));
```

Output:

```text
3
```

---

## Q25. Output?

```javascript
var str="Java";

console.log(str.match(/a/g));
```

Output:

```text
["a","a"]
```

---

## Q26. Output?

```javascript
console.log(/hello/.test("hello world"));
```

Output:

```text
true
```

---

## Q27. Output?

```javascript
console.log(/python/.test("JavaScript"));
```

Output:

```text
false
```

---

## Q28. Which method returns index?

**Answer**

```text
search()
```

---

## Q29. Which method returns matched values?

**Answer**

```text
match()
```

---

## Q30. Explain Pattern Matching in JavaScript.

**Answer**

Pattern Matching is performed using:

- Regular Expressions
- search()
- replace()
- match()
- test()

Important Flags:

```text
g

i

m

s

u

y
```

Applications:

- Form Validation
- Email Validation
- Mobile Number Validation
- Searching Text
- Replacing Text

Pattern Matching is one of the **most frequently asked JavaScript interview topics**, especially in **DOM, Form Validation, and Regular Expressions**.

````
````

# Part 14: Form Validation in JavaScript - Interview Questions and Answers

# Form Validation in JavaScript - Interview Questions and Answers

---

## Q1. What is Form Validation in JavaScript?

**Answer:**

Form Validation is the process of checking whether the user-entered data is correct before submitting the form to the server.

It helps to:

- Prevent invalid data
- Improve user experience
- Reduce server load
- Provide instant feedback

---

## Q2. Why is Form Validation required?

**Answer:**

Form Validation is required to:

1. Check mandatory fields.
2. Verify correct data format.
3. Prevent invalid inputs.
4. Improve data accuracy.
5. Reduce server-side validation errors.

---

## Q3. What are the types of Form Validation?

**Answer:**

There are two types:

1. Client-Side Validation
   - Performed using JavaScript.
   - Executed in the browser.

2. Server-Side Validation
   - Performed on the server.
   - More secure.

---

## Q4. What is Client-Side Validation?

**Answer:**

Validation performed in the browser using JavaScript before sending data to the server is called Client-Side Validation.

Example:

```javascript
if(name==""){
alert("Name Required");
}
```

---

## Q5. What is Server-Side Validation?

**Answer:**

Validation performed on the server after form submission is called Server-Side Validation.

Languages used:

- Java
- Python
- PHP
- Node.js

---

## Q6. Which event is mostly used for Form Validation?

**Answer**

```html
onsubmit
```

Example:

```html
<form onsubmit="return validate()">
```

---

## Q7. Why do we use return false in validation?

**Answer**

`return false` prevents form submission.

Example:

```javascript
if(name==""){
return false;
}
```

The form will not be submitted.

---

## Q8. How do you access form data in JavaScript?

**Answer**

Using:

```javascript
document.getElementById()
```

Example:

```javascript
var name=document.getElementById("fname").value;
```

---

## Q9. What does .value property return?

**Answer**

It returns:

```text
User entered data
```

Example:

```javascript
<input type="text" id="fname">

var x=document.getElementById("fname").value;
```

---

## Q10. Write a simple First Name Validation.

**Answer**

```javascript
function validate(){

var res=document.getElementById("fname").value;

if(res==""){
alert("First Name Required");
return false;
}

}
```

---

## Q11. How do you check empty input?

**Answer**

```javascript
if(res=="")
```

or

```javascript
if(res.length==0)
```

---

## Q12. How to check minimum length?

**Answer**

```javascript
if(res.length<3)
```

Example:

```javascript
if(name.length<3){

alert("Minimum 3 characters");

}
```

---

## Q13. How to check maximum length?

**Answer**

```javascript
if(name.length>8)
```

Example:

```javascript
alert("Maximum 8 characters");
```

---

## Q14. How to display error messages inside HTML?

**Answer**

Using:

```javascript
innerHTML
```

Example:

```javascript
document.getElementById("msg").innerHTML=
"Invalid Name";
```

---

## Q15. What is innerHTML?

**Answer**

innerHTML is used to:

```text
Insert or modify HTML content dynamically.
```

Example:

```javascript
element.innerHTML="Hello";
```

---

## Q16. How to validate Phone Number?

**Answer**

Example:

```javascript
if(phone.length!=10){

alert("Invalid Phone");

}
```

---

## Q17. Which function checks numeric values?

**Answer**

```javascript
isNaN()
```

NaN means:

```text
Not a Number
```

---

## Q18. Example of isNaN()

```javascript
var x="abc";

console.log(isNaN(x));
```

Output:

```text
true
```

---

## Q19. Example:

```javascript
var x="9876543210";

console.log(isNaN(x));
```

Output:

```text
false
```

Because it is numeric.

---

## Q20. How to validate numeric phone number?

**Answer**

```javascript
if(isNaN(phone)){

alert("Phone must be numeric");

}
```

---

## Q21. Which Regular Expression is used for Indian Phone Number Validation?

**Answer**

```javascript
/^[6-9]{1}[0-9]{9}$/
```

---

## Q22. Explain:

```javascript
/^[6-9]{1}[0-9]{9}$/
```

**Answer**

| Part | Meaning |
|------|---------|
| ^ | Start |
| [6-9]{1} | First digit must be 6-9 |
| [0-9]{9} | Remaining 9 digits |
| $ | End |

Total digits:

```text
10 digits
```

---

## Q23. Example of Phone Regex Validation

```javascript
var t=/^[6-9]{1}[0-9]{9}$/.test(phone);
```

Returns:

```text
true
```

or

```text
false
```

---

## Q24. What does test() return?

**Answer**

```text
Boolean value
```

Either:

```text
true

or

false
```

---

## Q25. How to change border color if validation fails?

**Answer**

```javascript
document.getElementById("phone")
.style.border="2px solid red";
```

---

## Q26. Example:

```javascript
<input id="phone">

document.getElementById("phone")
.style.border="2px solid red";
```

Output:

```text
Red border appears around textbox.
```

---

## Q27. What happens if validate() returns false?

**Answer**

The form submission stops.

Example:

```html
<form onsubmit="return validate()">
```

If:

```javascript
return false;
```

then

```text
Form will NOT submit.
```

---

## Q28. What happens if validate() returns true?

**Answer**

```text
Form gets submitted successfully.
```

---

## Q29. Is Client-Side Validation enough?

**Answer**

No.

Because:

- Users can disable JavaScript.
- Validation can be bypassed.

Therefore:

```text
Always use Server-Side Validation also.
```

---

## Q30. What are the advantages of Form Validation?

**Answer**

Advantages:

1. Improves user experience.
2. Prevents invalid input.
3. Saves server resources.
4. Gives immediate feedback.
5. Improves data quality.
6. Reduces errors.

---

## Q31. What are the disadvantages of Client-Side Validation?

**Answer**

1. Can be bypassed.
2. JavaScript may be disabled.
3. Not secure alone.
4. Requires Server-Side validation.

---

## Q32. Explain Form Validation in one sentence.

**Answer**

Form Validation is the process of checking whether user-entered data is valid before submitting it to the server using JavaScript or server-side programming languages.

---

## Q33. Which topics are commonly asked from Form Validation in Interviews?

**Answer**

Most Important Questions:

- onsubmit event
- return false
- isNaN()
- .value
- innerHTML
- test()
- Phone Regex
- Client vs Server Validation
- Form Validation using Regular Expressions

These are **very frequently asked JavaScript interview questions for Freshers**.

````
````

# Part 15: DOM (Document Object Model) in JavaScript - Interview Questions and Answers

# DOM (Document Object Model) in JavaScript - Interview Questions and Answers

---

## Q1. What is DOM in JavaScript?

**Answer:**

DOM stands for **Document Object Model**.

It is a programming interface that represents an HTML document as a **tree structure of objects**, allowing JavaScript to access and modify:

- HTML elements
- Attributes
- CSS styles
- Content

---

## Q2. What is the full form of DOM?

**Answer:**

DOM stands for:

```text
Document Object Model
```

---

## Q3. Why is DOM used?

**Answer:**

DOM is used to:

1. Change HTML content dynamically.
2. Change CSS styles dynamically.
3. Add new HTML elements.
4. Remove existing elements.
5. Handle user events.
6. Create interactive web pages.

---

## Q4. Explain DOM in simple words.

**Answer:**

DOM converts an HTML document into a tree of objects.

Example:

```html
<html>
<body>
    <h1>Hello</h1>
    <p>Welcome</p>
</body>
</html>
```

DOM Tree:

```text
Document
 |
 html
 |
 body
 |----h1
 |      |
 |    Hello

 |----p
        |
      Welcome
```

---

## Q5. Which object is the root object of DOM?

**Answer:**

```javascript
document
```

It represents the complete HTML page.

---

## Q6. What is document in JavaScript?

**Answer:**

The `document` object represents the HTML document loaded in the browser.

Example:

```javascript
document.title
```

Returns:

```text
Title of webpage
```

---

## Q7. How do you access an HTML element using ID?

**Answer**

Using:

```javascript
document.getElementById()
```

Example:

```javascript
document.getElementById("demo");
```

---

## Q8. Example of getElementById()

```html
<p id="msg">Hello</p>
```

```javascript
document.getElementById("msg").innerHTML="Welcome";
```

Output:

```text
Welcome
```

---

## Q9. What is innerHTML?

**Answer**

innerHTML is used to:

```text
Get or set HTML content of an element.
```

Example:

```javascript
element.innerHTML="Hello";
```

---

## Q10. Example:

```html
<h1 id="head"></h1>
```

```javascript
document.getElementById("head")
.innerHTML="JavaScript";
```

Output:

```text
JavaScript
```

---

## Q11. What is innerText?

**Answer**

innerText returns:

```text
Visible text only.
```

Example:

```javascript
element.innerText
```

---

## Q12. Difference between innerHTML and innerText?

| innerHTML | innerText |
|-----------|-----------|
| Returns HTML tags | Returns text only |
| Supports HTML | Does not support HTML |

Example:

```javascript
element.innerHTML="<b>Hello</b>"
```

Displays:

```text
Hello (Bold)
```

---

## Q13. What is document.write()?

**Answer**

document.write() writes data directly to the HTML page.

Example:

```javascript
document.write("Hello");
```

Output:

```text
Hello
```

---

## Q14. Why is document.write() not recommended?

**Answer**

Because:

1. It can overwrite the page.
2. Difficult to maintain.
3. DOM methods are better.

---

## Q15. How to change CSS using DOM?

**Answer**

Using:

```javascript
element.style.property
```

Example:

```javascript
document.getElementById("msg")
.style.color="red";
```

---

## Q16. Example:

```javascript
document.getElementById("msg")
.style.backgroundColor="yellow";
```

Changes:

```text
Background color to yellow.
```

---

## Q17. How to change font size using DOM?

**Answer**

```javascript
document.getElementById("msg")
.style.fontSize="30px";
```

---

## Q18. How to change image source dynamically?

**Answer**

Using:

```javascript
element.src
```

Example:

```javascript
document.getElementById("img")
.src="flower.jpg";
```

---

## Q19. How to change hyperlink dynamically?

**Answer**

Using:

```javascript
element.href
```

Example:

```javascript
document.getElementById("link")
.href="https://google.com";
```

---

## Q20. What is getElementsByTagName()?

**Answer**

It returns:

```text
All elements with the specified tag name.
```

Example:

```javascript
document.getElementsByTagName("p");
```

Returns:

```text
Collection of all paragraphs.
```

---

## Q21. What is getElementsByClassName()?

**Answer**

It selects all elements having the same class.

Example:

```javascript
document.getElementsByClassName("demo");
```

---

## Q22. What is querySelector()?

**Answer**

It returns:

```text
First matching element.
```

Example:

```javascript
document.querySelector("#id");
```

---

## Q23. What is querySelectorAll()?

**Answer**

It returns:

```text
All matching elements.
```

Example:

```javascript
document.querySelectorAll(".demo");
```

---

## Q24. Difference between querySelector() and querySelectorAll()

| querySelector | querySelectorAll |
|---------------|------------------|
| Returns first element | Returns all elements |
| Single object | NodeList |

---

## Q25. How to create a new element?

**Answer**

Using:

```javascript
document.createElement()
```

Example:

```javascript
var p=document.createElement("p");
```

---

## Q26. Example:

```javascript
var h=document.createElement("h1");

h.innerHTML="Welcome";
```

Creates:

```html
<h1>Welcome</h1>
```

---

## Q27. How to add element to webpage?

**Answer**

Using:

```javascript
appendChild()
```

Example:

```javascript
document.body.appendChild(h);
```

---

## Q28. How to remove an element?

**Answer**

Using:

```javascript
remove()
```

Example:

```javascript
element.remove();
```

---

## Q29. How to remove child element?

**Answer**

Using:

```javascript
removeChild()
```

Example:

```javascript
parent.removeChild(child);
```

---

## Q30. What is setAttribute()?

**Answer**

Used to set an attribute.

Example:

```javascript
element.setAttribute("class","demo");
```

---

## Q31. What is getAttribute()?

**Answer**

Used to get attribute value.

Example:

```javascript
element.getAttribute("href");
```

---

## Q32. What is DOM Tree?

**Answer**

DOM represents HTML as:

```text
Tree Structure
```

Example:

```text
Document
 |
 html
 |
 body
 |
 h1
 |
 p
```

Each node is called:

```text
DOM Node
```

---

## Q33. What are Leaf Nodes?

**Answer**

The last nodes of the DOM tree are called:

```text
Leaf Nodes
```

Example:

```html
<p>Hello</p>
```

Here:

```text
Hello
```

is a leaf node.

---

## Q34. Which is the most commonly used DOM method?

**Answer**

```javascript
document.getElementById()
```

It is the most frequently used DOM method in interviews.

---

## Q35. Explain DOM in one sentence.

**Answer**

DOM is a tree representation of an HTML document that allows JavaScript to dynamically access, modify, add, and delete HTML elements, attributes, and styles.

---

## Frequently Asked DOM Interview Questions

1. What is DOM?
2. What is document object?
3. What is getElementById()?
4. Difference between innerHTML and innerText.
5. How to create elements dynamically?
6. Difference between querySelector and querySelectorAll.
7. What is appendChild()?
8. What is DOM Tree?
9. What are leaf nodes?
10. How to change CSS using DOM?

These are among the **most frequently asked DOM interview questions for JavaScript Freshers**.

````
````

# Part 16: Animations in JavaScript - Interview Questions and Answers

# Animations in JavaScript - Interview Questions and Answers

---

## Q1. What is Animation in JavaScript?

**Answer:**

Animation in JavaScript is the process of changing the properties of an HTML element continuously over time to create motion or visual effects.

Examples:

- Moving an object
- Rotating images
- Sliding menus
- Loading spinners
- Bouncing balls

---

## Q2. What are the ways to create animations in JavaScript?

**Answer:**

There are three main ways:

1. CSS Animations
2. JavaScript Libraries (GSAP, Anime.js)
3. requestAnimationFrame()
4. setInterval()

---

## Q3. What is CSS Animation?

**Answer:**

CSS Animation uses:

```css
@keyframes
```

to create animations without writing JavaScript.

Example:

```css
@keyframes move {
from{
left:0px;
}
to{
left:100px;
}
}
```

---

## Q4. What is requestAnimationFrame()?

**Answer:**

`requestAnimationFrame()` is a browser API used to create smooth animations.

Syntax:

```javascript
requestAnimationFrame(functionName)
```

It synchronizes animations with the browser refresh rate.

---

## Q5. Why is requestAnimationFrame() preferred over setInterval()?

**Answer:**

Because:

1. Smooth animations
2. Better performance
3. Saves CPU usage
4. Synchronizes with browser refresh rate
5. Stops automatically in inactive tabs

---

## Q6. What is setInterval()?

**Answer:**

setInterval() repeatedly executes a function after a fixed time interval.

Syntax:

```javascript
setInterval(function,time)
```

Example:

```javascript
setInterval(move,1000);
```

Runs:

```text
move() every 1 second
```

---

## Q7. What is clearInterval()?

**Answer**

clearInterval() stops the interval.

Example:

```javascript
var id=setInterval(fun,1000);

clearInterval(id);
```

---

## Q8. Explain the animation example from your notes.

**Answer**

Example:

```javascript
var id=setInterval(Animate,5);
```

This executes:

```javascript
Animate()
```

every:

```text
5 milliseconds
```

---

## Q9. What does this statement do?

```javascript
c.style.top=c1+"px";
```

**Answer**

It moves the element vertically.

Example:

```text
0px
10px
20px
30px
...
```

The element moves downward.

---

## Q10. What does this statement do?

```javascript
c.style.left=c1+"px";
```

**Answer**

It moves the element horizontally.

Example:

```text
0px
20px
50px
100px
```

The element moves to the right.

---

## Q11. Explain this code:

```javascript
if(c1==300)
{
clearInterval(id);
}
```

**Answer**

When:

```text
Position reaches 300px
```

the animation stops.

---

## Q12. What is style property in JavaScript?

**Answer**

style property is used to change CSS dynamically.

Example:

```javascript
element.style.color="red";
```

or

```javascript
element.style.left="100px";
```

---

## Q13. Explain this:

```javascript
element.style.transform=
"translateX(100px)";
```

**Answer**

It moves the element:

```text
100 pixels horizontally.
```

---

## Q14. What is translateX()?

**Answer**

translateX() moves an element:

```text
Horizontally (X-axis)
```

Example:

```javascript
transform:translateX(100px);
```

---

## Q15. What is translateY()?

**Answer**

translateY() moves an element:

```text
Vertically (Y-axis)
```

Example:

```javascript
transform:translateY(50px);
```

---

## Q16. What is @keyframes?

**Answer**

@keyframes defines:

```text
Animation stages
```

Example:

```css
@keyframes slide{

from{
left:0px;
}

to{
left:200px;
}

}
```

---

## Q17. What is animation-duration?

**Answer**

Defines:

```text
How long animation runs.
```

Example:

```css
animation-duration:2s;
```

Animation lasts:

```text
2 seconds
```

---

## Q18. What is animation-iteration-count?

**Answer**

Specifies:

```text
How many times animation repeats.
```

Example:

```css
animation-iteration-count:infinite;
```

Animation runs forever.

---

## Q19. What is infinite animation?

**Answer**

Animation that repeats endlessly.

Example:

```css
animation:slide 3s infinite;
```

---

## Q20. Explain animation in one sentence.

**Answer**

Animation in JavaScript is the process of continuously changing the position, size, color, or style of an HTML element over time to create visual movement and interactive effects.

---

## Frequently Asked Animation Interview Questions

1. What is Animation in JavaScript?
2. Difference between CSS Animation and JS Animation.
3. What is requestAnimationFrame()?
4. Difference between setInterval() and requestAnimationFrame().
5. What is clearInterval()?
6. What is @keyframes?
7. What is animation-duration?
8. What is animation-iteration-count?
9. What is transform?
10. What is translateX()?

These are commonly asked animation questions for JavaScript Freshers.

````
````

# Part 17: BOM (Browser Object Model) in JavaScript - Interview Questions and Answers

# BOM (Browser Object Model) in JavaScript - Interview Questions and Answers

---

## Q1. What is BOM in JavaScript?

**Answer:**

BOM stands for:

```text
Browser Object Model
```

It provides JavaScript objects that allow interaction with the browser window and browser features.

Examples:

- Browser window
- Screen size
- Browser history
- Browser information
- Location URL

---

## Q2. What is the full form of BOM?

**Answer:**

```text
BOM = Browser Object Model
```

---

## Q3. Why is BOM used?

**Answer:**

BOM is used to:

1. Access browser information.
2. Get screen dimensions.
3. Open new browser windows.
4. Navigate browser history.
5. Redirect to another page.
6. Get browser details.

---

## Q4. Which is the root object of BOM?

**Answer:**

The root object is:

```javascript
window
```

All BOM objects are children of:

```text
window object
```

---

## Q5. What is the window object?

**Answer:**

The `window` object represents:

```text
Browser Window
```

It is the global object in JavaScript.

Example:

```javascript
window.alert("Hello");
```

or simply

```javascript
alert("Hello");
```

---

## Q6. What are the major BOM Objects?

**Answer:**

The important BOM objects are:

1. window
2. navigator
3. screen
4. location
5. history

---

## Q7. What is navigator object?

**Answer:**

The navigator object provides:

```text
Browser Information
```

Example:

```javascript
navigator.appName
navigator.userAgent
navigator.platform
```

---

## Q8. What is navigator.userAgent?

**Answer**

It returns:

```text
Browser name and version details.
```

Example:

```javascript
console.log(navigator.userAgent);
```

Output:

```text
Mozilla/5.0 Chrome...
```

---

## Q9. What is navigator.platform?

**Answer**

Returns:

```text
Operating System Platform
```

Example:

```javascript
console.log(navigator.platform);
```

Output:

```text
Win32
```

---

## Q10. What is screen object?

**Answer**

screen object gives:

```text
Screen Information
```

Such as:

- Width
- Height
- Available width
- Available height

---

## Q11. How to get screen width?

**Answer**

```javascript
screen.width
```

Example:

```javascript
console.log(screen.width);
```

Output:

```text
1920
```

(depends on device)

---

## Q12. How to get screen height?

**Answer**

```javascript
screen.height
```

Example:

```javascript
console.log(screen.height);
```

Output:

```text
1080
```

---

## Q13. Example from your notes:

```javascript
document.getElementById("Wid")
.innerHTML=screen.width;
```

What does it do?

**Answer**

Displays:

```text
Browser screen width
```

inside the HTML element.

---

## Q14. What is location object?

**Answer**

location object contains:

```text
Current URL Information
```

Example:

```javascript
location.href
```

---

## Q15. What does location.href return?

**Answer**

Returns:

```text
Complete URL of current webpage
```

Example:

```javascript
console.log(location.href);
```

Output:

```text
https://example.com/index.html
```

---

## Q16. How to redirect a webpage using BOM?

**Answer**

Using:

```javascript
location.href="https://google.com";
```

This redirects:

```text
Current page → Google
```

---

## Q17. What is history object?

**Answer**

history object is used to:

```text
Navigate browser history
```

Methods:

- history.back()
- history.forward()
- history.go()

---

## Q18. What does history.back() do?

**Answer**

Moves browser:

```text
Current Page → Previous Page
```

Example:

```javascript
history.back();
```

Equivalent to:

```text
Browser Back Button
```

---

## Q19. What does history.forward() do?

**Answer**

Moves browser:

```text
Previous Page → Next Page
```

Example:

```javascript
history.forward();
```

---

## Q20. What does history.go() do?

**Answer**

Moves browser to a specific history position.

Example:

```javascript
history.go(-1);
```

Means:

```text
Go back one page
```

Example:

```javascript
history.go(1);
```

Means:

```text
Go forward one page
```

---

## Q21. What is window.open()?

**Answer**

Used to open:

```text
New Browser Window
```

Example:

```javascript
window.open("https://google.com");
```

---

## Q22. What is window.close()?

**Answer**

Used to:

```text
Close browser window.
```

Example:

```javascript
window.close();
```

---

## Q23. What is alert() in BOM?

**Answer**

Displays:

```text
Message box with OK button.
```

Example:

```javascript
alert("Welcome");
```

Output:

```text
Welcome
[ OK ]
```

---

## Q24. What is confirm()?

**Answer**

Displays:

```text
OK and Cancel buttons
```

Example:

```javascript
confirm("Are you sure?");
```

Returns:

```text
true → OK

false → Cancel
```

---

## Q25. What is prompt()?

**Answer**

Displays:

```text
Input box to receive data from user.
```

Example:

```javascript
var name=prompt("Enter Name");
```

---

## Q26. What is the difference between DOM and BOM?

| DOM | BOM |
|------|------|
| Document Object Model | Browser Object Model |
| Works with HTML | Works with Browser |
| Manipulates webpage | Manipulates browser |
| Root is document | Root is window |

---

## Q27. Which object is parent of document object?

**Answer**

```javascript
window
```

Relationship:

```text
window
   |
document
```

---

## Q28. Explain BOM in one sentence.

**Answer**

BOM is a collection of browser-related objects such as window, navigator, screen, history, and location that allow JavaScript to communicate with and control the browser environment.

---

## Frequently Asked BOM Interview Questions

1. What is BOM?
2. BOM full form?
3. What is window object?
4. What is navigator object?
5. What is screen object?
6. Difference between DOM and BOM.
7. What is location.href?
8. What is history.back()?
9. What is window.open()?
10. What is confirm()?

These are very commonly asked JavaScript Fresher interview questions.

````
````

# Part 18: Object Oriented Programming (OOP) in JavaScript - Interview Questions and Answers

# Object Oriented Programming (OOP) in JavaScript - Interview Questions and Answers

---

## Q1. What is OOP in JavaScript?

**Answer:**

OOP stands for:

```text
Object Oriented Programming
```

It is a programming approach in which data and functions are grouped together into objects.

---

## Q2. What are the four pillars of OOP?

**Answer:**

1. Encapsulation
2. Abstraction
3. Inheritance
4. Polymorphism

---

## Q3. What is a Class in JavaScript?

**Answer:**

A class is a blueprint used to create objects.

Example:

```javascript
class Student{

}
```

---

## Q4. What is an Object?

**Answer:**

An object is an instance of a class.

Example:

```javascript
class Student{

}

var s1 = new Student();
```

Here:

```text
s1 is an object
```

---

## Q5. Which keyword is used to create an object?

**Answer**

```javascript
new
```

Example:

```javascript
var obj = new Student();
```

---

## Q6. What is Constructor?

**Answer**

Constructor is a special method that is automatically called when an object is created.

Example:

```javascript
class Student{

constructor(){

console.log("Constructor Called");

}

}
```

---

## Q7. What is the syntax of Constructor?

**Answer**

```javascript
constructor(){

}
```

---

## Q8. Can a class have multiple constructors?

**Answer**

No.

JavaScript supports:

```text
Only ONE constructor per class.
```

---

## Q9. Explain constructor with example.

```javascript
class Details{

constructor(fname,lname){

this.fname=fname;
this.lname=lname;

}

}

var d=new Details("Sachin","Tendulkar");
```

Output:

```text
fname = Sachin
lname = Tendulkar
```

---

## Q10. What is this keyword?

**Answer**

`this` refers to:

```text
Current Object
```

Example:

```javascript
this.name="Sachin";
```

---

## Q11. Explain this statement:

```javascript
this.fname=fname;
```

**Answer**

The object's variable:

```javascript
this.fname
```

stores:

```javascript
fname
```

passed from constructor.

---

## Q12. What is a Method in Class?

**Answer**

A function inside a class is called:

```text
Method
```

Example:

```javascript
class Demo{

show(){

return "Hello";

}

}
```

---

## Q13. How to call a class method?

**Answer**

Using object.

Example:

```javascript
obj.show();
```

---

## Q14. Example:

```javascript
class Student{

display(){

return "Welcome";

}

}

var s=new Student();

console.log(s.display());
```

Output:

```text
Welcome
```

---

## Q15. What is Inheritance?

**Answer**

Inheritance is the process by which:

```text
Child class acquires properties and methods of Parent class.
```

---

## Q16. Which keyword is used for inheritance?

**Answer**

```javascript
extends
```

Example:

```javascript
class Child extends Parent{

}
```

---

## Q17. Example of Inheritance

```javascript
class Parent{

show(){

return "Parent";

}

}

class Child extends Parent{

}

var c=new Child();

console.log(c.show());
```

Output:

```text
Parent
```

---

## Q18. What is super keyword?

**Answer**

super is used to:

```text
Call Parent Class Constructor
```

Example:

```javascript
super(name);
```

---

## Q19. Why do we use super()?

**Answer**

Because:

```text
Child constructor must call Parent constructor.
```

---

## Q20. Example:

```javascript
class Parent{

constructor(name){

this.name=name;

}

}

class Child extends Parent{

constructor(name){

super(name);

}

}
```

---

## Q21. What is Method Overriding?

**Answer**

When child class provides its own implementation of parent method.

Example:

```javascript
class Parent{

show(){

return "Parent";

}

}

class Child extends Parent{

show(){

return "Child";

}

}
```

---

## Q22. Output?

```javascript
var c=new Child();

console.log(c.show());
```

Output:

```text
Child
```

---

## Q23. Does JavaScript support Multiple Inheritance?

**Answer**

No.

JavaScript supports:

```text
Single Inheritance
```

through:

```javascript
extends
```

---

## Q24. What is Encapsulation?

**Answer**

Binding:

```text
Data + Methods
```

into a single unit is called:

```text
Encapsulation
```

---

## Q25. What is Abstraction?

**Answer**

Hiding internal implementation details and showing only required functionality.

Example:

```text
ATM Machine
```

User sees:

```text
Withdraw
Deposit
Balance
```

Internal code is hidden.

---

## Q26. What is Polymorphism?

**Answer**

One method behaving differently in different situations.

Example:

```javascript
show()
```

can behave differently in:

```text
Parent

Child
```

---

## Q27. What is Prototype in JavaScript?

**Answer**

Prototype is an object from which other objects inherit properties and methods.

---

## Q28. Why are prototypes used?

**Answer**

Because:

```text
Methods are shared among objects.
```

Memory is saved.

---

## Q29. What is Exception Handling?

**Answer**

Handling runtime errors using:

```text
try

catch

finally
```

---

## Q30. Syntax of Exception Handling

```javascript
try{

}

catch(e){

}

finally{

}
```

---

## Q31. What is try block?

**Answer**

Contains:

```text
Risky Code
```

that may produce exception.

---

## Q32. What is catch block?

**Answer**

It catches:

```text
Runtime Exception
```

Example:

```javascript
catch(e){

alert("Error");

}
```

---

## Q33. What is finally block?

**Answer**

finally block executes:

```text
Always
```

Whether exception occurs or not.

---

## Q34. Example

```javascript
try{

console.log("Hello");

}

catch(e){

console.log("Error");

}

finally{

console.log("Executed");

}
```

Output:

```text
Hello

Executed
```

---

## Q35. Explain OOP in one sentence.

**Answer**

Object Oriented Programming is a programming paradigm that organizes code into classes and objects to achieve reusability, inheritance, abstraction, encapsulation, and polymorphism.

---

## Frequently Asked OOP Interview Questions

1. What is OOP?
2. What is Class?
3. What is Object?
4. What is Constructor?
5. What is this keyword?
6. What is Inheritance?
7. Difference between Class and Object.
8. What is super()?
9. What is Method Overriding?
10. What is Encapsulation?
11. What is Abstraction?
12. What is Polymorphism?
13. What is Prototype?
14. What is Exception Handling?
15. Difference between try, catch and finally.

These are among the **most frequently asked JavaScript OOP interview questions for Freshers**.

````
````

# Part 19: Cookies in JavaScript - Interview Questions and Answers

# Cookies in JavaScript - Interview Questions and Answers

---

## Q1. What are Cookies in JavaScript?

**Answer:**

Cookies are small pieces of data stored in the user's browser as text files.

They are used to store:

- User preferences
- Login information
- Session IDs
- Language settings
- Shopping cart data

---

## Q2. Where are Cookies stored?

**Answer:**

Cookies are stored:

```text
Inside the Browser
```

as

```text
Small Text Files
```

on the user's computer.

---

## Q3. Why are Cookies used?

**Answer:**

Cookies are used to:

1. Remember users.
2. Store login sessions.
3. Save preferences.
4. Track user activity.
5. Store shopping cart details.

---

## Q4. How do you create a Cookie in JavaScript?

**Answer**

Using:

```javascript
document.cookie
```

Example:

```javascript
document.cookie="username=Sachin";
```

This creates:

```text
username = Sachin
```

cookie.

---

## Q5. What is document.cookie?

**Answer**

`document.cookie` is a property used to:

```text
Create
Read
Update
Delete
```

cookies.

---

## Q6. How do you read a Cookie?

**Answer**

Example:

```javascript
console.log(document.cookie);
```

Output:

```text
username=Sachin
```

---

## Q7. Example from your notes

```javascript
document.cookie =
"Nice to meet December batch Students";
```

What does it do?

**Answer**

It creates a cookie storing:

```text
Nice to meet December batch Students
```

inside browser storage.

---

## Q8. How do you check whether Cookie exists?

**Answer**

Example:

```javascript
if(document.cookie.length==0){

alert("No Cookie Found");

}
```

---

## Q9. What does this statement do?

```javascript
document.cookie.length
```

**Answer**

Returns:

```text
Length of cookie string
```

---

## Q10. Example

```javascript
if(document.cookie.length>0)
{
alert("Cookie Exists");
}
```

Output:

```text
Cookie Exists
```

if cookie is available.

---

## Q11. Can JavaScript create multiple Cookies?

**Answer**

Yes.

Example:

```javascript
document.cookie="user=John";

document.cookie="city=Hyderabad";
```

Creates:

```text
user=John

city=Hyderabad
```

---

## Q12. What is Cookie Name and Cookie Value?

**Answer**

Example:

```javascript
document.cookie="username=Sachin";
```

Here:

```text
Cookie Name  = username

Cookie Value = Sachin
```

---

## Q13. What is Session Cookie?

**Answer**

A cookie that exists only:

```text
Until browser is closed.
```

It is called:

```text
Session Cookie
```

---

## Q14. What is Persistent Cookie?

**Answer**

A cookie that remains:

```text
Even after browser is closed.
```

until expiry date.

---

## Q15. How do you set expiry date for Cookies?

**Answer**

Example:

```javascript
document.cookie=
"user=John; expires=Tue, 31 Dec 2026 12:00:00 UTC";
```

---

## Q16. How do you delete a Cookie?

**Answer**

By setting:

```text
Past Expiry Date
```

Example:

```javascript
document.cookie=
"user=John; expires=Thu, 01 Jan 1970 00:00:00 UTC";
```

---

## Q17. What are the limitations of Cookies?

**Answer**

1. Small storage size (~4KB)
2. Security risks
3. Sent with every HTTP request
4. Can be disabled by users
5. Slower than localStorage

---

## Q18. Difference between Cookies and Session?

| Cookies | Session |
|--------|---------|
| Stored in Browser | Stored in Server |
| Small Size | Larger Size |
| Less Secure | More Secure |
| Sent with requests | Stored on server |

---

## Q19. Difference between Cookies and Local Storage?

| Cookies | Local Storage |
|---------|---------------|
| 4KB Storage | 5MB+ Storage |
| Sent to Server | Not Sent |
| Has Expiry | No Expiry |
| Slower | Faster |

---

## Q20. Are Cookies secure?

**Answer**

Cookies are:

```text
Not completely secure.
```

Sensitive information such as:

- Passwords
- Banking details
- OTPs

should NOT be stored in cookies.

---

## Q21. What are HttpOnly Cookies?

**Answer**

HttpOnly Cookies:

```text
Cannot be accessed using JavaScript.
```

They are:

```text
More Secure
```

against XSS attacks.

---

## Q22. What are Secure Cookies?

**Answer**

Secure Cookies:

```text
Sent only over HTTPS connection.
```

This improves:

```text
Security
```

---

## Q23. Explain Cookies in one sentence.

**Answer**

Cookies are small text files stored in the browser that help websites remember user information, preferences, and session data across multiple visits.

---

## Frequently Asked Cookies Interview Questions

1. What are Cookies?
2. Where are Cookies stored?
3. What is document.cookie?
4. How to create Cookies?
5. How to read Cookies?
6. How to delete Cookies?
7. Session Cookie vs Persistent Cookie.
8. Cookies vs Session.
9. Cookies vs Local Storage.
10. Are Cookies secure?

These are the **most frequently asked Cookies interview questions for JavaScript Freshers**.

# 🎉 Entire JavaScript Interview Handbook Completed

You now have interview questions covering all topics from your **21-file JavaScript repository**, including:

* Introduction to JavaScript
* Variables & Keywords
* Data Types
* Type Casting
* Arrays
* Objects
* Operators
* Conditional Statements
* Looping Statements
* Events
* Functions
* Regular Expressions
* Pattern Matching
* Form Validation
* DOM
* Animations
* BOM
* OOP
* Cookies

**Total Coverage:** Approximately **500+ JavaScript Interview Questions and Answers** suitable for **Freshers and Java Full Stack Developer interviews**.
