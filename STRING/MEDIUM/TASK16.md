### Task 16: **Maximize the Number by Swapping Digits**

#### Problem Statement:
Given a number `k` and a string `s` of digits representing a positive integer, your task is to create the largest number possible by performing at most `k` swap operations on the digits of `s`. You can swap any two digits any number of times but the total number of swaps must not exceed `k`.

#### Input Format:
- A string `s` representing a positive integer, where `1 ≤ len(s) ≤ 1000`.
- An integer `k`, the maximum number of swaps allowed, where `1 ≤ k ≤ 10^3`.

#### Output Format:
- Return the largest number that can be formed by performing at most `k` swaps.

---

#### Example Test Cases:

1. **Input:**  
   ```  
   s = "1234567"
    k = 4  
   ```  
   **Output:**  
   ```  
   7654321  
   ```  
   **Explanation:**  
   Three swaps can make the input `1234567` into `7654321`, swapping `1` with `7`, `2` with `6`, and `3` with `5`.

2. **Input:**  
   ```  
   s = "3435335"
   k = 3  
   ```  
   **Output:**  
   ```  
   5543333  
   ```  
   **Explanation:**  
   Three swaps can transform `3435335` to `5543333`, swapping `3` with `5`, `4` with `5`, and finally `3` with `4`.

3. **Input:**  
   ```  
   s = "1034"
   k = 2  
   ```  
   **Output:**  
   ```  
   4301  
   ```  
   **Explanation:**  
   Two swaps can turn `1034` into `4301`, swapping `1` with `4` and `3` with `0`.

4. **Input:**  
   ```  
   s = "5678"
   k = 3  
   ```  
   **Output:**  
   ```  
   8765  
   ```  
   **Explanation:**  
   Three swaps can rearrange `5678` into `8765`, swapping `5` with `8`, `6` with `7`, and `7` with `6`.

5. **Input:**  
   ```  
   s = "1234"
   k = 2  
   ```  
   **Output:**  
   ```  
   4312  
   ```  
   **Explanation:**  
   Two swaps can make `1234` into `4312`, swapping `1` with `4` and `2` with `3`.

6. **Input:**  
   ```  
   s = "98765"
   k = 2  
   ```  
   **Output:**  
   ```  
   98765  
   ```  
   **Explanation:**  
   No swaps are needed as the input number is already the largest possible.

7. **Input:**  
   ```  
   s = "54321"
   k = 4  
   ```  
   **Output:**  
   ```  
   54321  
   ```  
   **Explanation:**  
   The input is already the largest possible number, no swaps needed.

8. **Input:**  
   ```  
   s = "121312"
   k = 3  
   ```  
   **Output:**  
   ```  
   321211  
   ```  
   **Explanation:**  
   Three swaps can turn `121312` into `321211`, swapping `1` with `3`, `2` with `3`, and `1` with `2`.

9. **Input:**  
   ```  
   s = "987"
   k = 1  
   ```  
   **Output:**  
   ```  
   987  
   ```  
   **Explanation:**  
   The input is already the largest possible number, no swap is required.

10. **Input:**  
    ```  
    s = "45321"
    k = 2  
    ```  
    **Output:**  
    ```  
    54321  
    ```  
    **Explanation:**  
    Two swaps can rearrange `45321` into `54321`, swapping `4` with `5` and `3` with `2`.

---

#### Solution:

```python
def find_maximum_num(s, k):
    s = list(s)
    
    def helper(s, k, index):
        if k == 0 or index == len(s):
            return ''.join(s)
        
        max_char = max(s[index:])
        if s[index] == max_char:
            return helper(s, k, index + 1)
        
        if k > 0:
            for i in range(len(s)-1, index, -1):
                if s[i] == max_char:
                    s[index], s[i] = s[i], s[index]
                    result = helper(s, k - 1, index + 1)
                    s[index], s[i] = s[i], s[index]  # Backtrack
                    return result
        return ''.join(s)

    return helper(s, k, 0)

s = input()
k = int(input())
print(find_maximum_num(s, k))
```
