# Number Words to Numeric Converter

This Python script converts numbers written in words (e.g., "one hundred twenty-three") into their numeric equivalent and formats the result using the Indian Numbering System (e.g., `1,23,45,678`).

## Features

- Converts numbers written in words into numeric format.
- Handles Indian numbering conventions (e.g., lakh, crore).
- Formats output using the Indian Numbering System (e.g., `1,23,456`).
- Supports numbers written in English with words like "hundred," "thousand," "lakh," and "crore."

## Requirements

- Python 3.6+
- `babel` library for formatting numbers in the Indian Numbering System.

## Installation

1. Install Python 3 if not already installed.
2. Install the required library using pip:
   ```bash
   pip install babel
   ```

## Usage

1. Run the script.
2. Input a number in words (e.g., `"one hundred twenty-three"`).
3. View the output in numeric format with Indian-style formatting.

### Example Usage

Input:

```plaintext
Enter a number in words: one lakh twenty-three thousand four hundred fifty-six
```

Output:

```plaintext
1,23,456
```

### Code Breakdown

The script uses dictionaries to map words to their numeric equivalents:

- `unitDIG`: Maps single digits (e.g., "one" -> 1).
- `teenDIG`: Maps numbers from 10 to 19.
- `tens`: Maps multiples of 10 (e.g., "twenty" -> 20).
- `multipliers`: Maps large number multipliers (e.g., "thousand," "lakh," "crore").

It processes the input word by word to compute the numeric value and formats the result using the `format_decimal` function from the `babel` library.

### Example Inputs and Outputs

| Input                                                            | Output        |
| ---------------------------------------------------------------- | ------------- |
| `one hundred twenty-three`                                       | `123`         |
| `twelve thousand three hundred forty-five`                       | `12,345`      |
| `one lakh twenty-three thousand four hundred fifty-six`          | `1,23,456`    |
| `two crore fifty lakh seventy-six thousand eight hundred ninety` | `2,50,76,890` |

## Notes

- The script supports numbers written in English only.
- Ensure input words are in lowercase and separated by spaces.
- Invalid words will terminate the script with an error message.

## Future Improvements

- Add support for decimal numbers in words (e.g., "point five" -> `0.5`).
- Extend support to other languages.

## License

This script is open-source and free to use under the MIT License.

## Author

Aaditya Paul

