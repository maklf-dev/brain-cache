# JavaScript : Vol 0

> for now, just some **Random Facts** !

## Global

- type of `null`
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

## Scope

### Subjects

- **Scope** : Where a variable can be accessed from.
- **Global Scope** : Placed in the root. a variable inside it can be accessed almost everywhere.
- **Function Scope** : Variables created inside a function are only available inside that function.
- **Block Scope** : A block is usually created with `{ }`.
- **Lexical Scope** : Inner functions can access variables from their outer functions.
```js
function createPriceCalculator(taxPercent) {
  function calculate(price) {
    return price + (price * taxPercent / 100);
  }

  return calculate;
}

const addTax = createPriceCalculator(20);

console.log(addTax(100));
```
- **Hoisting** : JavaScript processes declarations before running the code. But different declarations behave differently.
- **Accidental Global Variable** : when you create a function and do not declare it. its available everywhere which make it risky, because any other code can overwrite it. 
- **var vs let/const** :

| name | canBeChanged | accessOnlyInScope |
| --- | --- | --- |
| const | false | true |
| let | true | true |
| var | true | false |

### Notes
- Variables should live in the smallest place where they are needed. **Small scope = safer code.**
- Use const by default. | Use let when the value must change. | Avoid var.
- in `const`, the variable is not *deeply frozen*:
```js
const product = {
  title: "Gold Ring",
  price: 450
};

product.price = 500; //Valid
product = {}; //Invalid
```
- from **inside** a scope you **can** access outside, but from **outside** you **can not** access inside a scope.
- some hoisting rules:
  1. Function declarations are fully hoisted
  2. `var` declarations are hoisted, but assigned `undefined`
  3. `let` and `const` are hoisted, but not usable before declaration
  4. Function expressions follow variable rules
  5. Arrow functions also follow variable rule