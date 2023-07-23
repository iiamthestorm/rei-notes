## Cara run JavaScript
ada beberapa cara untuk running javascript, bisa di browser dan juga bisa di luar browser environtment.
Cara yang paling simple untuk membuat sciprt js adalah dengan html:
```html
<html>
<head>
  <meta charset="UTF-8">
  <title>Page Title</title>
</head>
<body>
  <script>
    // Your javascript code
    console.log("Hello World")
  </script>
</body>
</html>
```
simpan kode diatas dan jalankan browser dengan live preview plugin di vscode studio. And open inspect elemen on the browser itself. In the 'Developer Tools' pane, find and select console tab. Disana akan ketemu output nya. ```console.log()``` berguna untuk print sesuatu ke developer console di browser.

Anotherway to include javascript in a webpage is through an external script. Hampir mirip dengan CSS. Contoh:
Ini file html nya:
```html
<script src="javascript.js"></script>
```
ini file js nya:
```js
console.log("Hello World")
```

## Variables JavaScript
resource : https://javascript.info/variables, https://www.w3schools.com/js/js_numbers.asp
### console.log () & alert() differences
```js
let message;
message = 'Hello';
alert(message);
console.log(message);
```
```alert```() gunanya adalah untuk menampilkan pesan ketika halaman web page dibuka. Sedangkan ```console.log()``` hanya berguna untuk menampilkan pesan di console tab.

Variable js juga bisa dideklarasikan langsung kepada isi nya, seperti :
```js
let message = 'Hello';
alert(message);
console.log(message);
```
code di atas lebih mudah untuk dibaca.
### Multiline Variables
Variables multiline style is possible in js. for example:
```js
let user = 'John',
	age = 25,
	message = 'Hello';
```
bahkan dengan "comma-first" style:
```js
let user = 'John'
	, age = 25
	, message = 'Hello';
```
### Variable Naming
ada 2 limitations on variabel naming on js :
1. Namanya cuman bisa letters, digit, $, __
Contohnya:
```js
let $ = 1;
let _ = 2;_

alert($ + __);
```
3. Karakter pertama variable tidak boleh angka

Karakter non-latin boleh dipakai, tetapi tidak direkomendasikan seperti chinese, japanese kanji dll.
```js
let 冬眠 = "sleep"
let 春泥棒 = "Spring Thief"

console.log(冬眠);
alert(春泥棒);
```
Normally, we need to define a variable before using it. But in the old times, it was technically possible to create a variable by a mere assignment of the value without using `let`. This still works now if we don’t put `use strict` in our scripts to maintain compatibility with old scripts.
```js
// note: no "use strict" in this example
num = 5; // the variable "num" is created if it didn't exist
alert(num); // 5
```
This is a bad practice and would cause an error in strict mode:
```js
"use strict"; 

_num = 5; // error: num is not defined_
```
### Perbedaan let, var dan const
```let``` = sudah menjadi modern variable declaration.
```var``` = old school variable declaration.
`const` = kayak let cuman const value nya ga bisa di change.
### JavaScript Numbers are Always 64-bit Floating Point
Unlike many other programming languages, JavaScript does not define different types of numbers, like integers, short, long, floating-point etc.

JavaScript numbers are always stored as double precision floating point numbers, following the international IEEE 754 standard.

This format stores numbers in 64 bits, where the number (the fraction) is stored in bits 0 to 51, the exponent in bits 52 to 62, and the sign in bit 63:
![[Pasted image 20230206145420.png]]

