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

// expected output: "D"
```
---
- **.charCodeAt()**
  - Returns an integer between `0` and `65535` representing the Unicode of the character at a specified position in a string.

  - Examples:
```
'ABC'.charCodeAt(0) 

// expected output: 65
```

```
let text = "HELLO WORLD";
let code = text.charCodeAt(0);

// expected output: 72
```
---
- **.concat()**
  - Joins two strings together.

  - Examples:
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

// expected output: "seafood"
```
---
- **.includes()**
  - Returns `true` if a string contains a specified string. Otherwise, returns `false`.
  - This method is case sensitive.

  - Examples:
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
---
- **.indexOf()**
  - Returns the position (via index) of the first occurence of a value in a string.
  - Each space is also counted.
  - Returns -1 if the value is not found.
  - This method is case sensitive.

  - Examples:
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
---
- **.match()**
  - Matches a string against a regular expression and returns an array with said matches.
  - Returns `null` if no match is found.

  - Examples:
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

// expected output: ["ain"]
```

```
let text = "The rain in SPAIN stays mainly in the plain";
let result = text.match(/ain/gi);

document.getElementById("demo").innerHTML = result;

// gi initiates a global, case-insensitive search
// expected output: ["ain,AIN,ain,ain"]
```
---
- **.repeat()**
  - Constructs and returns a new string which contains the specified number of copies of the string on which it was called, concatenated together.
  - Does not mutate the original string.

  - Examples:
```
const chorus = 'Because I\'m happy. ';

console.log(`Chorus lyrics for "Happy": ${chorus.repeat(3)}`);

// expected output: "Chorus lyrics for "Happy": Because I'm happy. Because I'm happy. Because I'm happy."
```

```
let text = "Hello world!";
let result = text.repeat(2);

document.getElementById("demo").innerHTML = result;
// expected output: "Hello world!Hello world!"
```
---
- **.replace()**
  - Searches for a string for a value or a regular exprssion, then returns a new string with said value(s) replaced.
  - Does not mutate the original string.

  - Examples:
```
const p = 'The quick brown fox jumps over the lazy dog. If the dog reacted, was it really lazy?';

console.log(p.replace('dog', 'monkey'));
// expected output: "The quick brown fox jumps over the lazy monkey. If the dog reacted, was it really lazy?"
```

```
let str = document.getElementById("demo").innerHTML; 
let res = str.replace(/blue/g, "red");
document.getElementById("demo").innerHTML = res;

// expected output: "Mr Blue has a red house and a red car."
```
---
- **.search()**
  - Matches a string against a regular expression and returns the index of the first match.
  - Returns -1 if no match is found.
  - This method is case sensitive.

  - Examples:
```
const paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';

// any character that is not a word character or whitespace
const regex = /[^\w\s]/g;

console.log(paragraph.search(regex));
// expected output: 43
```

```
let text = "Mr. Blue has a blue house"
let position = text.search("Blue");

document.getElementById("demo").innerHTML = position;
// expected output: 4
```
---
- **.slice()**
  - Extracts a section of a string and returns it as a new string, without modifying the original string.

  - Examples:
```
const str = 'The quick brown fox jumps over the lazy dog.';

console.log(str.slice(31));
// expected output: "the lazy dog."

console.log(str.slice(4, 19));
// expected output: "quick brown fox"

console.log(str.slice(-4));
// expected output: "dog."

console.log(str.slice(-9, -5));
// expected output: "lazy"
```

```
// Slice the first 5 positions:
let text = "Hello world!";
let result = text.slice(0, 5);

document.getElementById("demo").innerHTML = result;
// expected output: "Hello"
```

```
// From position 3 to the end:
let text = "Hello world!"; 
let result = text.slice(3);

document.getElementById("demo").innerHTML = result;
// expected output: "lo world!"
```
---
- **.split()**
  - Splits a string into an array of substrings and returns the new array.
  - Does not mutate the original string.
  - If (" ") is used as a separator, the string is split between words.

  - Examples:
```
const str = 'The quick brown fox jumps over the lazy dog.';

const words = str.split(' ');
console.log(words[3]);
// expected output: "fox"
```

```
let text = "How are you doing today?";
const myArray = text.split("");

document.getElementById("demo").innerHTML = myArray;
// expected output: "H,o,w, ,a,r,e, ,y,o,u, ,d,o,i,n,g, ,t,o,d,a,y,?"
```

```
let text = "How are you doing today?";
const myArray = text.split(" ", 3);

document.getElementById("demo").innerHTML = myArray;
// expected output: "How,are,you"
```
---
- **.substr()**
  - Extracts a part of a string, beginning at a specified position, and returns a specified number of characters.
  - Does not mutate the original string.
  - To extract characters from the end of a string, use a negative start position.
  - This is a deprecated method (no longer recommended).

  - Examples:
```
const str = 'Mozilla';

console.log(str.substr(1, 2));
// expected output: "oz"

console.log(str.substr(2));
// expected output: "zilla"
```

```
let text = "Hello world!";
let result = text.substr(1, 4);

document.getElementById("demo").innerHTML = result;
// expected output: "ello"
```
---
- **.toLowerCase()**
  - Converts a string to lowercase letters.
  - Does not mutate the original string.

  - Examples:
```
const sentence = 'The quick brown fox jumps over the lazy dog.';

console.log(sentence.toLowerCase());
// expected output: "the quick brown fox jumps over the lazy dog."
```

```
let text = "Hello World!";
let result = text.toLowerCase();

document.getElementById("demo").innerHTML = result;
// expected output: "hello world!"
```
---
- **.toUpperCase()**
  - Converts a string to uppercase letters.
  - Does not mutate the original string.

  - Examples:
```
const sentence = 'The quick brown fox jumps over the lazy dog.';

console.log(sentence.toUpperCase());
// expected output: "THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG."
```

```
let text = "Hello World!";
let result = text.toUpperCase();

document.getElementById("demo").innerHTML = result;
// expected output: "HELLO WORLD!"
```
---
- **.trim()**
  - Removes whitespace from both sides of a string.
  - Does not mutate the original string.

  - Examples:
```
const greeting = '   Hello world!   ';

console.log(greeting);
// expected output: "   Hello world!   ";

console.log(greeting.trim());
// expected output: "Hello world!";
```

```
let text = "     Hello World!     ";
let result = text.trim();

document.getElementById("demo2").innerHTML = result;
// expected result: "Hello World!
```
