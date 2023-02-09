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
### Popping and Pushing
When you work with arrays, it is easy to remove elements and add new elements. This is what popping and pushing is:
```ad-important

Popping items **out** of an array, or pushing items **into** an array.
```
#### JavaScript Array pop()
The `pop()` method removes the last element from an array:
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.pop();
```
The `pop()` method returns the value that was "popped out":
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits.pop();
```
#### JavaScript Array push()
The `push()` method adds a new element to an array (at the end):
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Kiwi");
```
The `push()` method returns the new array length:
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let length = fruits.push("Kiwi");
```
### Shifting Elements
Shifting is equivalent to popping, but working on the first element instead of the last.
#### JavaScript Array shift()
The `shift()` method removes the first array element and "shifts" all other elements to a lower index.
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.shift();
```
#### JavaScript Array unshift()
The `unshift()` method adds a new element to an array (at the beginning), and "unshifts" older elements:
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];  
fruits.unshift("Lemon");
```
### Merging (Concatenating) Arrays
The `concat()` method creates a new array by merging (concatenating) existing arrays:
```js
const myGirls = ["Cecilie", "Lone"];
const myBoys = ["Emil", "Tobias", "Linus"];

const myChildren = myGirls.concat(myBoys);
```
```ad-important

The `concat()` method does not change the existing arrays. It always returns a new array.
```
The `concat()` method can take any number of array arguments:
```js
const arr1 = ["Cecilie", "Lone"];
const arr2 = ["Emil", "Tobias", "Linus"];
const arr3 = ["Robin", "Morgan"];
const myChildren = arr1.concat(arr2, arr3);
```
The `concat()` method can also take strings as arguments:
```js
const arr1 = ["Emil", "Tobias", "Linus"];  
const myChildren = arr1.concat("Peter");
```
### Splicing and Slicing Arrays
The `splice()` method adds new items to an array.
The `slice()` method slices out a piece of an array.
#### JavaScript Array splice()
The `splice()` method can be used to add new items to an array:
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];  
fruits.splice(2, 0, "Lemon", "Kiwi");
```
```ad-important

The first parameter (2) defines the position **where** new elements should be **added** (spliced in).
The second parameter (0) defines **how many** elements should be **removed**.
The rest of the parameters ("Lemon" , "Kiwi") define the new elements to be **added**.
```
#### Using splice() to Remove Elements
With clever parameter setting, you can use `splice()` to remove elements without leaving "holes" in the array:
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];  
fruits.splice(0, 1);
```
```ad-important

The first parameter (0) defines the position where new elements should be **added** (spliced in).

The second parameter (1) defines **how many** elements should be **removed**.

The rest of the parameters are omitted. No new elements will be added.
```
#### JavaScript Array slice()
The `slice()` method slices out a piece of an array into a new array.

This example slices out a part of an array starting from array element 1 ("Orange"):
```js
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];  
const citrus = fruits.slice(1);
```
```ad-important

The `slice()` method creates a new array.

The `slice()` method does not remove any elements from the source array.
```
This example slices out a part of an array starting from array element 3 ("Apple"):
```js
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(3);
```
The `slice()` method can take two arguments like `slice(1, 3)`.
The method then selects elements from the start argument, and up to (but not including) the end argument.
```js
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];  
const citrus = fruits.slice(1, 3);
```
If the end argument is omitted, like in the first examples, the `slice()` method slices out the rest of the array.
```js
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];  
const citrus = fruits.slice(2);
```
### Automatic toString()
JavaScript automatically converts an array to a comma separated string when a primitive value is expected. This is always the case when you try to output an array. These two examples will produce the same result:
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();
```
```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits;
```
```ad-important

All JavaScript objects have a toString() method.

```


## Loops
### The for ... of loop
The basic tool for looping through a collection is the [`for...of`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of) loop:
```js
const cats = ['Leopard', 'Serval', 'Jaguar', 'Tiger', 'Caracal', 'Lion'];

for (const cat of cats) {
  console.log(cat);
}
```
In this example, `for (const cat of cats)` says:
1.  Given the collection `cats`, get the first item in the collection.
2.  Assign it to the variable `cat` and then run the code between the curly brackets `{}`.
3.  Get the next item, and repeat (2) until you've reached the end of the collection.
### map() and filter() 