### Adding Numbers and Strings
```ad-warning

JavaScript uses the + operator for both addition and concatenation. Numbers are added. Strings are concatenated.
```
If you add two strings, the result will be a string concatenation:
```js
let x = "10";
let y = "20";
let z = x + y;
```
If you add two numbers, the result will be a number:
```js
let x = 10;
let y = 20;
let z = x + y;
```
If you add a number and a string, the result will be a string concatenation:
```js
let x = 10;  
let y = "20";  
let z = x + y;
```
If you add a string and a number, the result will be a string concatenation:
```js
let x = "10";  
let y = 20;  
let z = x + y;
```
A common mistake is to expect this result to be 30 :
```js
let x = 10;
let y = 20;
let z = "The result is: " + x + y;
// the result is 1020
```
A common mistake is to expect this result to be 102030 :
```js
let x = 10;
let y = 20;
let z = "30";
let result = x + y + z;
// the result 3030
// x + y = 30 (number)
// (x + y) + z (string)
// 30 + "30" = 3030.
```
### Numeric Strings
JavaScript strings can have numeric content :
```js
let x = 100;         // x is a number

let y = "100";       // y is a string
```
JavaScript will try to convert strings to numbers in all numeric operations. This will work:
```js
let x = "100";
let y = "10";
let z = x / y;
```

### NaN - Not a Number
`NaN` is a JavaScript reserved word indicating that a number is not a legal number. Trying to do arithmetic with a non-numeric string will result in `NaN` (Not a Number):
```js
let x = 100 / "Apple";
console.log(x);
// This will result in NaN.
```
However, if the string contains a numeric value , the result will be a number:
```js
let x = 100 / "10";
console.log(x);
```
You can use the global JavaScript function `isNaN()` to find out if a value is a not a number:
```js
let x = 100 / "Apple";
isNaN(x);
```
Watch out for `NaN`. If you use `NaN` in a mathematical operation, the result will also be `NaN`:
```js
let x = NaN;  
let y = 5;  
let z = x + y;
console.log(z);
```
Or the result might be a concatenation like NaN5:
```js
let x = NaN;
let y = "5";
let z = x + y;
console.log(z);
```
`NaN` is a number: `typeof NaN` returns `number`:
```js
typeof NaN;
```

### Infinity
`Infinity` (or `-Infinity`) is the value JavaScript will return if you calculate a number outside the largest possible number.
```js
let myNumber = 2;  
// Execute until Infinity  
while (myNumber != Infinity) {  
  myNumber = myNumber * myNumber;  
}
```
Division by 0 (zero) also generates `Infinity`:
```js
let x =  2 / 0;  
let y = -2 / 0;
```
`Infinity` is a number: `typeof Infinity` returns `number`.
```js
typeof Infinity;
```

### Hexadecimal
JavaScript interprets numeric constants as hexadecimal if they are preceded by 0x.
```js
let x = 0xFF;
```
```ad-warning

Never write a number with a leading zero (like 07).  
Some JavaScript versions interpret numbers as octal if they are written with a leading zero.
```
By default, JavaScript displays numbers as **base 10** decimals.

But you can use the `toString()` method to output numbers from **base 2** to **base 36**.

Hexadecimal is **base 16**. Decimal is **base 10**. Octal is **base 8**. Binary is **base 2**.
```js
let myNumber = 32;  
myNumber.toString(32);  
myNumber.toString(16);  
myNumber.toString(12);  
myNumber.toString(10);  
myNumber.toString(8);  
myNumber.toString(2);
```

### JavaScript Numbers as Objects
Normally JavaScript numbers are primitive values created from literals:
```js
let x = 123;
```
But numbers can also be defined as objects with the keyword `new`:
```js
let y = new Number(123);
```
```js
let x = 123;  
let y = new Number(123);
```
```ad-warning

Do not create Number objects.

The `new` keyword complicates the code and slows down execution speed.

Number Objects can produce unexpected results:
```
When using the `==` operator, x and y are **equal**.
When using the `===` operator, x and y are **not equal**.
```ad-warning

Comparing two JavaScript objects **always** returns **false**.

```

### Numeric conversion, unary +
The plus `+` exists in two forms: the binary form that we used above and the unary form.

The unary plus or, in other words, the plus operator `+` applied to a single value, doesn’t do anything to numbers. But if the operand is not a number, the unary plus converts it into a number.

