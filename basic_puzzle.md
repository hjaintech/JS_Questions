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
- Primitive: Primitive data types include `numbers`, `strings`, `booleans`, `null`, `undefined`
- Non-primitive: For example, `functions`, `objects` & `arrays`

One of the major difference between how Javascript treats these `categories` of data types is `equality check`.
- Primitives are compared by value i.e two values are strictly equal if they have the same value. 
- Non primitive values are compared by reference instead of value. So, two objects are only strictly equal if they refer to the same underlying object. This means that even if two non-primitives have the same properties and values, still they are not strictly equal.
