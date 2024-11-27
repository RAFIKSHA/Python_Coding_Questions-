# Task 3: Reverse the Order of Words in a String

## Problem Statement
Write a program that accepts a string and reverses the order of its words. The characters within each word must remain unchanged.

### Input:
	• A string `s` containing words separated by spaces.
	• The string will not contain leading or trailing spaces, and words are separated by a single space.

### Output:
	• A string with the order of words reversed, while maintaining the original order of characters within each word.

### Constraints:
	• The string length will not exceed 1000 characters.
	• Each word will consist of only alphanumeric characters.

### Examples:

Example 1:

Input:
"hello world"

Output:
world hello

Example 2:

Input:
Python is awesome

Output:
awesome is Python

Example 3:

Input:
I love programming

Output:
programming love I

## Solution

```python
def reverse_words(s):
    words = s.split()                # Split the string into words
    reversed_words = words[::-1]     # Reverse the list of words
    return " ".join(reversed_words)  # Join the reversed words into a string

# Read input string from the user
s = input()

# Output: Display the reversed order of words
print(reverse_words(s))

