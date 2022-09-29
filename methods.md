<h1>String Methods Review</h1>

- **charAt**
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
- **charCodeAt**
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
- **concat**
  - Joins two strings together.
```
const str1 = 'Hello';
const str2 = 'World';

console.log(str1.concat(' ', str2));
// expected output: "Hello World"

console.log(str2.concat(', ', str1));
// expected output: "World, Hello"
```

```
let text1 = "sea";
let text2 = "food";
let result = text1.concat(text2);

// expected output: seafood
```
- **includes**
  - Returns `true` if a string contains a specified string. Otherwise, returns `false`.
  - This method is case sensitive.
```
const sentence = 'The quick brown fox jumps over the lazy dog.';

const word = 'fox';

console.log(`The word "${word}" ${sentence.includes(word) ? 'is' : 'is not'} in the sentence`);
// expected output: "The word "fox" is in the sentence"
```

```
let text = "Hello world, welcome to the universe.";
let result = text.includes("world");

// expected output: true
```
- **indexOf**
- **match**
- **repeat**
- **replace**
- **search**
- **slice**
- **split**
- **substr**
- **toLowerCase**
- **toUpperCase**
- **trim**
