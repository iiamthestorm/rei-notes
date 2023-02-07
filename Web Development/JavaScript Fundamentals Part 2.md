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
-   `substr(_start_, _length_)`

#### JavaScript String slice()
`slice()` extracts a part of a string and returns the extracted part in a new string.

The method takes 2 parameters: start position, and end position (end not included).
```js
let text = "Apple, Banana, Kiwi";
let part = text.slice(7, 13);

console.log(part);
```
```ad-attention

JavaScript counts positions from zero.
First position is 0.
Second position is 1.
```
If you omit the second parameter, the method will slice out the rest of the string:
```js
let text = "Apple, Banana, Kiwi";  
let part = text.slice(7);

console.log(part);
```
If a parameter is negative, the position is counted from the end of the string:
```js
let text = "Apple, Banana, Kiwi";
let part = text.slice(-12);

console.log(part);
```
This example slices out a portion of a string from position -12 to position -6:
```js
let text = "Apple, Banana, Kiwi";
let part = text.slice(-12, -6);

console.log(part);
```

#### JavaScript String substring()
`substring()` is similar to `slice()`.

The difference is that start and end values less than 0 are treated as 0 in `substring()`.

```ad-hint

It means that you can't five minus value as it will be treated as 0.
```
If you omit the second parameter, `substring()` will slice out the rest of the string.

#### JavaScript String substr()
`substr()` is similar to `slice()`.

The difference is that the second parameter specifies the **length** of the extracted part.












### Replacing String Content
The `replace()` method replaces a specified value with another value in a string:
```js
let text = "Please visit Microsoft!";
let newText = text.replace("Microsoft", "W3Schools");

console.log(newText);
```
```ad-info

The `replace()` method does not change the string it is called on.
The `replace()` method returns a new string.
The `replace()` method replaces **only the first** match
If you want to replace all matches, use a regular expression with the /g flag set. See examples below.
```
To replace case insensitive, use a **regular expression** with an `/i` flag (insensitive):
```js
let text = "Please visit Microsoft!";
let newText = text.replace(/MICROSOFT/i, "W3Schools");

console.log(newText);
```
```ad-info

Regular expressions are written without quotes.
```
To replace all matches, use a **regular expression** with a `/g` flag (global match):
```js
let text = "Please visit Microsoft and Microsoft!";
let newText = text.replace(/Microsoft/g, "W3Schools");

console.log(newText);
```

### JavaScript String ReplaceAll()
In 2021, JavaScript introduced the string method replaceAll():
```js
let text = "I love cats. Cats are very easy to love. Cats are very popular."
text = text.replaceAll("Cats","Dogs");
text = text.replaceAll("cats","dogs");

console.log(text);
```
The `replaceAll()` method allows you to specify a regular expression instead of a string to be replaced.

If the parameter is a regular expression, the global flag (g) must be set set, otherwise a TypeError is thrown.
```js
let text = "I love cats. Cats are very easy to love. Cats are very popular";
text = text.replaceAll(/Cats/g,"Dogs");
text = text.replaceAll(/cats/g,"dogs");

console.log(text);
```
```ad-info

`replaceAll()` is an [ES2021](https://www.w3schools.com/js/js_2021.asp) feature.
`replaceAll()` does not work in Internet Explorer.
```







### Converting to Upper and Lower Case
A string is converted to upper case with `toUpperCase()`:
A string is converted to lower case with `toLowerCase()`:
#### JavaScript String toUpperCase()
```js
let text1 = "Hello World!";
let text2 = text1.toUpperCase();

console.log(text2);
```
#### JavaScript String toLowerCase()
```js
let text1 = "Hello World!";       // String
let text2 = text1.toLowerCase();  // text2 is text1 converted to lower

console.log(text2);
```