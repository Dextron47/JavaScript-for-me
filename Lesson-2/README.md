# Numbers and Maths in JavaScript

## Numbers

Numbers are a **primitive data type** in JavaScript.  
They can be **integer or floating-point** (with decimal points), and JavaScript doesn’t distinguish between the two — it's all `Number`.

✅ Numbers can be integer or decimal (floating) in JavaScript.
✅ Operations like +, -, *, /, %, ** are supported.
✅ The Math object lets you perform advanced operations.
✅ Parsing methods (parseInt, parseFloat, Number) help you convert strings into numbers.

---

### 🔹 Examples:

```javascript
// Integer
let age = 25;

// Floating point
let price = 19.99;

// Negative number
let temperature = -5;

```

## Maths Operations

You can perform all the common mathematical operations in JavaScript:

✅ Addition (+)

```javascript
2 + 3; // 5
```

✅ Subtraction (-)

```javascript
10 - 4; // 6
```
✅ Multiplication (*)

```javascript
5 * 2; // 10
```
✅ Division (/)

```javascript
20 / 4; // 5
```
✅ Modulus (%) — remainder of division

```javascript
10 % 3; // 1
```
✅ Exponentiation (**)

```javascript
2 ** 3; // 8
```

## 🔹 Order of Operations in JavaScript

Just like in regular math, JavaScript follows a **specific order** when performing multiple operations in a single expression.  
This is known as the **Order of Operations**, also called **Operator Precedence**.

---

### 🔹 The BODMAS Rule

JavaScript follows a similar rule to **BODMAS** (also known as PEMDAS):

**B**rackets  
**O**rders (Exponents: powers and roots)  
**D**ivision  
**M**ultiplication  
**A**ddition  
**S**ubtraction

---

## 🔹 Example:

```javascript
let result = 5 + 3 * 2;
console.log(result); // 11
```

🔹 With Brackets:

```javascript
let result = (5 + 3) * 2;
console.log(result); // 16
```
✅ Brackets change the default order. Addition happens first, then multiplication.

🔹 Full Precedence Example:

```javascript
let result = (10 + 2) * 3 ** 2 / 6 - 4;
console.log(result); // Output: 2
```

Step-by-step:
1. Parentheses: (10 + 2) → 12
2. Exponent: 3 ** 2 → 9
3. Multiply: 12 * 9 → 108
4. Divide: 108 / 6 → 18
5. Subtract: 18 - 4 → 14

JavaScript follows these rules when evaluating expressions:

Priority |	Operation Type                          | Example
1        |	Brackets ()                             | (a + b)
2        |	Exponentiation **                       | 2 ** 3
3	     |  Multiplication *, Division /, Modulo %	| a * b / c
4	     |  Addition +, Subtraction -	            | a + b - c

Use parentheses () to control and clarify the order of operations!

🔹 Practice 
What will be the result of the following?

```javascript
let answer = 4 + 6 * (10 - 8) ** 2;
```
Try it yourself before checking the answer below.

Answer:

Parentheses: (10 - 8) → 2
Exponent: 2 ** 2 → 4
Multiply: 6 * 4 → 24
Add: 4 + 24 → 28

### 🔹 In programming: 
2,3, 4 = integers 
2.2, 2.5 = floating point numbers(floats)
Computer have a problem working with floats.

### 🔹 Example 
```javascript
0.1 + 0.2 // 0.30000000000000004
```
🔹 While calculating money, we want to avoid this inacurracies
```javascript
20.95 + 7.99 // 28.939999999999998
2095 + 799 // 2894
(2095 + 799) / 100 // 28.94
```
Calculations with floats are sometimes inaccurate.
when working with money,
1. Do the calculation in cents 
2. Convert back to dollars

### 🔹 Math Object:
JavaScript provides a Math object with numerous methods to perform advanced operations:

```javascript
Math.round(4.7); // 5
Math.floor(4.7); // 4
Math.ceil(4.2); // 5
Math.random(); // a number between 0 and 1
Math.max(10, 20, 30); // 30
Math.min(10, 20, 30); // 10
Math.abs(-5); // 5
Math.pow(2, 4); // 16
Math.sqrt(25); // 5
```
### 🔹 Parsing and Conversion:
Sometimes you need to convert strings to numbers.
JavaScript provides:

✅ parseInt() — parses a string into an integer:
```javascript
parseInt("42"); // 42
parseInt("42px"); // 42
parseInt("3.14"); // 3
```

✅ parseFloat() — parses a string into a float:
```javascript
parseFloat("3.14"); // 3.14
parseFloat("42.5px"); // 42.5
```

✅ Number() — converts directly to a number:
```javascript
Number("42"); // 42
Number("3.14"); // 3.14
```




