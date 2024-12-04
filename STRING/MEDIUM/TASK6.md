### Task: Interleave Two Strings

#### Problem Statement:
Given two strings, **merge** them by interleaving their characters. The interleaved string should take one character from `s1`, then one from `s2`, and so on. If one string is longer than the other, append the remaining characters from the longer string at the end.

#### Input Format:
- Two strings `s1` and `s2`.

#### Output Format:
- Return a string where the characters of `s1` and `s2` are interleaved.

#### Constraints:
- The length of both strings will be between 1 and 1000.
- If the strings have different lengths, append the remaining characters from the longer string at the end.

---

#### Examples and Test Cases:

1. **Input:**  
   ```  
   s1 = "abc", s2 = "123"
   ```  
   **Output:**  
   ```  
   "a1b2c3"
   ```

2. **Input:**  
   ```  
   s1 = "hello", s2 = "world"
   ```  
   **Output:**  
   ```  
   "hweolrllod"
   ```

3. **Input:**  
   ```  
   s1 = "abc", s2 = "xyz"
   ```  
   **Output:**  
   ```  
   "axbycz"
   ```

4. **Input:**  
   ```  
   s1 = "abc", s2 = "1"
   ```  
   **Output:**  
   ```  
   "a1bc"
   ```

5. **Input:**  
   ```  
   s1 = "abc", s2 = ""
   ```  
   **Output:**  
   ```  
   "abc"
   ```

6. **Input:**  
   ```  
   s1 = "1", s2 = "abcdef"
   ```  
   **Output:**  
   ```  
   "1abcdef"
   ```

7. **Input:**  
   ```  
   s1 = "abcd", s2 = "1234"
   ```  
   **Output:**  
   ```  
   "a1b2c3d4"
   ```

8. **Input:**  
   ```  
   s1 = "abcd", s2 = "xyz"
   ```  
   **Output:**  
   ```  
   "axbyczd"
   ```

9. **Input:**  
   ```  
   s1 = "a", s2 = "bcdefgh"
   ```  
   **Output:**  
   ```  
   "abcdefgh"
   ```

10. **Input:**  
    ```  
    s1 = "apple", s2 = "juice"
    ```  
    **Output:**  
    ```  
    "ajpuppliee"
    ```

---

#### Solution:

```python
def interleave_strings(s1, s2):
    result = []
    i, j = 0, 0
    while i < len(s1) and j < len(s2):
        result.append(s1[i])
        result.append(s2[j])
        i += 1
        j += 1
    
    # Append any remaining characters from s1 or s2
    result.append(s1[i:])
    result.append(s2[j:])
    
    return ''.join(result)

s1 = input()
s2 = input()
result = interleave_strings(s1, s2)
print(result)
```
