<h1>String Methods Review</h1>

- **.charAt()**
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
- **.charCodeAt()**
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
- **.concat()**
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
- **.includes()**
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
- **.indexOf()**
  - Returns the position (via index) of the first occurence of a value in a string.
  - Each space is also counted.
  - Returns -1 if the value is not found.
  - This method is case sensitive.
```
const paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';

const searchTerm = 'dog';
const indexOfFirst = paragraph.indexOf(searchTerm);

console.log(`The index of the first "${searchTerm}" from the beginning is ${indexOfFirst}`);
// expected output: "The index of the first "dog" from the beginning is 40"

console.log(`The index of the 2nd "${searchTerm}" is ${paragraph.indexOf(searchTerm, (indexOfFirst + 1))}`);
// expected output: "The index of the 2nd "dog" is 52"
```

```
let text = "Hello world, welcome to the universe.";
let result = text.indexOf("welcome");

document.getElementById("demo").innerHTML = result;

// expected output: 13
```

```
let text = "Hello world, welcome to the universe.";
document.getElementById("demo").innerHTML = text.indexOf("e", 5);;

// find "e", starting at index 5:
// expected output: 14
```
- **.match()**
  - Matches a string against a regular expression and returns an array with said matches.
  - Returns `null` if no match is found.
```
const paragraph = 'The quick brown fox jumps over the lazy dog. It barked.';
const regex = /[A-Z]/g;
const found = paragraph.match(regex);

console.log(found);
// expected output: Array ["T", "I"]
```

```
let text = "The rain in SPAIN stays mainly in the plain";
let result = text.match("ain");
 
document.getElementById("demo").innerHTML = result;

// expected output: ain
```

```
let text = "The rain in SPAIN stays mainly in the plain";
let result = text.match(/ain/gi);

document.getElementById("demo").innerHTML = result;

// gi initiates a global, case-insensitive search
// expected output: ain,AIN,ain,ain
```
- **.repeat()**
- **.replace()**
- **.search()**
- **.slice()**
- **.split()**
- **.substr()**
- **.toLowerCase()**
- **.toUpperCase()**
- **.trim()**
