
# Similify

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![GitHub issues](https://img.shields.io/github/issues/Untoldhacker-Dev/similify.bb.svg)](https://github.com/Untoldhacker-Dev/similify.bb/issues)
[![GitHub stars](https://img.shields.io/github/stars/Untoldhacker-Dev/similify.bb.svg)](https://github.com/Untoldhacker-Dev/similify.bb/stargazers)
[![Telegram](https://img.shields.io/badge/chat-on%20telegram-0088cc.svg)](https://t.me/CubeTon)

Similify is a versatile JavaScript package designed to simplify and enhance similarity comparisons in various contexts. Whether you're comparing words, objects, arrays, or exploring string lengths and numerical ranges, Similify provides an easy-to-use interface with customizable thresholds. Effortlessly find the most similar instances and match percentages, making complex comparisons a breeze. Streamline your similarity analysis and unlock new possibilities with Similify.

## Intention 

> This version of Similify is Made for BB Bots only



## Usage

Require Similify in your Bot JavaScript code and start using its functions:

### Compare Words

```javascript
const { compareWords } = Libs.similify;

// Example usage with default threshold (70)
const result = compareWords("apple", "orange");
// Bot.inspect(result);
// Output: { mostSimilar: 'orange', matchPercentage: 71.43 }  
```

### Word to Object in Array Comparison

```javascript
const { wordToObjectArrayComparison } = Libs.similify;

const objectsArray = [{ name: "banana" }, { name: "orange" }];

const result = wordToObjectArrayComparison("apple", objectsArray, "name");
// Bot.inspect(result);
// Output: { mostSimilar: 'orange', matchPercentage: 71.43 }  
```

### Compare Objects

```javascript
const { compareObjects } = Libs.similify;

// Example usage with default threshold (70)
const result = compareObjects({ a: 1, b: 2 }, { a: 1, b: 3 });
// Bot.inspect(result);
// Output: { mostSimilar: '{"a":1,"b":2}', matchPercentage: 71.43 }  
```

### Compare Array Places

```javascript
const { compareArrayPlaces } = Libs.similify;

const array1 = ["apple", "banana"];
const array2 = ["orange", "banana"];

const result = compareArrayPlaces(array1, 0, array2, 1);
// Bot.inspect(result);
// Output: { mostSimilar: 'banana', matchPercentage: 71.43 }  
```

### Compare Word to Array

```javascript
const { compareWordToArray } = Libs.similify;

const word = "apple";
const array = ["orange", "banana", "grape"];

const result = compareWordToArray(word, array);
// Bot.inspect(result);
// Output: { mostSimilar: 'grape', matchPercentage: 57.14 }  
```

### Compare Arrays

```javascript
const { compareArrays } = Libs.similify;

const array1 = ["apple", "banana"];
const array2 = ["orange", "banana", "grape"];

const result = compareArrays(array1, array2);
// Bot.inspect(result);
// Output: { mostSimilar: ['banana'], matchPercentage: 66.67 }  
```

### Compare String Length

```javascript
const { compareStringLength } = Libs.similify;

const result = compareStringLength("apple", "orange");
// Bot.inspect(result);
// Output: { longerString: 'orange', lengthDifference: 1 }  
```

### Compare Number to Range

```javascript
const { compareNumberToRange } = Libs.similify;

const result = compareNumberToRange(25, 20, 30);
// Bot.inspect(result);
// Output: { withinRange: true, deviationFromMidpoint: 2.5 }  
```

## Below are explanations for each function provided by the Similify package:

### `compareWords(word1, word2, threshold = 70)`

This function compares two words, `word1` and `word2`, by calculating the similarity percentage based on letter matching. The default threshold is set to 70, and the function returns an object with the most similar word and the match percentage.

### `wordToObjectArrayComparison(word, objectArray, key, threshold = 70)`

This function compares a word to the values of a specified key within an array of objects (`objectArray`). It calculates the similarity percentage for each value and returns an object containing the most similar object instance and the corresponding match percentage.

### `compareObjects(obj1, obj2, threshold = 70)`

Compares two objects (`obj1` and `obj2`) by converting them to JSON strings and then calculating the similarity percentage based on letter matching. The default threshold is set to 70, and the function returns an object with the most similar object and the match percentage.

### `compareArrayPlaces(array1, index1, array2, index2, threshold = 70)`

Compares two elements at specified indices (`index1` and `index2`) within two arrays (`array1` and `array2`). It calculates the similarity percentage based on letter matching and returns an object with the most similar element and the match percentage. The default threshold is set to 70.

### `compareWordToArray(word, array, threshold = 70)`

Compares a word to each element in an array (`array`). It calculates the similarity percentage for each element and returns an object with the most similar element and the match percentage. The default threshold is set to 70.

### `compareArrays(array1, array2, threshold = 70)`

Compares each element in two arrays (`array1` and `array2`). It calculates the similarity percentage for each pair of elements and returns an object with the most similar elements and the match percentage. The default threshold is set to 70.

### `compareStringLength(str1, str2)`

Compares the lengths of two strings (`str1` and `str2`). It returns an object with the longer string and the absolute difference in length between the two strings.

### `compareNumberToRange(number, min, max)`

Checks if a number is within a specified range (`min` to `max`). It returns an object with a boolean indicating whether the number is within the range and the deviation of the number from the midpoint of the range.

These functions provide a variety of comparison functionalities, allowing users to find similarities in words, objects, arrays, string lengths, and numerical ranges. Users can also customize the threshold for similarity based on their specific requirements.


## Support

For support and discussions, join our Telegram channel: [CubeTon](https://t.me/CubeTon)

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
