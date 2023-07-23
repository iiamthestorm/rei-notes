## Built-in browser functions

We've used functions built in to the browser a lot in this course.

Every time we manipulated a text string, for example:
```js
const myText = 'I am a string';
const newString = myText.replace('string', 'sausage');
console.log(newString);
// the replace() string function takes a source string,
// and a target string and replaces the source string,
// with the target string, and returns the newly formed string
```
Or every time we manipulated an array:
```js
const myArray = ['I', 'love', 'chocolate', 'frogs'];
const madeAString = myArray.join(' ');
console.log(madeAString);
// the join() function takes an array, joins
// all the array items together into a single
// string, and returns this new string
```
Or every time we generate a random number:
```js
const myNumber = Math.random();
// the random() function generates a random number between
// 0 and up to but not including 1, and returns that number
```
We were using a _function_!

## Functions versus methods
Functions that are part of objetcs are called methods. 
## Optional Parameters
Some of the js built in function doesn't need parameter, but it is best practice if you want to produce a certain output with including a parameters. For example :
```js
const myArray = ['I', 'love', 'chocolate', 'frogs'];
const madeAString = myArray.join(' ');
console.log(madeAString);
// returns 'I love chocolate frogs'

const madeAnotherString = myArray.join();
console.log(madeAnotherString);
// returns 'I,love,chocolate,frogs'
```

## Anonymous functions and arrow functions
### Anonymous function
We can create our anonymous function like this :
```js
(function () {
	console.log('Hello!');
})
```
anonymous function can be created without specifying name. You'll often see anonymous functions when a function expects to receive another function as a parameter. In this case the function parameter is often passed as an anonymous function. 

For example, let's say you want to run some code when the user types into a text box. To do this you can call the [`addEventListener()`](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener "addEventListener()") function of the text box. This function expects you to pass it (at least) two parameters:

-   the name of the event to listen for, which in this case is [`keydown`](https://developer.mozilla.org/en-US/docs/Web/API/Element/keydown_event "keydown")
-   a function to run when the event happens.

When the user presses a key, the browser will call the function you provided, and will pass it a parameter containing information about this event, including the particular key that the user pressed:
```js
function logKey(event) {
  console.log(`You pressed "${event.key}".`);
}

textBox.addEventListener('keydown', logKey);
```
instead of defining a separater `logKey()` function, you can pass an anonymous function into `addEventListener()`:
```js
textBox.addEventListener('keydown', function(event) {
  console.log(`You pressed "${event.key}".`);
});
```
### Arrow function
We can create a simple version of anonymous function with arrow function.
```ad-important

Instead of `function(event)`, we can write `(event) =>`: 
```
```js
textBox.addEventListener('keydown', (event) => {
  console.log(`You pressed "${event.key}".`);
});
```
If the function only has one line in the curly brackets, we can omit the curly brackets:
```js
textBox.addEventListener('keydown', (event) => console.log(`You pressed "${event.key}".`));
```
If the function only takes one parameter, you can also omit the brackets around the parameter:
```js
textBox.addEventListener('keydown', event => console.log(`You pressed "${event.key}".`));
```
Finally, if your function needs to return a value, and contains only one line, you can also omit the `return` statement. In the following example we're using the [`map()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) method of `Array` to double every value in the original array:
```js
const originals = [1, 2, 3];

const doubled = originals.map(item => item * 2);

console.log(doubled); // [2, 4, 6]
```
`map` method takes each item in the array in turn, passing it into the given function. It then takes the value returned by that function and adds it to a new array.

so in the example above you can see that `(item) => item * 2` is the arrow function equivalent of :
```js
function doubleItem(item) {
	return item * 2;
}
```
I think arrow function is great for readable code and make it shorter.
