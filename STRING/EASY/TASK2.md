
# Task 2: Capitalize Name Strings

## Problem Statement
You are given a string containing words separated by spaces. Your task is to ensure that:
- The first letter of each alphabetic word is capitalized.
- Words that start with numbers or non-alphabetic characters should remain unchanged
- 
## Explanation
1. Words starting with an alphabetic character will have their first letter capitalized, and the rest of the word remains the same.
2. Words starting with a numeric or non-alphabetic character remain unchanged.
3. Spaces between words are preserved.

### Example Walkthrough
**Input:**
`vinay raykar 12abc john doe 2abc`
- "vinay" becomes "Vinay" (alphabetic word).
- "raykar" becomes "Raykar" (alphabetic word).
- "12abc" remains unchanged (starts with a number).
- "john" becomes "John" (alphabetic word).
- "doe" becomes "Doe" (alphabetic word).
- "2abc" remains unchanged (starts with a number).

**Output:**
`Vinay Raykar 12abc John Doe 2abc`

---

## Constraints
- The string contains alphanumeric characters and spaces only.
- There will be no punctuation marks in the string.
- The string length will be at most 100 characters.

---

## Solution

### Function Definition
The solution is implemented in Python as follows:

```python
def capitalize_name(name):
    # Split the input string into individual words
    words = name.split()
    
    # Iterate through each word
    for i in range(len(words)):
        # Check if the word starts with an alphabetic character
        if words[i][0].isalpha():
            # Capitalize the first letter of the word
            words[i] = words[i].capitalize()
    
    # Join the words back into a single string and return
    return " ".join(words)

# Input: Read the string from the user
name = input("Enter the string: ")

# Output: Display the result
print(capitalize_name(name))

