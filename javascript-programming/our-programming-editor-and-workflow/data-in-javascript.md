# Data in JavaScript

In programming, a concept of data type is important to label and classify any digital information given. This is important because the program must know the characteristics of the information because a _computer cannot understand the information given_.

Therefore, different data in programming have **data types.**

## The Data Types in JavaScript

There are two sub-groups of data types: **primitive** and **non-primitive**

**Primitive**: Primitive data types are the most basic data types in JavaScript. They are immutable, meaning their values cannot be changed once created. Each primitive type represents a single value.

**Non-Primitive:** Non-primitive data types, also known as reference types, are more complex. They can hold collections of values and more complex entities. Unlike primitive types, non-primitive types are mutable, meaning their values can be changed.

* **Immutability**: Primitive types are immutable, while non-primitive types are mutable.
* **Storage**: Primitive types store the actual value, whereas non-primitive types store references to the values.

### Primitive Data Types

**String**: Represents textual data.

```javascript
let name = "Alice";
```

**Number**: Represents both integer and floating-point (_approximation of real_) numbers.

```javascript
let age = 30;
let price = 19.99;
```

**Boolean**: Represents a logical entity and can have two values: `true` or `false`.

```javascript
let isStudent = true;
```

**Undefined**: A variable that has been declared but not assigned a value.

```javascript
let x;
console.log(x); // undefined
```

**Null**: Represents the intentional absence of any object value.

```javascript
let y = null;
```

**Symbol**: A unique and immutable primitive value, often used as keys for object properties.

```javascript
let sym = Symbol('description');
```

**BigInt**: Represents integers with arbitrary precision.

```javascript
let bigNumber = BigInt(1234567890123456789012345678901234567890n);
```

_In this introductory programming course, we will not be learning non-primitive data types._

## Recommended Readings

* Data Types ([Link](https://javascript.info/types))

