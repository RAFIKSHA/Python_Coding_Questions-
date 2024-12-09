### Task 17: **Smallest Substring with All Unique Characters**

#### Problem Statement:
Given a string `s`, find the length of the smallest substring that contains all the unique characters of the string at least once. The goal is to identify the shortest window in the string where all the unique characters are present.

#### Input Format:
- A string `s`, where `1 ≤ s.size() ≤ 10^5`.

#### Output Format:
- Return the length of the smallest window that contains all unique characters of the string at least once.

---

#### Example Test Cases:

1. **Input:**  
   ```  
   s = "ABACBA"  
   ```  
   **Output:**  
   ```  
   3  
   ```  
   **Explanation:**  
   The smallest substring containing all distinct characters is `"BAC"` with a length of 3.

2. **Input:**  
   ```  
   s = "AABB"  
   ```  
   **Output:**  
   ```  
   2  
   ```  
   **Explanation:**  
   The smallest substring containing all distinct characters is `"AB"` with a length of 2.

3. **Input:**  
   ```  
   s = "MOMOTI"  
   ```  
   **Output:**  
   ```  
   4  
   ```  
   **Explanation:**  
   The smallest substring containing all distinct characters is `"MOTI"` with a length of 4.

4. **Input:**  
   ```  
   s = "HELLOHELLO"  
   ```  
   **Output:**  
   ```  
   4  
   ```  
   **Explanation:**  
   The smallest substring containing all distinct characters is `"HELO"` with a length of 4.

5. **Input:**  
   ```  
   s = "ABCABC"  
   ```  
   **Output:**  
   ```  
   3  
   ```  
   **Explanation:**  
   The smallest substring containing all distinct characters is `"ABC"` with a length of 3.

6. **Input:**  
   ```  
   s = "GRABITGRAB"  
   ```  
   **Output:**  
   ```  
   5  
   ```  
   **Explanation:**  
   The smallest substring containing all distinct characters is `"GRABT"` with a length of 5.

7. **Input:**  
   ```  
   s = "LOOP"  
   ```  
   **Output:**  
   ```  
   3  
   ```  
   **Explanation:**  
   The smallest substring containing all distinct characters is `"LOP"` with a length of 3.

8. **Input:**  
   ```  
   s = "ABCDEF"  
   ```  
   **Output:**  
   ```  
   6  
   ```  
   **Explanation:**  
   The smallest substring containing all distinct characters is the entire string `"ABCDEF"`, with a length of 6.

9. **Input:**  
   ```  
   s = "SKETCH"  
   ```  
   **Output:**  
   ```  
   6  
   ```  
   **Explanation:**  
   The smallest substring containing all distinct characters is the entire string `"SKETCH"`, with a length of 6.

10. **Input:**  
    ```  
    s = "YYXX"  
    ```  
    **Output:**  
    ```  
    3  
    ```  
    **Explanation:**  
    The smallest substring containing all distinct characters is `"YXY"` with a length of 3.

---

#### Solution:

```python
def smallest_distinct_window(s):
    n = len(s)
    distinct_chars = set(s)
    distinct_count = len(distinct_chars)

    start, end = 0, 0
    char_count = {}
    min_length = n + 1

    while end < n:
        char_count[s[end]] = char_count.get(s[end], 0) + 1

        while len(char_count) == distinct_count:
            min_length = min(min_length, end - start + 1)
            char_count[s[start]] -= 1
            if char_count[s[start]] == 0:
                del char_count[s[start]]
            start += 1

        end += 1
    
    return min_length

s = input()
print(smallest_distinct_window(s))
```
