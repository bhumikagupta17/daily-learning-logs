# 🚀 JavaScript: Async Programming & Fetch API

---

## 1. Synchronous vs Asynchronous JavaScript

### 🔹 Synchronous JavaScript
**Definition:**  
Code runs in a particular sequence of instructions.

**Behavior:**  
Each instruction **waits** for the previous instruction to complete its execution.

**Problem:**  
If an instruction takes too long, it causes a **block** in the flow, leading to delays in the UI.

---

### 🔹 Asynchronous JavaScript
**Definition:**  
Allows the program to execute next instructions **immediately** without waiting for the previous one to finish.

**Benefit:**  
Ensures that the execution flow is not blocked by heavy tasks.

**Example:**
```
console.log("1");
console.log("2");

// Runs parallelly as it has a delay of 4 sec.
setTimeout(() => {
  console.log("Hello");
}, 4000);

console.log("3");
console.log("4");

// Output: 1, 2, 3, 4, Hello
```
## 2. Callbacks
### 🔹 Definition
- A function passed as an argument to another function.

### 🔹 Important Rules
- When passing a function as a callback, do NOT use parentheses ().
- Using parentheses executes the function immediately instead of passing it.
- Correct:
```
calculator(1, 2, sum);
```

- Incorrect:
```
calculator(1, 2, sum());
```
### 🔹 Callback Hell (Pyramid of Doom)
- Definition:
Nested callbacks stacked below one another, forming a pyramid structure.

- Issue:
Makes the code very difficult to understand, debug, and manage.

- Error Example:
```
getData(1, getData(2));
```

❌ This causes an error because the second function is called immediately instead of being passed as a reference.

## 3. Promises

- Definition:
Promises are the solution to callback hell. A Promise is an object representing the eventual completion or failure of a task.

### 🔹 Promise States

- Pending: Initial state; result is undefined (waiting).
- Fulfilled (Resolved): Task completed successfully; result is a value.
- Rejected: Task failed; result is an error object.

### 🔹 Using Promises

- .then() → Executes when promise is fulfilled.
- .catch() → Executes when promise is rejected.

### 🔹 Promise Chain

- Returning a promise inside .then() to ensure sequential execution.
```
getData(1)
  .then(() => getData(2))
  .then(() => getData(3));
```

## 4. Async / Await
### 🔹 async Function
- An async function always returns a promise.

### 🔹 await Keyword
- Pauses the execution of the surrounding async function until the promise is settled.
- Logic:
  - First call finishes → then second call starts.
- Example:
```
async function fetchData() {
  const res = await fetch(url);
  const data = await res.json();
  console.log(data);
}

fetchData();
```

## 5. IIFE (Immediately Invoked Function Expression)
### 🔹 Definition
- A function that is called immediately after it is defined.

### 🔹 Purpose
- Eliminates the need to create a named function just to call it once.

### 🔹 Syntax Types
```
(function () { ... })();

(() => { ... })();

(async () => { ... })();
```
## 6. Fetch API & JSON
### 🔹 Fetch API
- Provides an interface for fetching (sending/receiving) resources via Request/Response objects.

### 🔹 Process Flow
- fetch(url) returns a promise.
  - The response is not directly readable.
  - response.json() returns another promise.
  - Final result is a usable JS object.

- Example:
```
fetch(url)
  .then(res => res.json())
  .then(data => console.log(data))
  .catch(err => console.log(err));
```

## 7. HTTP Basics

### 🔹 HTTP Verbs

| Method | Purpose       |
|--------|----------------|
| GET    | Retrieve data  |
| POST   | Send data      |
| PUT / PATCH | Update data |
| DELETE | Delete data    |


### 🔹 Response Status Codes

| Code Range | Meaning                          |
|-------------|----------------------------------|
| 100–199     | Informational responses          |
| 200–299     | Successful                       |
| 400–499     | Client-side errors (e.g., 404)   |
| 500–599     | Server-side errors              |

