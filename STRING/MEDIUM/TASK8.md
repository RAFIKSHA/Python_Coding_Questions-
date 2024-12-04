

### Task: Find the Length of the Shortest Uncommon Subsequence

#### Problem Statement:
Write a program to find the length of the **shortest subsequence** in one string `s1` that is **not** a subsequence of another string `s2`. A subsequence of a string is a sequence that can be derived from the string by deleting some or no characters without changing the order of the remaining characters.

#### Input Format:
- Two strings `s1` and `s2`.

#### Output Format:
- The length of the shortest subsequence in `s1` that is **not** a subsequence of `s2`.

#### Constraints:
- Both strings will consist of lowercase English letters only.
- The length of the strings will be between 1 and 1000.

---

#### Examples and Test Cases:

1. **Input:**  
   ```
   abc  
   acbd  
   ```  
   **Output:**  
   ```
   1  
   ```

2. **Input:**  
   ```
   abc  
   ab  
   ```  
   **Output:**  
   ```
   3  
   ```

3. **Input:**  
   ```
   axc  
   ahbgdc  
   ```  
   **Output:**  
   ```
   3  
   ```

4. **Input:**  
   ```
   abc  
   abc  
   ```  
   **Output:**  
   ```
   4  
   ```

5. **Input:**  
   ```
   bca  
   abc  
   ```  
   **Output:**  
   ```
   3  
   ```

6. **Input:**  
   ```
   abcdef  
   abc  
   ```  
   **Output:**  
   ```
   6  
   ```

7. **Input:**  
   ```
   xy  
   y  
   ```  
   **Output:**  
   ```
   2  
   ```

8. **Input:**  
   ```
   hello  
   elloh  
   ```  
   **Output:**  
   ```
   5  
   ```

9. **Input:**  
   ```
   xyz  
   yxz  
   ```  
   **Output:**  
   ```
   3  
   ```

10. **Input:**  
    ```
    apple  
    pple  
    ```  
    **Output:**  
    ```
    5  
    ```

---

#### Solution:

```python
def shortest_uncommon_subsequence(s1, s2):
    if s1 not in s2:
        return len(s1)
    
    for i in range(1, len(s1) + 1):
        for j in range(len(s1) - i + 1):
            if s1[j:j+i] not in s2:
                return i
    return len(s1) + 1

s1 = input()
s2 = input()
result = shortest_uncommon_subsequence(s1, s2)
print(result)
```
