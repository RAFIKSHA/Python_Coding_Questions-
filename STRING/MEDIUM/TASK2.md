### Task: Find the Longest Palindromic Substring  

#### Problem Statement:  
Write a program to identify the **longest palindromic substring** in a given string. A palindrome is a sequence of characters that reads the same backward as forward.

#### Input Format:  
- A single string `s`.

#### Output Format:  
- A single line containing the **longest palindromic substring** in the given input string.  
- If there are multiple palindromic substrings of the same length, return any one.

#### Constraints:  
- The string will only consist of lowercase English letters.
- 1 ≤ Length of string ≤ 1000.

---

#### Examples and Test Cases:

1. **Input:**  
   ```
   babad
   ```  
   **Output:**  
   ```
   bab
   ```  
   *(or "aba")*

2. **Input:**  
   ```
   cbbd
   ```  
   **Output:**  
   ```
   bb
   ```

3. **Input:**  
   ```
   a
   ```  
   **Output:**  
   ```
   a
   ```

4. **Input:**  
   ```
   ac
   ```  
   **Output:**  
   ```
   a
   ```  
   *(or "c")*

5. **Input:**  
   ```
   racecar
   ```  
   **Output:**  
   ```
   racecar
   ```

6. **Input:**  
   ```
   abcdcba
   ```  
   **Output:**  
   ```
   abcdcba
   ```

7. **Input:**  
   ```
   banana
   ```  
   **Output:**  
   ```
   anana
   ```

8. **Input:**  
   ```
   abba
   ```  
   **Output:**  
   ```
   abba
   ```

9. **Input:**  
   ```
   abcdef
   ```  
   **Output:**  
   ```
   a
   ```  
   *(or "b", "c", "d", "e", "f")*

10. **Input:**  
    ```
    abccbc
    ```  
    **Output:**  
    ```
    bccb
    ```

---

#### Solution:

```python
def longest_palindrome(s):
    n = len(s)
    if n == 0:
        return ""
    
    longest = ""
    
    for i in range(n):
        for j in range(i + 1, n + 1):
            substring = s[i:j]
            if substring == substring[::-1] and len(substring) > len(longest):
                longest = substring
    
    return longest

# Input from the user
input_string = input()
result = longest_palindrome(input_string)
print("Longest Palindromic Substring:", result)
```
