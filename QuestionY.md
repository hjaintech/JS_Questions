### Question
`"A" - "B" + 2`
### Output: 
`"NaN2"`
### Explanation
Since the `-` operator can not be applied to strings, and since neither `"A"` nor `"B"` can be converted to numeric values, `"A" - "B"` jields `NaN`, which is then concatenated with the string `"2"` to yeild `"NaN2"`
