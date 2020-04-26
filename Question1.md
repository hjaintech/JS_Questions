
# Given a sentence, convert each word in the sentence to capital case

Given a sentence, convert each word in sentence into capital case. A word is in capital case when first character of word is in upper case and rest of letters are in lower case. 

## Example
> ### Input
> india is a beautiFul country
> ### Output
> India Is A Beautiful Country
> ### Explanation
> The input sentence has 5 words. In the output, each word has it's first character in upper case and all other characters in lower case.

## Approach
Let us try to understand the approach and soution in a step wise manner.
- The problem statement says that we have to make modifications on each word in the sentence. So, think about a way to break the sentence into words. In Javascript, we can split any string into substrings using `String.prototype.split()` method. It accepts a `separator` as an argument. In our case we can do this as
```js
const sentence = "india is a beautiFul country";
const words = sentence.split(' ');
console.log(words); // ["india", "is", "a", "beautiFul", "country"]
```
- Once we have individual `words` to work on, we can now think how to make first letter of word as capital case and rest as small case. So again we will have to split the individual word into two parts. 
  - First Character
  - Remaining Characters
  
  For this we can use `destructuring` in Javascript as below
```js
const word = "india";
const [firstChar, ...restChars] = word;
console.log(firstChar); // i
console.log(restChars); // ['n', 'd', 'i', 'a']
```
- Now that we have first character, we can capitalise it using `Array.prototype.toUpperCase()` method as shown below
```js
const char = 'a';
console.log(char.toUpperCase()) // A
```
- Now the we have rest of the word in a array of string format. For example, `['n', 'd', 'i', 'a']`.  So we have to perform two steps now.
  - Join the character array to form a string. This can be done using `Array.prototype.join()`
  -    Convert the string into lower case. This can be done using `String.prototype.toLowerCase()` method
 
  Below are code snippets for the same.
```js
const charArray = ['n', 'd', 'i', 'a'];
const charString = charArray.join('');
console.log(charString); // 'ndia'
```

```js
const string = "HELLO";
const stringInLowerCase = string.toLowerCase();
console.log(stringInLowerCase) // "hello"
```
- Finally we can join the words using a simple `+` operator as below
```js
const firstChar = "I";
const restString = "ndia";
const completeString = firstChar + restString;
console.log(completeString) // India
```

## Complete Code Implementation
```js
const convertToSentenceCase = (string) => {
	// Split the sentence into words
	const words = string.split(' ');
	
	// Iterate over the words
	for(let i = 0 ; i < words.length; i ++){
		// Split the word into 'firstChar' and 'restChars'
		let [firstChar, ...restChars] = words[i];
		
		// Converting first character into captial case
		firstChar = firstChar.toUpperCase();
		
		// Joining the character array and then converting them into lower case
		restChars = restChars.join('').toLowerCase();
		
		// finally join the word
		words[i] = firstChar + restChars;
	}
	// Finally join the words with a space in between and return the sentence in capital case
	return words.join(' ');
}

// Driver code
const sentenceInCapitalCase = convertToSentenceCase("india is a beautiFul country");
console.log(sentenceInCapitalCase); // India Is A Beautiful Country
```
