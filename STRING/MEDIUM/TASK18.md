### Task: **Binary String Addition**

#### Problem Statement:
Given two binary strings `s1` and `s2` consisting of only `0`s and `1`s, calculate their sum and return the resultant binary string. The output string should not have any leading zeros.

#### Input Format:
- Two binary strings `s1` and `s2` where each string has a length between 1 and \(10^6\).

#### Output Format:
- A binary string representing the sum of `s1` and `s2`.

---

#### Example Test Cases:

1. **Input:**
   ```
   s1 = "1100", s2 = "101"
   ```
   **Output:**
   ```
   "11101"
   ```

2. **Input:**
   ```
   s1 = "110101", s2 = "101110"
   ```
   **Output:**
   ```
   "1101011"
   ```

3. **Input:**
   ```
   s1 = "111", s2 = "100"
   ```
   **Output:**
   ```
   "1011"
   ```

4. **Input:**
   ```
   s1 = "1001", s2 = "1100"
   ```
   **Output:**
   ```
   "11001"
   ```

5. **Input:**
   ```
   s1 = "1111", s2 = "1111"
   ```
   **Output:**
   ```
   "11110"
   ```

6. **Input:**
   ```
   s1 = "10101", s2 = "1101"
   ```
   **Output:**
   ```
   "100010"
   ```

7. **Input:**
   ```
   s1 = "100", s2 = "1101"
   ```
   **Output:**
   ```
   "1201"
   ```

8. **Input:**
   ```
   s1 = "1111", s2 = "10101"
   ```
   **Output:**
   ```
   "11100"
   ```

9. **Input:**
   ```
   s1 = "101010", s2 = "110100"
   ```
   **Output:**
   ```
   "1011110"
   ```

10. **Input:**
    ```
    s1 = "1000", s2 = "111"
    ```
    **Output:**
    ```
    "1111"
    ```

---

#### Solution:

```python
def add_binary(s1, s2):
    result = []
    carry = 0
    i, j = len(s1) - 1, len(s2) - 1
    
    while i >= 0 or j >= 0 or carry:
        val1 = int(s1[i]) if i >= 0 else 0
        val2 = int(s2[j]) if j >= 0 else 0
        total = val1 + val2 + carry
        
        carry = total // 2
        result.append(str(total % 2))
        
        i -= 1
        j -= 1
    
    return ''.join(result[::-1])

s1 = input()
s2 = input()

print(add_binary(s1, s2))
```
