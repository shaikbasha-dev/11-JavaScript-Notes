# Cookies in JavaScript

## 1. Introduction

Cookies are small pieces of data stored by a web browser on the user's computer. They are used to store information temporarily or permanently so that websites can remember users and their preferences.

Cookies are stored in **text files** and are maintained by the browser.

Examples of information stored in cookies:

* User login information
* Username
* Theme preference (Dark/Light mode)
* Language settings
* Shopping cart items
* Session identifiers

---

## 2. Definition

A **Cookie** is a small text-based data stored in the browser that allows websites to remember information about the user across different pages and visits.

JavaScript provides the following property to work with cookies:

```javascript
document.cookie
```

---

## 3. Why Cookies are Used

Cookies are used to:

1. Store login sessions.
2. Remember user preferences.
3. Store shopping cart information.
4. Save language settings.
5. Track user activity.
6. Personalize websites.
7. Maintain session information.

---

## 4. Creating a Cookie

Syntax:

```javascript
document.cookie = "name=value";
```

Example:

```javascript
document.cookie = "username=Sachin";
```

This creates a cookie named:

```text
username
```

with value:

```text
Sachin
```

---

## 5. Reading a Cookie

Syntax:

```javascript
document.cookie
```

Example:

```javascript
console.log(document.cookie);
```

Output:

```text
username=Sachin
```

---

## 6. Updating a Cookie

You can update a cookie by assigning a new value.

Example:

```javascript
document.cookie = "username=Virat";
```

Now the cookie value becomes:

```text
username=Virat
```

---

## 7. Deleting a Cookie

Cookies are deleted by setting their expiry date to a past date.

Example:

```javascript
document.cookie =
"username=Sachin; expires=Thu, 01 Jan 1970 00:00:00 UTC;";
```

This removes the cookie.

---

## 8. Example Program

### HTML Document

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Cookies in JavaScript</title>
</head>

<body>

    <button onclick="getCookie()">
        Get Cookie
    </button>

<script>

function setCookie(){

document.cookie =
"message=Nice to meet December Batch Students, All the Very Best !!!";

}

function getCookie(){

setCookie();

if(document.cookie.length==0){

alert("No cookie found");

}

else{

alert("Cookie is set in browser");

}

}

</script>

</body>
</html>
```

---

## 9. Step-by-Step Explanation

### Line 1

```html
<!DOCTYPE html>
```

Declares HTML5 document.

---

### Line 2

```html
<html>
```

Root element of webpage.

---

### Line 3

```html
<button onclick="getCookie()">
```

Creates a button.

When the button is clicked:

```javascript
getCookie()
```

will execute.

---

### Line 4

```javascript
function setCookie()
```

Creates a function to store cookie.

---

### Line 5

```javascript
document.cookie =
"message=Nice to meet December Batch Students";
```

Creates a cookie named:

```text
message
```

with value:

```text
Nice to meet December Batch Students
```

---

### Line 6

```javascript
document.cookie.length
```

Checks whether cookie exists.

---

### Line 7

```javascript
if(document.cookie.length==0)
```

If no cookie exists:

```text
No cookie found
```

will be displayed.

---

### Line 8

```javascript
else
```

If cookie exists:

```text
Cookie is set in browser
```

will be displayed.

---

## Output

After clicking button:

```text
Cookie is set in browser
```

If cookies are disabled:

```text
No cookie found
```

---

## 10. Cookie with Expiry Date

Syntax:

```javascript
document.cookie =
"name=value; expires=date";
```

Example:

```javascript
document.cookie =
"user=Sachin; expires=Fri, 31 Dec 2027 12:00:00 UTC";
```

The cookie remains stored until the specified expiry date.

---

## 11. Cookie with Path

Syntax:

```javascript
document.cookie =
"name=value; path=/";
```

Example:

```javascript
document.cookie =
"user=Sachin; path=/";
```

This cookie becomes accessible throughout the website.

---

## 12. Session Cookie

A session cookie is deleted automatically when the browser closes.

Example:

```javascript
document.cookie =
"sessionId=12345";
```

No expiry date is specified.

---

## 13. Persistent Cookie

A persistent cookie remains even after the browser is closed.

Example:

```javascript
document.cookie =
"user=Sachin; expires=Fri, 31 Dec 2027 12:00:00 UTC";
```

---

## 14. Cookie Properties

Common cookie attributes:

| Property | Description                 |
| -------- | --------------------------- |
| expires  | Expiration date of cookie   |
| max-age  | Lifetime in seconds         |
| path     | Path where cookie is valid  |
| domain   | Domain name                 |
| secure   | Sent only over HTTPS        |
| SameSite | Restricts cross-site access |

---

## Example

```javascript
document.cookie =
"user=Sachin;
expires=Fri, 31 Dec 2027 12:00:00 UTC;
path=/;
secure";
```

---

## Difference Between Session and Persistent Cookies

| Session Cookie               | Persistent Cookie     |
| ---------------------------- | --------------------- |
| Temporary                    | Permanent             |
| Deleted after browser closes | Remains until expiry  |
| No expires attribute         | Has expires attribute |
| Used for login sessions      | Used for preferences  |

---

## Advantages of Cookies

1. Stores user preferences.
2. Maintains user sessions.
3. Easy to implement.
4. Improves user experience.
5. Allows personalization.

---

## Limitations of Cookies

1. Limited storage size (~4KB).
2. User can disable cookies.
3. Security risks if not encrypted.
4. Sent with every HTTP request.
5. Not suitable for large data.

---

## Interview Questions

### Q1. What are Cookies in JavaScript?

**Answer:**

Cookies are small text files stored in the browser to save user-related information.

---

### Q2. Which property is used to create cookies?

**Answer:**

```javascript
document.cookie
```

---

### Q3. Where are cookies stored?

**Answer:**

Cookies are stored as text files in the browser.

---

### Q4. How do you create a cookie?

**Answer:**

```javascript
document.cookie="username=Sachin";
```

---

### Q5. How do you read cookies?

**Answer:**

```javascript
console.log(document.cookie);
```

---

### Q6. How do you delete a cookie?

**Answer:**

Set expiry date to a past date.

```javascript
document.cookie=
"user=Sachin;
expires=Thu, 01 Jan 1970 00:00:00 UTC";
```

---

### Q7. Difference between Session Cookie and Persistent Cookie?

**Answer:**

Session cookie is deleted when browser closes.

Persistent cookie remains until expiry date.

---

### Q8. What is the maximum size of a cookie?

**Answer:**

Approximately:

```text
4 KB
```

---

## Important Points

1. Cookies store small pieces of data.
2. Cookies are stored as text files.
3. JavaScript uses `document.cookie`.
4. Cookies maintain sessions.
5. Cookies can have expiry dates.
6. Cookies improve user experience.
7. Cookies have storage limitations.
8. Cookies are sent with HTTP requests.

---

## Summary

Cookies in JavaScript are small text-based data stored in the browser to preserve user information across multiple requests and sessions. Using the `document.cookie` property, developers can create, read, update, and delete cookies. Cookies are widely used for session management, storing user preferences, authentication, and personalization of websites, making them an essential part of modern web development.
