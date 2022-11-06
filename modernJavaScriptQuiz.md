## 1. What is the difference between variables declared with var, let and const?
**Ans:** *var - variable is scoped to the function where it was declared
     let - variable is scoped to the closest brackets and CAN be redefined
     const - variable is scoped to the closest brackets and CAN NOT be redefined*

**Explanation:** When a variable declared with 'var' keyword, the variable becomes available in the scope of the function where it was declared.
If you try and access it outside of the function, it will be undefined and you will receive reference error. If declared outside of a function,
then it becomes a global variable.
When a variable is declared with 'let' keyword, the variable is available only in the enclosing brackets. This type of variable can be reassigned/redefined any time.
When a variable is declared with 'const', it behaves exactly like 'let', but it can't be reassigned/redefined.

## 2. Why string interpolation is useful?
**Ans:** *It allows to easily concatenate multiple strings (avoiding the "+" operator) and insert values "in place as they are"*

**Explanation:** string interpolation simplifies string concatenation and insertion of javascript expression somewhere inside the string. It also makes string more readable because of the syntax.

## 3. What is array/object destructuring?
**Ans:** Destructuring allows to pull some value from an object/array with single line of code.

**Explanation** Array/object destructuring allows to efficiently pull some key/value from the array/object avoiding writing redunant lines of code.

## 4. What is the difference between destructuring and rest operator?
**Ans:** *Destructuring pulls value from an object/array. Rest operator puts "the rest" of values into an array.*

**Explanation** Destructuring pulls value out of an array or object while rest operator puts the rest of undestructured/rest values into a single array.

## 5. How .map or .reduce array methods can be helpful?
**Ans:** *Both allow to loop/iterate over an array. .map will produce a new array with mapped values. .reduce will produce a single accumulated value from the existing array elements (e.g. sum of all elements).*

**Explanation** .map and .reduce methods both allow loop over an array and both produce a new value. The .map method maps every value of the existing array to some other, new value and produces a new array. The .reduce method accumulates a value over its iterations and eventually returns the accumulated value as a result.

## 6. How may states a Promise can have?
**Ans:** *Three*

**Explanation** Promise has 3 states: Pending, Resolved, Rejected. When resolved or rejected Promise becomes settled.

## 7. Is async code somehow different from sync code?
**Ans:** *Yes. All async code always executed after all sync code is finished.*

**Explanation** Yes, async and sync are different. Async code is non-blocking and always executed after all sync code. Sync code is always executed before async code.