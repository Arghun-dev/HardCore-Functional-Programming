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
