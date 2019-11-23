# Deep JavaScript Foundation Notes

*Necessay notes while watching and practicing JavaScript from Kyle Simpson's JavaScript Foundation Course* 



- *Everything is objct in JavaScript* is **wrong**. There are seven primitive types:
    - Undefined
    - NULL
    - Boolean
    - Number
    - String
    - Object
    - Symbol
- JavaScript refers `function` as a subtype of a `object` type
- `Array` can be referred to as subtype of `object` type
- `BigInt` is a built-in object used to represent numbers grater than 2^53 - 1 ([MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt))
- Unlike C++/Java etc. In JavaScript, variables don't have types, values do. 
- `typeof` always returns a `string`

> Why `typeof null` returns an `object` instead of `null`?
- From ES1, if you want to unset an object a regular valua, like a number you would use `undefined` but if you want to unset an objct, you would use `null`, that is the historical part why `typeof null` returns an `object`, which a **BUG** of JavaScript language design

- Consider the scenario:
```javascript
    var f = function(){};
    typeof f // "function"

    var arr = [1, 2, 3];
    typeof arr // "object"
``` 
which is also historical thing (bug)

- Undefined vs Undeclared vs Uninitialized (aka TDZ (Temporal Dead Zone)) 
    - Undefined: We can have have variable that's been initilized that is undefined 
    - Undeclared: We can have a variable that has been never even created which is undeclared.
    - Uninitialized: We can have a variable that's never been initialized