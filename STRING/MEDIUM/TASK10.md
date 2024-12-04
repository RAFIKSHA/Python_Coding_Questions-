### Task: Check if a String Can Be Split into Equal Parts

#### Problem Statement:
Write a program that determines if a given string `s` can be split into `n` equal parts without a remainder. If the string can be split equally, return `True`; otherwise, return `False`.

#### Input Format:
- A string `s`.
- An integer `n`.

#### Output Format:
- `True` if the string can be split into `n` equal parts; otherwise, `False`.

#### Constraints:
- The string will consist of lowercase English letters only.
- The integer `n` will be a positive integer.

---

#### Examples and Test Cases:

1. **Input:**  
   ```
   abcabc  
   3  
   ```  
   **Output:**  
   ```
   True  
   ```

2. **Input:**  
   ```
   abcabcabc  
   3  
   ```  
   **Output:**  
   ```
   True  
   ```

3. **Input:**  
   ```
   abcdef  
   2  
   ```  
   **Output:**  
   ```
   True  
   ```

4. **Input:**  
   ```
   hello  
   3  
   ```  
   **Output:**  
   ```
   False  
   ```

5. **Input:**  
   ```
   abc  
   2  
   ```  
   **Output:**  
   ```
   False  
   ```

6. **Input:**  
   ```
   aabbcc  
   2  
   ```  
   **Output:**  
   ```
   True  
   ```

7. **Input:**  
   ```
   abcd  
   4  
   ```  
   **Output:**  
   ```
   True  
   ```

8. **Input:**  
   ```
   test  
   3  
   ```  
   **Output:**  
   ```
   False  
   ```

9. **Input:**  
   ```
   xyzxyzxyz  
   3  
   ```  
   **Output:**  
   ```
   True  
   ```

10. **Input:**  
    ```
    aabbccdd  
    4  
    ```  
    **Output:**  
    ```
    True  
    ```

---

#### Solution:

```python
def can_split_into_equal_parts(s, n):
    if len(s) % n == 0:
        return True
    return False

s = input()
n = int(input())
result = can_split_into_equal_parts(s, n)
print(result)
``` 

---
