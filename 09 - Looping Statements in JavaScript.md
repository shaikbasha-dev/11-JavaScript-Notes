# Looping Statements in JavaScript

## Introduction

Looping Statements are used to execute a block of code repeatedly until a specified condition becomes false.

Loops help developers:

* Avoid writing repetitive code.
* Iterate through arrays and objects.
* Perform repetitive tasks efficiently.
* Reduce code length and improve readability.

JavaScript provides the following looping statements:

1. for Loop
2. while Loop
3. do...while Loop
4. for...of Loop
5. for...in Loop

---

# 1. for Loop

The **for loop** is used when the number of iterations is known in advance.

## Syntax

```javascript
for(initialization; condition; increment/decrement){

    // code to execute

}
```

---

## Example

```javascript
for(var i = 0; i < 5; i++){

    console.log(i);

}
```

### Output

```text
0
1
2
3
4
```

### Explanation

```javascript
var i = 0
```

Initialization happens once.

```javascript
i < 5
```

Condition is checked before every iteration.

```javascript
i++
```

Increments the value by 1 after every iteration.

---

# Flow of for Loop

```text
Initialization

↓

Condition

↓

True → Execute Loop Body

↓

Increment / Decrement

↓

Condition Again

↓

False → Exit Loop
```

---

# Example: Print Numbers 1 to 10

```javascript
for(var i = 1; i <= 10; i++){

    console.log(i);

}
```

### Output

```text
1
2
3
4
5
6
7
8
9
10
```

---

# 2. while Loop

The while loop executes as long as the condition remains true.

## Syntax

```javascript
while(condition){

    // code

}
```

---

## Example

```javascript
var i = 0;

while(i < 5){

    console.log(i);

    i++;

}
```

### Output

```text
0
1
2
3
4
```

---

### Explanation

The loop continues until:

```javascript
i < 5
```

becomes false.

---

# Example: Print Even Numbers

```javascript
var i = 2;

while(i <= 10){

    console.log(i);

    i += 2;

}
```

### Output

```text
2
4
6
8
10
```

---

# 3. do...while Loop

The do...while loop executes the block **at least once**, even if the condition is false.

---

## Syntax

```javascript
do{

    // code

}
while(condition);
```

---

## Example

```javascript
var i = 0;

do{

    console.log(i);

    i++;

}
while(i < 5);
```

### Output

```text
0
1
2
3
4
```

---

## Example Showing Special Feature

```javascript
var i = 10;

do{

    console.log(i);

}
while(i < 5);
```

### Output

```text
10
```

### Explanation

Even though:

```javascript
10 < 5
```

is false,

the loop executes once because the condition is checked after execution.

---

# Difference Between while and do...while

| while                   | do...while             |
| ----------------------- | ---------------------- |
| Condition checked first | Code executes first    |
| May execute zero times  | Executes at least once |
| Entry Controlled Loop   | Exit Controlled Loop   |

---

# Infinite Loop

An Infinite Loop is a loop that never ends because the condition never becomes false.

---

## Infinite for Loop

```javascript
for(var i = 0; i >= 0; i++){

    console.log(i);

}
```

Here:

```javascript
i >= 0
```

is always true.

Therefore the loop never stops.

---

## Infinite while Loop

```javascript
var i = 0;

while(i >= 0){

    console.log(i);

    i++;

}
```

The condition is always true.

---

## Infinite do...while Loop

```javascript
var i = 0;

do{

    console.log(i);

    i++;

}
while(i >= 0);
```

The loop continues forever.

---

# Breaking Infinite Loop

You can stop a loop using:

```javascript
break;
```

Example:

```javascript
for(var i=0; i<100; i++){

    if(i==5){

        break;

    }

    console.log(i);

}
```

### Output

```text
0
1
2
3
4
```

---

# 4. for...of Loop

The **for...of** loop is used to iterate over:

* Arrays
* Strings
* Iterable Objects

---

## Syntax

```javascript
for(variable of iterable){

    // code

}
```

---

## Example

```javascript
var arr = [1,2,3,4,5];

for(var i of arr){

    console.log(i);

}
```

### Output

```text
1
2
3
4
5
```

---

## Example with String

```javascript
var name = "Basha";

for(var ch of name){

    console.log(ch);

}
```

### Output

```text
B
a
s
h
a
```

---

# 5. for...in Loop

The **for...in** loop is used to iterate over:

* Object Properties
* Non-Iterable Objects

---

## Syntax

```javascript
for(variable in object){

    // code

}
```

---

## Example

```javascript
var obj = {

    name : "John",

    age : 30,

    city : "New York"

};

for(var i in obj){

    console.log(i + " : " + obj[i]);

}
```

---

### Output

```text
name : John

age : 30

city : New York
```

---

# Difference Between for...of and for...in

| for...of                    | for...in                     |
| --------------------------- | ---------------------------- |
| Iterates values             | Iterates keys                |
| Used with Arrays            | Used with Objects            |
| Works with iterable objects | Works with object properties |
| Returns values              | Returns property names       |

---

### Example

```javascript
var arr = [10,20,30];

for(var i in arr){

    console.log(i);

}
```

Output:

```text
0
1
2
```

Because it returns indexes.

---

```javascript
for(var i of arr){

    console.log(i);

}
```

Output:

```text
10
20
30
```

Because it returns values.

---

# Important Points

1. Loops are used for repetitive tasks.
2. for loop is used when the number of iterations is known.
3. while loop checks condition before execution.
4. do...while executes at least once.
5. Infinite loops never terminate.
6. break statement exits the loop.
7. for...of is used for arrays and iterable objects.
8. for...in is used for objects.

---

# Summary

Looping Statements are one of the most important concepts in JavaScript. They allow developers to execute repetitive tasks efficiently, iterate through arrays and objects, and build dynamic applications. Understanding `for`, `while`, `do...while`, `for...of`, and `for...in` loops is essential for mastering JavaScript programming and modern web development.
