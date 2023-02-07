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

### String
A string in JavaScript must be surrounded by quotes.
```js
let str = "Hello";
let str2 = 'Single quotes are ok too';
let phrase = `can embed another ${str}`;
```
In JavaScript, there are 3 types of quotes.

1.  Double quotes: `"Hello"`.
2.  Single quotes: `'Hello'`.
3.  Backticks: `` `Hello` ``.

Double and single quotes are “simple” quotes. There’s practically no difference between them in JavaScript.

Backticks are “extended functionality” quotes. They allow us to embed variables and expressions into a string by wrapping them in `${…}`, for example:
```js
let name = "John";

// embed a variable
alert( `Hello, ${name}!` ); // Hello, John!

// embed an expression
alert( `the result is ${1 + 2}` ); // the result is 3
```
The expression inside `${…}` is evaluated and the result becomes a part of the string. We can put anything in there: a variable like `name` or an arithmetical expression like `1 + 2` or something more complex.
```ad-important

Please note that this can only be done in backticks. Other quotes don’t have this embedding functionality!
```
```js
console.log( "the result is ${1 + 2}" ); // the result is ${1 + 2} (double quotes do nothing)
```

### Boolean (logical type)
The boolean type has only two values: `true` and `false`.

This type is commonly used to store yes/no values: `true` means “yes, correct”, and `false` means “no, incorrect”.

For instance:
```js
let nameFieldChecked = true; // yes, name field is checked
let ageFieldChecked = false; // no, age field is not checked
```
Boolean values also come as a result of comparisons:
```js
let isGreater = 4 > 1;

alert( isGreater ); // true (the comparison result is "yes")
```

### The "Null" value
The special `null` value does not belong to any of the types described above.

It forms a separate type of its own which contains only the `null` value:
```js
let age = null;
```
In JavaScript, `null` is not a “reference to a non-existing object” or a “null pointer” like in some other languages.

It’s just a special value which represents “nothing”, “empty” or “value unknown”.

The code above states that `age` is unknown.

### The "undefined" value
The special value `undefined` also stands apart. It makes a type of its own, just like `null`.

The meaning of `undefined` is “value is not assigned”.

If a variable is declared, but not assigned, then its value is `undefined`:
```js
let age;

alert(age); // shows "undefined"
```
Technically, it is possible to explicitly assign `undefined` to a variable:
```js
let age = 100;

// change the value to undefined
age = undefined;

alert(age); // "undefined"
```
```ad-tip

…But we don’t recommend doing that. Normally, one uses `null` to assign an “empty” or “unknown” value to a variable, while `undefined` is reserved as a default initial value for unassigned things.
```

## Data Types (Continuation)
### String (Continuation)
There is no difference between " " and ' ' in string. You can choose one of them and stick with it.




## String Methods
### JavaScript String Length
The `length` property returns the length of a string:
```js
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
let length = text.length;

console.log(length);
```
### Extracting String Parts
There are 3 methods for extracting a part of a string:
-   `slice(_start_, _end_)`
-   `substring(_start_, _end_)`
-   `substr(_start_, _length_)`j