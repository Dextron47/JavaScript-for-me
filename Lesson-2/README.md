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




