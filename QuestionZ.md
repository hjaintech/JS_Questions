### Question
`1 + -"1" + "2"`
### Output: 
`"02"`
### Explanation
Based on order of operations, the first operation to be performed is `-"1"` (the extra `-` before the `"1"` is treated as a unary operator). 
Thus javascript converts `"1"` into `1`, which then becomes `-1` when the `-` is applied. It is then added to `1` yielding `0`, which is then converted to a string and concatenated with the final `"2"` operand, yielding `"02"`
