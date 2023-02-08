## Arrays
Arrays is a ordered list value with single variable in javascript. 
```ad-tip

It is always recommended to declare arrays variable with `const`.
```
### Changing an Array Element
```js
const cars = ["Saab", "Volvo", "BMW"];
cars[0] = "Opel";
```
### Access the Full Array
You can also access the full aray with this command :
```js
const cars = ["Saab", "Volvo", "BMW"];
document.getElementById("demo").innerHTML = cars;
```
### Arrays are Objects
Arrays are a special type of objects. The `typeof` operator in JavaScript returns "object" for arrays. But, JavaScript arrays are best described as arrays. Arrays use **numbers** to access its "elements". In this example, `person[0]` returns John:
```js
const person = ["John", "Doe", 46];
```
Objects use **names** to access its "members". In this example, `person.firstName` returns John:
```js
const person = {firstName:"John", lastName:"Doe", age:46};
```

## JavaScript Array Methods
### Converting Arrays to Strings
The JavaScript method `toString()` converts an array to a string of (comma separated) array values.
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();
```
result:
```
Banana,Orange,Apple,Mango
```
The join() method also joins all array elements into a string.

It behaves just like toString(), but in addition you can specify the separator:
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.join(" * ");
```
result : 
```
Banana * Orange * Apple * Mango
```