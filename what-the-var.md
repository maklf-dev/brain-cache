# JavaScript : Vol 0

> for now, just some **Random Facts** !

## Global

- type og `null`
```js
console.log(typeof null); // object 😬 historical bug
```
- to check type of array
```js
Array.isArray([]); // true
```
- NaN means *Not a Number*, and also the type of it is `number` !
```js
typeof NaN; // number ✌️
```
- falsy values : `false`, `0`, `""`, `null`, `undefined`, `NaN`; all the rest values including `{}` , `[]` are truthy


## Functions

### Notes
- in functions, `console.log` is for checking, and `return` is for building reusable logic.

- if the condition ends the function, return immediately.
```js
function getCheckoutMessage(cart) {
  if (!cart.userLoggedIn) {
    return "Please log in first";
  }

  if (cart.items.length === 0) {
    return "Your cart is empty";
  }

  if (cart.total <= 0) {
    return "Invalid cart total";
  }

  return "Ready to checkout";
}
```

### Function Types
```js
//declaration
function name(parameters){
    //codes
    return //result
}

//expression
const variable = function(parameters){
    //codes
    return //this result saves in variable
}

//Arrow
const variable = (parameters) => {
    //codes
    return //this also result saves in variable
}

//One line arrow
const variable = (parameters) => //code; //this acts like return and save result of //code in variable
```
**Note:** Arrow functions handle `this` differently.

### Function Debugging Checklist

1. Did I call the function?
2. Did I pass the correct arguments?
3. Are the argument types correct?
4. Did the function return a value?
5. Am I using the returned value?
6. Is the function changing outside data unexpectedly?
7. Is the function doing too many jobs?