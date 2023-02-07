## Data Types
A value in JavaScript is always of a certain type. For example, a string or a number.

There are eight basic data types in JavaScript. Here, we’ll cover them in general and in the next chapters we’ll talk about each of them in detail.

We can put any type in a variable. For example, a variable can at one moment be a string and then store a number:
```js
// no error
let message = "hello";
message = 123456;
```
Programming languages that allow such things, such as JavaScript, are called “dynamically typed”, meaning that there exist data types, but variables are not bound to any of them.
### Number
```js
let n = 123;
n = 12.345;
```
The _number_ type represents both integer and floating point numbers.

There are many operations for numbers, e.g. multiplication `*`, division `/`, addition `+`, subtraction `-`, and so on.

Besides regular numbers, there are so-called “special numeric values” which also belong to this data type: `Infinity`, `-Infinity` and `NaN`.
- Infinity represents the mathematical Infinity ∞. It is a special value that’s greater than any number. We can get it as a result of division by zero:
```js
alert( 1 / 0 ); // Infinity
```
Or just reference it directly:
```js
alert( Infinity ); // Infinity
```
