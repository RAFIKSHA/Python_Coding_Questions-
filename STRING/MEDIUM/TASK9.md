### Task: Check for Overlapping Substrings

#### Problem Statement:
Write a program to check if two given substrings overlap in a given string. Two substrings overlap if there is any character that appears in both substrings when placed next to each other in the string.

#### Input Format:
- A single string `s`.
- Two substrings `sub1` and `sub2`.

#### Output Format:
- Return **True** if the two substrings overlap in the string `s`, otherwise return **False**.

#### Constraints:
- The string `s` and both substrings `sub1` and `sub2` will consist of lowercase English letters only.
- The length of the string `s` and the substrings will be between 1 and 1000.

---

#### Examples and Test Cases:

1. **Input:**  
   ```
   abcabc  
   ab  
   bc  
   ```  
   **Output:**  
   ```
   True  
   ```

2. **Input:**  
   ```
   hello  
   he  
   lo  
   ```  
   **Output:**  
   ```
   False  
   ```

3. **Input:**  
   ```
   abcde  
   abc  
   cde  
   ```  
   **Output:**  
   ```
   True  
   ```

4. **Input:**  
   ```
   abcde  
   abc  
   bcd  
   ```  
   **Output:**  
   ```
   True  
   ```

5. **Input:**  
   ```
   zigzag  
   zig  
   zag  
   ```  
   **Output:**  
   ```
   True  
   ```

6. **Input:**  
   ```
   programming  
   pro  
   am  
   ```  
   **Output:**  
   ```
   False  
   ```

7. **Input:**  
   ```
   startstart  
   star  
   art  
   ```  
   **Output:**  
   ```
   True  
   ```

8. **Input:**  
   ```
   hellohello  
   hello  
   hello  
   ```  
   **Output:**  
   ```
   True  
   ```

9. **Input:**  
   ```
   testcase  
   test  
   case  
   ```  
   **Output:**  
   ```
   False  
   ```

10. **Input:**  
    ```
    aaabbbaaa  
    aaa  
    bbb  
    ```  
    **Output:**  
    ```
    False  
    ```

---

#### Solution:

```python
def check_overlap(s, sub1, sub2):
    if sub1 in s and sub2 in s:
        for i in range(len(s) - len(sub1) + 1):
            if s[i:i + len(sub1)] == sub1:
                for j in range(i + len(sub1), len(s) - len(sub2) + 1):
                    if s[j:j + len(sub2)] == sub2:
                        return True
    return False

s = input()
sub1 = input()
sub2 = input()
result = check_overlap(s, sub1, sub2)
print(result)
``` 

---
