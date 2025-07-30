# 🔹 What is Hoisting in JavaScript?

**Hoisting** is JavaScript's default behavior of **moving declarations to the top of their scope** (either the function or the global scope) **before the code is executed**.

This means you can sometimes use variables **before** you declare them.


```javascript
greet()
function greet()
{
    console.log("Good morning!")
} // It works
```

---

## 🔸 1. Variable Hoisting with `var`

```javascript
console.log(a); // undefined
var a = 10;
```

👉 Behind the scenes, JavaScript rewrites it like this:
```javascript
var a;
console.log(a); // undefined
a = 10;
```
✅ The declaration (var a) is hoisted, but the assignment (a = 10) is not.

## 🔸 2. let and const Are Hoisted Too, BUT…
They are hoisted to the top of the block without being initialized, so accessing them before declaration gives a ReferenceError.

```javascript
console.log(b); // ❌ ReferenceError
let b = 20;

console.log(c); // ❌ ReferenceError
const c = 30;
```

This is because they are in a "temporal dead zone" — a period between entering the scope and the actual declaration.

## 🔸 3. Function Hoisting
✅ Function declarations are fully hoisted (both the name and body):

```javascript
greet(); // Hello!
function greet() {
  console.log("Hello!");
}
```
❌ Function expressions are not fully hoisted:

```javascript
sayHi(); // ❌ TypeError: sayHi is not a function

var sayHi = function() {
  console.log("Hi!");
};
```

🔸 Summary
|Declaration Type|	Hoisted?|	Initialized?|	Can use before declaration?|
|--------------|---------|-----------|--------|
|var|	✅ Yes|	✅ As undefined|	✅ |(but not recommended)|
|let/const|	✅ Yes|	❌ No|	❌ ReferenceError|
|function (declared)|	✅ Yes|	✅ Yes|	✅|
|Function expression|	✅ (var)|	❌ No|	❌|

## 🔸 Visual Example:
```javascript
console.log(x); // undefined
var x = 5;

console.log(y); // ReferenceError
let y = 10;

greet(); // Hello
function greet() {
  console.log("Hello");
}
```

## 🔸 Practice (Optional)
1️⃣ What is the output?

```javascript
console.log(title);
var title = "JS Tutorial";
```
2️⃣ What happens here?

```javascript
console.log(num);
let num = 42;
```
3️⃣ Will this function call work?


```javascript
sayHello();

const sayHello = function () {
  console.log("Hi!");
};
```
### ✅ Answers:
1️⃣ undefined

2️⃣ ReferenceError: Cannot access 'num' before initialization

3️⃣ TypeError: sayHello is not a function