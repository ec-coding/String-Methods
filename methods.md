<h1>String Methods Review</h1>

1. charAt
  - Returns a new string consisting of the character located at the specified `index`. If the `index` is out of range, `charAt()` returns an empty string.

- Examples:
```
const sentence = 'The quick brown fox jumps over the lazy dog.';

const index = 4;

console.log(`The character at index ${index} is ${sentence.charAt(index)}`);
// expected output: "The character at index 4 is q"
```


charCodeAt
concat
includes
indexOf
match
repeat
replace
search
slice
split
substr
toLowerCase
toUpperCase
trim
