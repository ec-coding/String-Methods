<h1>String Methods Review</h1>

- charAt
  - Returns a new string consisting of the character located at the specified `index`. If the `index` is out of range, `charAt()` returns an empty string.

  - Examples:
```
const sentence = 'The quick brown fox jumps over the lazy dog.';

const index = 4;

console.log(`The character at index ${index} is ${sentence.charAt(index)}`);
// expected output: "The character at index 4 is q"
```

```
let text = "HELLO WORLD";
let letter = text.charAt(text.length-1);

document.getElementById("demo").innerHTML = letter;

// expected output: D
```
- charCodeAt
  - Returns an integer between `0` and `65535` representing the Unicode of the character at a specified position in a string.
```
'ABC'.charCodeAt(0) 

// expected output: 65
```

```
let text = "HELLO WORLD";
let code = text.charCodeAt(0);

// expected output: 72
```
- concat
- includes
- indexOf
- match
- repeat
- replace
- search
- slice
- split
- substr
- toLowerCase
- toUpperCase
- trim
