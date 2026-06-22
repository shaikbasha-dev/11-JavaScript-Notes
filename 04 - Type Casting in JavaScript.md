# Type Casting in JavaScript

## Introduction

Type Casting, also called **Type Conversion**, is the process of converting a value from one data type to another.

JavaScript supports two types of type casting:

1. Implicit Type Casting (Automatic Conversion)
2. Explicit Type Casting (Manual Conversion)

---

## 1. Implicit Type Casting

Implicit Type Casting is automatically performed by JavaScript whenever different data types are used together in an expression.

### Example

```javascript
var result = "The answer is: " + 42;

console.log(result);
console.log(typeof(result));
```

### Output

```text
The answer is: 42
string
```

### Explanation

* Here `"The answer is: "` is a string.
* `42` is a number.
* JavaScript automatically converts `42` into a string.
* Then both values are concatenated.

This process is called **Implicit Type Casting**.

---

## 2. Explicit Type Casting

Explicit Type Casting means converting a value manually using built-in functions.

Some commonly used conversion functions are:

* Number()
* String()
* Boolean()
* parseInt()
* parseFloat()

### Example

```javascript
var str = "123";

var num = Number(str);

console.log(num);
console.log(typeof(num));


var num2 = 456;

var str2 = String(num2);

console.log(str2);
console.log(typeof(str2));
```

### Output

```text
123
number

456
string
```

---

# 1. String to Number Conversion

You can convert a string into a number using:

* Number()
* parseInt()
* parseFloat()

---

### Example 1

```javascript
var s = "Virat";

console.log(s);
console.log(typeof(s));

var s1 = Number(s);

console.log(s1);
console.log(typeof(s1));
```

### Output

```text
Virat
string

NaN
number
```

### Explanation

* `"Virat"` cannot be converted into a valid number.
* Therefore Number() returns **NaN**.
* NaN means **Not a Number**.

---

### Example 2

```javascript
var s2 = "v";

console.log(s2);
console.log(typeof(s2));

var s3 = Number(s2);

console.log(s3);
console.log(typeof(s3));
```

### Output

```text
v
string

NaN
number
```

---

### Example 3

```javascript
var s4 = "";

console.log(s4);
console.log(typeof(s4));

var s5 = Number(s4);

console.log(s5);
console.log(typeof(s5));
```

### Output

```text
""
string

0
number
```

---

### Example 4

```javascript
var s6 = " ";

console.log(s6);
console.log(typeof(s6));

var s7 = Number(s6);

console.log(s7);
console.log(typeof(s7));
```

### Output

```text
" "
string

0
number
```

---

# 2. Number to String Conversion

You can convert a Number to String using:

* String()
* toString()

---

### Example 1

```javascript
var age = 35;

console.log(age);
console.log(typeof(age));

var str = String(age);

console.log(str);
console.log(typeof(str));
```

### Output

```text
35
number

35
string
```

---

### Example 2

```javascript
var marks = 97.5;

console.log(marks);
console.log(typeof(marks));

var str2 = String(marks);

console.log(str2);
console.log(typeof(str2));
```

### Output

```text
97.5
number

97.5
string
```

> Note:
>
> Use **String()** with a capital **S**.
>
> `string()` is incorrect and will throw an error.

---

# 3. String to Boolean Conversion

You can convert a String into Boolean using:

```javascript
Boolean()
```

### Rule

* Non-empty String → true
* Empty String → false

---

### Example 1

```javascript
var sa = "Sachin";

console.log(sa);
console.log(typeof(sa));

var sb = Boolean(sa);

console.log(sb);
console.log(typeof(sb));
```

### Output

```text
Sachin
string

true
boolean
```

---

### Example 2

```javascript
var s1 = "";

console.log(s1);
console.log(typeof(s1));

var s2 = Boolean(s1);

console.log(s2);
console.log(typeof(s2));
```

### Output

```text
""
string

false
boolean
```

---

# 4. Boolean to String Conversion

You can convert Boolean into String using:

* String()
* toString()

---

### Example 1

```javascript
var s1 = true;

console.log(s1);
console.log(typeof(s1));

var s2 = String(s1);

console.log(s2);
console.log(typeof(s2));
```

### Output

```text
true
boolean

true
string
```

---

### Example 2

```javascript
var s1 = false;

console.log(s1);
console.log(typeof(s1));

var s2 = String(s1);

console.log(s2);
console.log(typeof(s2));
```

### Output

```text
false
boolean

false
string
```

---

# 5. Boolean to Number Conversion

You can convert Boolean into Number using:

```javascript
Number()
```

### Rule

| Boolean | Number |
| ------- | ------ |
| true    | 1      |
| false   | 0      |

---

### Example 1

```javascript
var s1 = true;

console.log(s1);
console.log(typeof(s1));

var s2 = Number(s1);

console.log(s2);
console.log(typeof(s2));
```

### Output

```text
true
boolean

1
number
```

---

### Example 2

```javascript
var s1 = false;

console.log(s1);
console.log(typeof(s1));

var s2 = Number(s1);

console.log(s2);
console.log(typeof(s2));
```

### Output

```text
false
boolean

0
number
```

---

# 6. Number to Boolean Conversion

You can convert Number into Boolean using:

```javascript
Boolean()
```

### Rule

| Number              | Boolean |
| ------------------- | ------- |
| 0                   | false   |
| Any Non-Zero Number | true    |

---

### Example 1

```javascript
var s1 = 42;

console.log(s1);
console.log(typeof(s1));

var s2 = Boolean(s1);

console.log(s2);
console.log(typeof(s2));
```

### Output

```text
42
number

true
boolean
```

---

### Example 2

```javascript
var s1 = 0;

console.log(s1);
console.log(typeof(s1));

var s2 = Boolean(s1);

console.log(s2);
console.log(typeof(s2));
```

### Output

```text
0
number

false
boolean
```

---

## Important Notes

1. Type Casting is the conversion of one data type into another.
2. JavaScript supports:

   * Implicit Type Casting
   * Explicit Type Casting
3. `Number()` converts values into numbers.
4. `String()` converts values into strings.
5. `Boolean()` converts values into booleans.
6. `NaN` means **Not a Number**.
7. Empty string `""` converts to `0` using Number().
8. Empty string `""` converts to `false` using Boolean().
9. Any non-zero number converts to `true`.
10. `true → 1` and `false → 0` when converted to Number.

---

## Summary

Type Casting is one of the most important concepts in JavaScript.

JavaScript allows:

* String ↔ Number
* String ↔ Boolean
* Number ↔ String
* Number ↔ Boolean
* Boolean ↔ Number
* Boolean ↔ String

Understanding Type Casting helps developers avoid unexpected results and write reliable JavaScript programs.
