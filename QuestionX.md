### Question
`(0.1 + 0.2 == 0.3)`
### Output: 
`false`
### Explanation
This happens because the computer works on `Base 2` while decimal is `Base 10` which causes precision errors when doing decimal calculations.
```js
0.1 + 0.2 // 0.30000000000000004
```
A simple solution to fix this is
```js
Number((0.1 + 0.2).toFixed(2)) === 0.3 
```
Here, the numbers are added together, returning the floating number. Then precision is set to 2 decimal digits using `toFixed` which gives a string "0.3". Finally the `Number()` function casts the string back to a valid Number.
