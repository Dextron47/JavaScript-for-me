# 🔹 Strings in JavaScript

A **string** is a sequence of characters used to represent text.  
In JavaScript, strings are **surrounded by quotes**:

- **Single quotes**: `'Hello'`
- **Double quotes**: `"Hello"`
- **Backticks** (Template literals): `` `Hello` ``

---

## 🔹 Declaring Strings

```javascript
let firstName = "Sudhanshu";
let lastName = 'Jha';
let greeting = `Hello, ${firstName}!`; // using template literals
```

## 🔹 String Concatenation

You can combine (join) strings using the + operator or template literals.

```javascript
let fullName = firstName + " " + lastName;
console.log(fullName); // Sudhanshu Jha
```

✅ Or use template literals:

```javascript
let fullName = `${firstName} ${lastName}`;
```
## 🔹 String Properties and Methods
JavaScript provides several built-in string methods:

|Method|Description|Example|
|---|---|---|
|length|Returns length of string |	"hello".length → 5|
|toUpperCase()|	Converts to uppercase|	"hello".toUpperCase() → "HELLO"|
|toLowerCase()| Converts to lowercase|	"HELLO".toLowerCase() → "hello"|
|includes()| Checks if string contains a substring|	"apple".includes("p") → true|
|indexOf()|	Returns index of substring|	"banana".indexOf("n") → 2|
|slice(start, end)|	Extracts part of string| "JavaScript".slice(0, 4) → "Java"|
|trim()| Removes whitespace from both ends| " hello ".trim() → "hello"|
|replace()|	Replaces part of string|	"hello".replace("h", "y") → "yello"|


## 🔹 Type Coercion in JavaScript

**Type coercion** in JavaScript refers to the **automatic or implicit conversion of values** from one data type to another.

JavaScript is a **dynamically typed** language — which means you don’t need to declare the type of a variable.  

Because of that, it sometimes **converts types automatically** when performing operations.

---

## 🔸 Types of Coercion

### ✅ Implicit Coercion
JavaScript **automatically converts** types behind the scenes.

```javascript
let result = "5" + 2;  // "52" → number 2 is converted to string
let sum = "5" - 2;     // 3   → string "5" is converted to number
```

🔸 Implicit Coercion Examples
```javascript
"10" + 5       // "105"   → number becomes string
"10" - 5       // 5       → string becomes number
"10" * "2"     // 20      → both strings converted to numbers
true + 1       // 2       → true becomes 1
false + 1      // 1       → false becomes 0
null + 1       // 1       → null becomes 0
undefined + 1  // NaN     → undefined cannot be coerced to number
```

✅ Explicit Coercion

You manually convert values using functions like Number(), String(), or Boolean().

```javascript
Number("123");     // 123
String(123);       // "123"
Boolean(0);        // false
```

🔸 Explicit Coercion Examples
```javascript
let str = "42";
let num = Number(str);     // 42
let boolVal = Boolean(""); // false (empty string)
let boolVal2 = Boolean("hi"); // true (non-empty string)
let strFromBool = String(true); // "true"
```

## 🔹 Escape Characters
Use a backslash \ to escape characters inside strings:

```javascript
let quote = 'It\'s a nice day';
let path = "C:\\Users\\Dextron47";
```
## 🔹 What is String Interpolation in JavaScript?

String interpolation is a way to insert variables or expressions into strings.

In JavaScript, this is done using template literals, which are strings enclosed in backticks (``) instead of single or double quotes.

✅ Syntax:
```javascript
`string text ${expression} string text`
```

✅ Example:
```javascript
let name = "Alice";
let age = 22;

let message = `Hello, my name is ${name} and I am ${age} years old.`;
console.log(message);
// Output: Hello, my name is Alice and I am 22 years old.
```

Here:

- **name** and **age** are placeholders.
- JavaScript evaluates them and injects their values into the string.

## 🔹 Why use interpolation?
String interpolation with template literals:

- Is cleaner and more readable than concatenation.
- Allows multiline strings.
- Supports expression evaluation inside ${}.

✅ You can even do calculations:
```javascript
let x = 5;
let y = 10;
console.log(`The sum of x and y is ${x + y}`);
// Output: The sum of x and y is 15
```

## 🔹 Comparison with Concatenation:

Concatenation:

```javascript
let result = "Hello " + name + ", you are " + age + " years old.";
```

Interpolation:

```javascript
let result = `Hello ${name}, you are ${age} years old.`;
```
✅ Interpolation is cleaner, especially when dealing with longer strings or multiple variables.

## 🔹 Multiline Strings
Using template literals, you can write multiline strings:

```javascript
let message = `Hello,
This is a multiline
string in JavaScript.`;
```

## 🔹 Practice 
1️⃣ What will this print?

```javascript
let name = "JavaScript";
console.log(name.length);
```
2️⃣ Combine firstName = "Ada" and lastName = "Lovelace" into one string using template literals.
3️⃣ Extract the word "Script" from "JavaScript" using .slice().

✅ Answers:

1️⃣ 10

2️⃣ `${firstName} ${lastName}` → "Ada Lovelace"

3️⃣ "JavaScript".slice(4) → "Script"


string = text