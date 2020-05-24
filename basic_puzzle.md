#### Problem

```js
"1, 2, 3" === "1, 2, 3"
[1, 2, 3] === [1, 2, 3]
```

#### Solution
```js
true
false
```

#### Explanation
JavaScript provides different data types to hold different types of values. These data types can be classified in below two `categories`
- <b>Primitive:</b> Primitive data types include `numbers`, `strings`, `booleans`, `null`, `undefined`
- <b>Non-primitive:</b> For example, `functions`, `objects` & `arrays`

One of the major difference between how Javascript treats these `categories` of data types is `equality check`.
- <b>Primitives</b> are compared by value i.e two values are strictly equal if they have the same value. 
- <b>Non primitive</b> values are compared by reference instead of value. So, two objects are only strictly equal if they refer to the same underlying object. This means that even if two non-primitives have the same properties and values, still they are not strictly equal.

Now coming back to the question, here as `"1, 2, 3"` is a string (primitive data type), it is compared by `value` and thus returns `true`. However, as `[1, 2, 3]` is an array (non-primitive data type), it is compared by reference and thus returns `false` because values at both ends of `===` are different references to arrays.
