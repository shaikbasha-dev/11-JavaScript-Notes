# Conditional Statements in JavaScript

## Introduction

Conditional Statements are used to make decisions in JavaScript.

They allow a program to execute different blocks of code depending on whether a condition is **true** or **false**.

JavaScript provides the following conditional statements:

1. if Statement
2. if...else Statement
3. if...else if...else Statement
4. switch Statement

---

# 1. if Statement

The **if statement** executes a block of code only when the specified condition is true.

## Syntax

```javascript
if(condition){
    // code to execute
}
```

## Example

```javascript
var age = 18;

if(age >= 18){
    console.log("You are eligible to vote.");
}
```

### Output

```text
You are eligible to vote.
```

### Explanation

* The condition is:

```javascript
age >= 18
```

* If the condition is true, the code inside the if block is executed.
* Since age is 18, the message is displayed.

---

# 2. if...else Statement

The **else statement** executes when the if condition is false.

## Syntax

```javascript
if(condition){

    // Executes if condition is true

}
else{

    // Executes if condition is false

}
```

---

## Example

```javascript
var age = 15;

if(age >= 18){

    console.log("Eligible to Vote");

}
else{

    console.log("Not Eligible to Vote");

}
```

### Output

```text
Not Eligible to Vote
```

---

### Explanation

Since:

```javascript
15 >= 18
```

is false,

the else block is executed.

---

# 3. if...else if...else Statement

This statement is used when there are multiple conditions.

## Syntax

```javascript
if(condition1){

    // code

}
else if(condition2){

    // code

}
else{

    // code

}
```

---

## Example

```javascript
var age = 16;

if(age >= 18){

    console.log("You are eligible to vote.");

}
else if(age >= 16){

    console.log("You are eligible for a learner's permit.");

}
else{

    console.log("You are not eligible.");

}
```

### Output

```text
You are eligible for a learner's permit.
```

---

### Explanation

First Condition:

```javascript
age >= 18
```

Result:

```text
false
```

Second Condition:

```javascript
age >= 16
```

Result:

```text
true
```

Hence the second block executes.

---

## Another Example

```javascript
var marks = 82;

if(marks >= 90){

    console.log("Grade A");

}
else if(marks >= 75){

    console.log("Grade B");

}
else if(marks >= 50){

    console.log("Grade C");

}
else{

    console.log("Fail");

}
```

### Output

```text
Grade B
```

---

# 4. switch Statement

The switch statement is used as an alternative to multiple if-else statements.

It checks the value of an expression and executes the matching case.

---

## Syntax

```javascript
switch(expression){

    case value1:

        // code

        break;

    case value2:

        // code

        break;

    default:

        // code

}
```

---

## Example

```javascript
var day = "Monday";

switch(day){

    case "Monday":

        console.log("Today is Monday.");

        break;

    case "Tuesday":

        console.log("Today is Tuesday.");

        break;

    case "Wednesday":

        console.log("Today is Wednesday.");

        break;

    default:

        console.log("It's not Monday, Tuesday, or Wednesday.");

}
```

---

### Output

```text
Today is Monday.
```

---

### Explanation

The switch statement compares:

```javascript
day
```

with:

```javascript
"Monday"
```

Since both are equal,

this block executes:

```javascript
console.log("Today is Monday.");
```

The `break` statement stops further execution.

---

# Importance of break Statement

Consider:

```javascript
var day = "Monday";

switch(day){

    case "Monday":

        console.log("Monday");

    case "Tuesday":

        console.log("Tuesday");

    case "Wednesday":

        console.log("Wednesday");

}
```

### Output

```text
Monday

Tuesday

Wednesday
```

Because there is **no break statement**, all remaining cases execute.

---

## With break

```javascript
var day = "Monday";

switch(day){

    case "Monday":

        console.log("Monday");

        break;

    case "Tuesday":

        console.log("Tuesday");

        break;

}
```

### Output

```text
Monday
```

---

# Nested if Statement

An if statement inside another if statement is called Nested if.

## Example

```javascript
var age = 20;

var citizen = true;

if(age >= 18){

    if(citizen == true){

        console.log("Eligible to Vote");

    }

}
```

### Output

```text
Eligible to Vote
```

---

# Comparison Between if-else and switch

| if-else                       | switch                    |
| ----------------------------- | ------------------------- |
| Used for conditions           | Used for fixed values     |
| Supports relational operators | Uses exact matching       |
| Suitable for ranges           | Suitable for menu options |
| Slower for many conditions    | Faster and cleaner        |

---

# Important Points

1. Conditional statements control the flow of execution.
2. `if` executes only when the condition is true.
3. `else` executes when the condition is false.
4. `else if` is used for multiple conditions.
5. `switch` is an alternative to multiple if-else statements.
6. `break` stops further execution in switch.
7. `default` executes when no case matches.

---

# Summary

Conditional Statements are one of the most important concepts in JavaScript. They help programmers make decisions, validate conditions, execute different code blocks, and control program flow. The `if`, `else`, `else if`, and `switch` statements are widely used in web development for form validation, authentication systems, menu-driven programs, and business logic implementations.
