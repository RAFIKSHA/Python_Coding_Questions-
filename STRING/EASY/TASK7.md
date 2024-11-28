### Task: Check if a Given String is a Palindrome

#### Problem Statement:  
Write a program that checks if a given string is a palindrome. The program should ignore spaces, punctuation, and case differences while performing the palindrome check.

---

### Input:  
A string `s` that may contain spaces, punctuation, and mixed case characters.

---

### Output:  
Return `True` if the string is a palindrome, otherwise return `False`.

---

### Constraints:  
1. The string will not be empty.  
2. The string may contain letters, numbers, spaces, and punctuation marks.  
3. The maximum length of the string will be **1000 characters**.

---

### Examples:

#### Example 1:  
**Input:**  
```
A man a plan a canal Panama  
```  
**Output:**  
```
True  
```  

---

#### Example 2:  
**Input:**  
```
Was it a car or a cat I saw?  
```  
**Output:**  
```
True  
```  

---

#### Example 3:  
**Input:**  
```
hello  
```  
**Output:**  
```
False  
```  

---

#### Example 4:  
**Input:**  
```
No lemon, no melon  
```  
**Output:**  
```
True  
```  

---

#### Example 5:  
**Input:**  
```
Able was I, ere I saw Elba  
```  
**Output:**  
```
True  
```  

---

#### Example 6:  
**Input:**  
```
Madam, in Eden, I'm Adam  
```  
**Output:**  
```
True  
```  

---

#### Example 7:  
**Input:**  
```
12321  
```  
**Output:**  
```
True  
```  

---

#### Example 8:  
**Input:**  
```
Was it a racecar or a cat I saw?  
```  
**Output:**  
```
True  
```  

---

#### Example 9:  
**Input:**  
```
notapalindrome  
```  
**Output:**  
```
False  
```  

---

#### Example 10:  
**Input:**  
```
Mr. Owl ate my metal worm  
```  
**Output:**  
```
True  
```  

---

### Solution:

```python
import string

def is_palindrome(s):
    cleaned_str = ""
    for char in s:
        if char.isalnum():  # Only keep alphanumeric characters
            cleaned_str += char.lower()  # Convert to lowercase
    return cleaned_str == cleaned_str[::-1]  # Check if the string is the same forwards and backwards

s = input()
print(is_palindrome(s))
```
