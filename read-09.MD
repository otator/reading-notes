# Refactoring
code refactoring is rewriting a code that does the same as the code does. But more readable and less-code.

it is better to divide your code into separate files to make it readable. And import these files in the main file that will run.

```javascript
// Unrefactored code

const URLstore = [];

function makeShort(URL) {
  const rndName = Math.random().toString(36).substring(2);
  URLstore.push({[rndName]: URL});
  return rndName;


function getLong(shortURL) {
  for (let i = 0; i < URLstore.length; i++) {
    if (URLstore[i].hasOwnProperty(shortURL) !== false) {
      return URLstore[i][shortURL];
    }
  }
}
```

```javascript
// Refactored code

const URLstore = new Map(); // Change this to a Map

function makeShort(URL) {
  const rndName = Math.random().toString(36).substring(2);
  // Place the short URL into the Map as the key with the long URL as the value
  URLstore.set(rndName, URL);
  return rndName;
}

function getLong(shortURL) {
  // Leave the function early to avoid an unnecessary else statement
  if (URLstore.has(shortURL) === false) {
    throw 'Not in URLstore!';
  }
  return URLstore.get(shortURL); // Get the long URL out of the Map
}
```



### Functional Programming

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data. [wiki-link](https://en.wikipedia.org/wiki/Functional_programming)

**Pure Functions** are the functions that don't cause any observable side effects. they return the same result if given the same arguments.

```javascript
  // Impure function
  let PI = 3.14;

  function getArea(radius){
    return radius**2 * PI;
  }

  getArea(2);
```

the code above could return different data if the PI value changed with time by anyone.

so that the PI varibale must be passed as an argument for the function.

```javascript
  // pure function
  let PI = 3.14;

  function getArea(radius, PI){
    return radius**2 * PI;
  }

  getArea(2,PI);
```



