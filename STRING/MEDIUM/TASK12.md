---

### Task 12: Multiply Two Strings

#### Problem Statement:
Write a program to multiply two numbers represented as strings, `s1` and `s2`. The product should also be returned as a string. You are not allowed to use any built-in functions or convert the strings to integers. The numbers may contain leading zeros and could also be negative. If the result is positive, you don't need to specify a '+' sign at the beginning.

#### Input Format:
- Two strings `s1` and `s2` representing the numbers.

#### Output Format:
- The product of the two numbers as a string.

#### Constraints:
- `1 ≤ s1.size(), s2.size() ≤ 103`
- The numbers can be negative.
- There can be leading zeros in the numbers.

---

#### Examples and Test Cases:

1. **Input:**  
   ```
   s1 = "0033"  
   s2 = "2"  
   ```  
   **Output:**  
   ```
   "66"  
   ```  
   **Explanation:**  
   `33 * 2 = 66`

2. **Input:**  
   ```
   s1 = "11"  
   s2 = "23"  
   ```  
   **Output:**  
   ```
   "253"  
   ```  
   **Explanation:**  
   `11 * 23 = 253`

3. **Input:**  
   ```
   s1 = "123"  
   s2 = "0"  
   ```  
   **Output:**  
   ```
   "0"  
   ```  
   **Explanation:**  
   Anything multiplied by `0` results in `0`.

4. **Input:**  
   ```
   s1 = "9"  
   s2 = "99"  
   ```  
   **Output:**  
   ```
   "891"  
   ```  
   **Explanation:**  
   `9 * 99 = 891`

5. **Input:**  
   ```
   s1 = "999"  
   s2 = "999"  
   ```  
   **Output:**  
   ```
   "998001"  
   ```  
   **Explanation:**  
   `999 * 999 = 998001`

6. **Input:**  
   ```
   s1 = "005"  
   s2 = "100"  
   ```  
   **Output:**  
   ```
   "500"  
   ```  
   **Explanation:**  
   `5 * 100 = 500`

7. **Input:**  
   ```
   s1 = "123456789"  
   s2 = "987654321"  
   ```  
   **Output:**  
   ```
   "121932631112635269"  
   ```  
   **Explanation:**  
   `123456789 * 987654321 = 121932631112635269`

8. **Input:**  
   ```
   s1 = "-123"  
   s2 = "456"  
   ```  
   **Output:**  
   ```
   "-56088"  
   ```  
   **Explanation:**  
   `-123 * 456 = -56088`

9. **Input:**  
   ```
   s1 = "-11"  
   s2 = "-23"  
   ```  
   **Output:**  
   ```
   "253"  
   ```  
   **Explanation:**  
   `-11 * -23 = 253`

10. **Input:**  
    ```
    s1 = "0"  
    s2 = "0"  
    ```  
    **Output:**  
    ```
    "0"  
    ```  
    **Explanation:**  
    `0 * 0 = 0`

---

#### Solution:

```python

```python
def multiply_strings(s1, s2):
    is_negative = (s1[0] == '-') ^ (s2[0] == '-')
    s1, s2 = s1.lstrip('-0'), s2.lstrip('-0')
    if not s1 or not s2:
        return "0"
    result = [0] * (len(s1) + len(s2))
    for i in range(len(s1) - 1, -1, -1):
        for j in range(len(s2) - 1, -1, -1):
            mul = (ord(s1[i]) - ord('0')) * (ord(s2[j]) - ord('0'))
            pos1, pos2 = i + j, i + j + 1
            total = mul + result[pos2]
            result[pos1] += total // 10
            result[pos2] = total % 10
    result_str = ''.join(map(str, result)).lstrip('0')
    if is_negative and result_str:
        result_str = '-' + result_str
    return result_str or "0"

s1 = input().strip()
s2 = input().strip()
print(multiply_strings(s1, s2))
```

```

---
