# JavaScript: Objects, Classes, and Inheritance

## 1. Objects & Prototypes
- **Object:** An entity with state (properties) and behavior (methods).
- **Prototype:** A special property in every JS object.
- **```__proto__```:** Used to set an object's prototype to inherit methods (e.g., ```karanArjun.__proto__ = employee```).
- **Priority:** If an object and its prototype have the same method, the object's method is used.

## 2. Classes in JS
- **Definition:** A template for creating objects.
- **Method Implementation:**
```
class Toyota {
  setBrand(brand) {
    this.brandName = brand; // "this" refers to the specific object property
  }
}
```

## 3. The Constructor
- **Automatic Invocation:** The constructor is automatically invoked by the new keyword.
- **Purpose:** It is used to initialize the object at the time of creation.
- **Parameters:** You can pass arguments to the constructor to set initial values.
- **Behavior Note:** If a class defines parameters but you do not pass arguments during creation, the code still executes (the values simply remain undefined).
```
class MyClass {
  constructor(arg) {
    console.log("Initialized with:", arg);
  }
}
let obj = new MyClass("data"); // Automatically triggers constructor
```

## 4. Inheritance & super Keyword
- **Inheritance:** Reuse code using the syntax class Child extends Parent.
- **Method Overriding:** If the Child and Parent have the same method, the Child's version is used.
- **super Keyword:** * Used to call the constructor of the parent class to access parent properties.
- **Mandatory Rule:** In a derived class, you must call super() before using this or exiting the constructor (invoke karna hi padhega).
- **Value Passing:** Object creation involves assigning values to the parent constructor by passing them through the child constructor into super().

## 5. Error Handling
- **Try-Catch:** Used to manage potential crashes without stopping the program.
- **Try Block:** Wraps the code that might fail.
- **Catch Block:** Handles the resulting Error Object if an error occurs.
