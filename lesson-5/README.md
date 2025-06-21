# 🔹 Variables in JavaScript

A **variable** is a container for storing data values like numbers, strings, or objects.  
Think of it as a **label** for data you want to use and manipulate later in your program.

---

## 🔸 Declaring Variables

In JavaScript, you can declare variables using:

- `var` (old, avoid using)
- `let` (block-scoped, modern)
- `const` (block-scoped, constant)

---

### ✅ Using `let`

```javascript
let name = "Dextron";
let age = 21;

console.log(name); // Dextron
```

### ✅ Using const
```javascript
const country = "India";
```
❌ You cannot change the value of a const variable:

```javascript
country = "USA"; // ❌ Error
```
### ⚠️ Using var (Avoid)
```javascript
var score = 100;
```
var has function scope (not block scope) and can lead to bugs. Use let or const instead.

## 🔹 Syntax Rules for Variables in JavaScript

To declare variables properly in JavaScript, you must follow certain **syntax rules**.  
Breaking these rules will result in **errors** or **unexpected behavior**.

---

### ✅ 1. Use `let`, `const`, or `var` to declare variables

```javascript
let name = "Alice";
const age = 25;
var score = 100;
```

❌ Don’t declare a variable without a keyword (will create a global variable):

```javascript
name = "Bob"; // Not recommended
```

### ✅ 2. Variable names must start with a letter, $, or _
```javascript
let city = "Mumbai";
let $price = 100;
let _score = 10;
```
❌ Invalid examples:
```javascript
let 1user = "Sam"; // ❌ starts with number
let *name = "Jon"; // ❌ invalid 
```

### ✅ 3. Variable names are case-sensitive
```javascript
let username = "john";
let Username = "jane";
These are two different variables.
```

### ✅ 4. Variable names cannot use reserved keywords

Reserved words like let, class, function, return, etc., cannot be used as variable names.

```javascript
let function = "doSomething"; // ❌ Error
```

### ✅ 5. Variable names should be descriptive

Good naming helps make your code clear and readable:

```javascript
let x = 10;           // ❌ Bad
let studentAge = 10;  // ✅ Good
```

### ✅ 6. You can declare multiple variables in one line (but not recommended for beginners)
```javascript
let a = 1, b = 2, c = 3;
```
For better readability, declare one variable per line.

### ✅ 7. Reassignment rules:

let and var variables can be reassigned:

```javascript
let score = 10;
score = 15; // ✅ OK
```
const variables cannot be reassigned:

```javascript
const pi = 3.14;
pi = 3.14159; // ❌ Error
```

### 🔸 Summary Table
|Rule	|Valid? |	Example|
| --- | --- | --- |
|Starts with letter, $, or _|	✅	|let _user = "John";|
|Starts with a number	|❌|	let 1user = "John";|
|Uses reserved keyword	|❌|	let return = 10;|
|Case sensitive	|✅|	user ≠ User|
|Declared without keyword (let, etc.)|	❌|	name = "Sam";|
|Reassign with let	|✅|	let x = 5; x = 10;|
|Reassign with const	|❌|	const y = 5; y = 10;|

### 🔸 Practice 
Mark these as ✅ Valid or ❌ Invalid:

1️⃣ let 123age = 20;
2️⃣ let $price = 99;
3️⃣ let return = 5;
4️⃣ const user = "Jane"; user = "Jake";
5️⃣ let name = "Bob";

✅ Answers:
1️⃣ ❌
2️⃣ ✅
3️⃣ ❌
4️⃣ ❌
5️⃣ ✅

## Naming convention
| Case | Example | 
| --- | --- |
|camelCase|      cartQuantity|
|PascalCase|    CartQuantity|
|underscore(snake_case)|     cart_quantity|
|kebab-case|     cart-quantity // not recommended in JavaScript|