For example:
```js
// No effect on numbers
let x = 1;
alert( +x ); // 1

let y = -2;
alert( +y ); // -2

// Converts non-numbers
alert( +true ); // 1
alert( +"" );   // 0
```
It actually does the same thing as `Number(...)`, but is shorter.

The need to convert strings to numbers arises very often. For example, if we are getting values from HTML form fields, they are usually strings. What if we want to sum them?

The binary plus would add them as strings:
```js
let apples = "2";
let oranges = "3";

alert( apples + oranges ); // "23", the binary plus concatenates strings
```
If we want to treat them as numbers, we need to convert and then sum them:
```js
let apples = "2";
let oranges = "3";

// both values converted to numbers before the binary plus
console.log(+apples + +oranges);

// the longer variant
// alert( Number(apples) + Number(oranges) ); // 5
```
From a mathematician’s standpoint, the abundance of pluses may seem strange. But from a programmer’s standpoint, there’s nothing special: unary pluses are applied first, they convert strings to numbers, and then the binary plus sums them up.

Why are unary pluses applied to values before the binary ones? As we’re going to see, that’s because of their _higher precedence_.

### Operator Precedence
If an expression has more than one operator, the execution order is defined by their precedence, or, in other words, the default priority order of operators.

From school, we all know that the multiplication in the expression 1 + 2 * 2 should be calculated before the addition. That’s exactly the precedence thing. The multiplication is said to have a higher precedence than the addition.

Parentheses override any precedence, so if we’re not satisfied with the default order, we can use them to change it. For example, write (1 + 2) * 2.

There are many operators in JavaScript. Every operator has a corresponding precedence number. The one with the larger number executes first. If the precedence is the same, the execution order is from left to right.

Here’s an extract from the precedence table (you don’t need to remember this, but note that unary operators are higher than corresponding binary ones):

| Precedence | Name           | Sign |
| ---------- | -------------- | ---- |
| ...        | ...            | ...  |
| 14         | unary plus     | +    |
| 14         | unary negation | -    |
| 13         | exponentiation | **   |
| 12         | multiplication | *    |
| 12         | division       | /    |
| 11         | addition       | +    |
| 11         | substraction   | -    |
| ...        | ...            | ...  |
| 2          | assignment     | =    |
| ...           |   ...             | ...     |

As we can see, the “unary plus” has a priority of 14 which is higher than the 11 of “addition” (binary plus). That’s why, in the expression "+apples + +oranges", unary pluses work before the addition.

### Bitwise operators
Bitwise operators treat arguments as 32-bit integer numbers and work on the level of their binary representation.

These operators are not JavaScript-specific. They are supported in most programming languages.

The list of operators:
-   AND ( `&` )
-   OR ( `|` )
-   XOR ( `^` )
-   NOT ( `~` )
-   LEFT SHIFT ( `<<` )
-   RIGHT SHIFT ( `>>` )
-   ZERO-FILL RIGHT SHIFT ( `>>>` ) 

These operators are used very rarely, when we need to fiddle with numbers on the very lowest (bitwise) level. We won’t need these operators any time soon, as web development has little use of them, but in some special areas, such as cryptography, they are useful. You can read the [Bitwise Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#bitwise_operators) chapter on MDN when a need arises.

### Comma
The comma operator `,` is one of the rarest and most unusual operators. Sometimes, it’s used to write shorter code, so we need to know it in order to understand what’s going on.

The comma operator allows us to evaluate several expressions, dividing them with a comma `,`. Each of them is evaluated but only the result of the last one is returned.

For example:
```js
let a = (1 + 2, 3 + 4);

alert( a ); // 7 (the result of 3 + 4)
```
```ad-caution

**Comma has a very low precedence**
Please note that the comma operator has very low precedence, lower than =, so parentheses are important in the example above.

Without them: a = 1 + 2, 3 + 4 evaluates + first, summing the numbers into a = 3, 7, then the assignment operator = assigns a = 3, and the rest is ignored. It’s like (a = 1 + 2), 3 + 4.
```

