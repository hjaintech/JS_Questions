## What would be the output of below code snippet?

```js
var name = "Bob";
name[0] = 'T';
name[1] = 'o';
name[2] = 'm';

console.log(`${name} Smith`);

```


## Output: 
`Bob Smith`

## Explanation:

This happens because Strings are `immutable` in JavaScript. So you can't mutate the string value. the original value remains unchanged. So effectively `name[0] = 'T'` doesn't make any change, although it doesn't throw an error as well.

Note that below re-assignment works as expected.
`name = 'Tom'`
