# Operators

In programming there are 4 fundamental operations with data.

1. **Assignment**: storing a data value in a variable
2. **Arithmetic**: operators used for mathematical calculations
3. **Comparison**: operators used to compare two values
4. **Logical**: operators used to combine multiple Boolean values or assess the True or False aspects between multiple values

## Assignment Operation

```javascript
let name = "Mr. Park";
```

Assignment operation is a way to store a value into a labeled container called a _**variable**._

## Arithmetic Operation

<table><thead><tr><th width="120">Symbol</th><th>Operators</th></tr></thead><tbody><tr><td>+</td><td>Addition</td></tr><tr><td>-</td><td>Subtraction</td></tr><tr><td>*</td><td>Multiplication</td></tr><tr><td>**</td><td>Exponentiation</td></tr><tr><td>/</td><td>Division</td></tr><tr><td>%</td><td>Modulus (Division Remainder)</td></tr><tr><td>++</td><td>Increment</td></tr><tr><td>--</td><td>Decrement</td></tr></tbody></table>

Arithmetic operations all require two values (a left operand and a right operand) except for the increment and decrement operators.

{% tabs %}
{% tab title="Example Code" %}
```javascript
// Arithmetic Examples:
let x = 10;
let y = 5;

console.log(x + y);
console.log(x - y);
console.log(x * y);
console.log(x / y);
console.log(x ** y);
console.log(x % y);

console.log(x++);
console.log(y--);
```
{% endtab %}

{% tab title="Output" %}
```
15
5
50
2
100000
0
10
5
```
{% endtab %}
{% endtabs %}

### Comparison & Logical Operator

Comparison and Logical operators will be explained in a future lesson when we learn how to do decision making with programming.

## Related Readings

* Operators ([Link](https://javascript.info/operators))

