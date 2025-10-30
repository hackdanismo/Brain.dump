# JavaScript

+ [Functions](#functions)
    + [Parameters](#parameters)
+ [Loops](#loops)

## Functions
A `function` is a reusable code block. In `JavaScript` a function is defined using the `function` keyword.

```javascript
function foo() {
    // Code to be executed is here
}

// Call the function to execute the code
foo();


// An example:
function add(a, b) {
    return a + b;
}
```

Using the modern syntax of `arrow functions` that were introduced in `ES6 (ECMAScript 2015)`:

```javascript
const foo = () => {
    // Code to be executed is here
}

// Call the function to execute the code
foo();


// An example:
const add = (a, b) => {
    return a + b;
}

// An example (shorthand, no return keyword):
const add = (a, b) => a + b;
```

### Parameters
Functions can contain `parameters` that act like variables inside the function. This allows `arguments` as values to be passed into the function when called. In this example, parameters `a` and `b` have been created. When the function is called, we can pass two `arguments` into these `parameters`. The function will then return the total of these two values.

```javascript
const add = (a, b) => a + b;

// Call the function to get the return the total of 2 and 4 = 6.
add(2, 4);
```

Default values can be added to the `parameters` so if no values are passed as `arguments`, the function will still return a value.

```javascript
const add = (a = 10, b = 2) => a + b;

// Call the function to get the return the total of 10 and 2 = 12.
add();
```

## Loops
A `loop` can be used to output data from an `array`. Here is the traditional way to loop over an array using a `for loop`:

```javascript
// Array containing a number of URLs for the Frontify website.
const urls = [
    "https://www.frontify.com/en/",
    "https://www.frontify.com/en/pricing",
    "https://www.frontify.com/en/request-demo",
]

// Using a for loop to loop over each of the URLs in the array.
for (let i = 0; i < urls.length; i++) {
    console.log(urls[i]);
}
```

Since `ES6 (ECMAScript 2015)`, the loop can be reduced to the newer, and simpler, shorthand syntax:

```javascript
// Array containing a number of URLs for the Frontify website.
const urls = [
    "https://www.frontify.com/en/",
    "https://www.frontify.com/en/pricing",
    "https://www.frontify.com/en/request-demo",
]

// Using a for loop to loop over each of the URLs in the array.
for (const i of urls) {
    console.log(i);
}
```
