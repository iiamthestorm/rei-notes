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
Arrays are a special type of objects. The `typeof` operator in JavaScript returns "object" for arrays. 