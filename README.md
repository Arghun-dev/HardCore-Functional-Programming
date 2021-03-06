# HardCore-Functional-Programming

**Every Function is a single valued collection of pairs**

## Functions (Same Input Same Output => Pure Functions)

1. Total => For every input there is a corresponding output
2. Deterministic => Always receive the same output for a given input
3. No-observable Side Effects => No observable effects besides computing a value


is this a function or not?

```js
const headerText = header_selector => querySelector(header_selector).text();
```

**actually this is not a function, because this function is going to go out into the world, and try to find a text, and the text could change any time, so it's not giving me the same output, if I give it the same input**

## Pure Functions Advantages

1. Reliable => returns same output for the same input
2. Portable => They're not stuck in their environment
3. Reusable
4. Testable
5. Composable
6. Properties/Contract

## Properties, Arguments & Currying

**Properties**

let's see `add` and `multiply` you know they hold properties:

// associative
```js
add(add(x, y), z) === add(x, add(y, z));
```

// commutative => we can switch the arguments
```js
add(x, y) === add(y, x);
```

## Currying

```js
const add = (x, y) => x + y;

const curry = f => x => y => f(x, y);

const curriedAdd = curry(add);

const increment = curriedAdd(1);

const result = increment(2);
```

So what curryied did was allow me to give Add. But I can give it a function or an argument and it remembers it.

So then it's just waiting for it's `y`, it remembers it's `x`
