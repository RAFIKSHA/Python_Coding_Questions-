### Task: Check if One String Is a Subsequence of Another

#### Problem Statement:
Write a program to check if one string is a **subsequence** of another. A string `s2` is considered a subsequence of string `s1` if `s2` can be derived from `s1` by deleting some or no characters without changing the order of the remaining characters.

#### Input Format:
- Two strings `s1` and `s2`.

#### Output Format:
- Output `True` if `s2` is a subsequence of `s1`, otherwise output `False`.

#### Constraints:
- Both `s1` and `s2` will consist of only lowercase English letters.
- 1 ≤ Length of `s1`, `s2` ≤ 1000.

---

#### Examples and Test Cases:

1. **Input:**  
   ```  
   s1 = "abcde"
   s2 = "ace"
   ```  
   **Output:**  
   ```  
   True
   ```  

2. **Input:**  
   ```  
   s1 = "abcde"
   s2 = "aec"
   ```  
   **Output:**  
   ```  
   False
   ```  

3. **Input:**  
   ```  
   s1 = "hello"
   s2 = "hlo"
   ```  
   **Output:**  
   ```  
   True
   ```  

4. **Input:**  
   ```  
   s1 = "hannah"
   s2 = "hnh"
   ```  
   **Output:**  
   ```  
   True
   ```  

5. **Input:**  
   ```  
   s1 = "abcdef"
   s2 = "abz"
   ```  
   **Output:**  
   ```  
   False
   ```  

6. **Input:**  
   ```  
   s1 = "axbycz"
   s2 = "abc"
   ```  
   **Output:**  
   ```  
   True
   ```  

7. **Input:**  
   ```  
   s1 = "abracadabra"
   s2 = "acb"
   ```  
   **Output:**  
   ```  
   True
   ```  

8. **Input:**  
   ```  
   s1 = "abcdefgh"
   s2 = "ace"
   ```  
   **Output:**  
   ```  
   True
   ```  

9. **Input:**  
   ```  
   s1 = "computer"
   s2 = "cotr"
   ```  
   **Output:**  
   ```  
   True
   ```  

10. **Input:**  
    ```  
    s1 = "supercalifragilisticexpialidocious"
    s2 = "scl"
    ```  
    **Output:**  
    ```  
    True
    ```  

11. **Input:**  
    ```  
    s1 = "acde"
    s2 = "aed"
    ```  
    **Output:**  
    ```  
    False
    ```  

12. **Input:**  
    ```  
    s1 = "racecar"
    s2 = "rcar"
    ```  
    **Output:**  
    ```  
    True
    ```  

13. **Input:**  
    ```  
    s1 = "abcdef"
    s2 = "acf"
    ```  
    **Output:**  
    ```  
    True
    ```  

14. **Input:**  
    ```  
    s1 = "hello"
    s2 = "hello"
    ```  
    **Output:**  
    ```  
    True
    ```  

15. **Input:**  
    ```  
    s1 = "laptop"
    s2 = "ltp"
    ```  
    **Output:**  
    ```  
    True
    ```  

---

#### Solution:

```python
def is_subsequence(s1, s2):
    i, j = 0, 0
    while i < len(s1) and j < len(s2):
        if s1[i] == s2[j]:
            j += 1
        i += 1
    return j == len(s2)

s1 = input()
s2 = input()
result = is_subsequence(s1, s2)
print(result)
```
