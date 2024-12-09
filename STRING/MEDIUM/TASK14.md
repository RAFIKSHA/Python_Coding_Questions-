### Task 14: Calculating Factorial of Large Numbers Efficiently

#### Problem Statement:
Given an integer `n`, find the factorial of `n` and return a list of integers that make up the digits of the factorial.

#### Input Format:
- A single integer `n` (1 ≤ n ≤ 1000).

#### Output Format:
- A list of integers denoting the digits of `n!`.

#### Constraints:
- The input number `n` can be as large as 1000, so the factorial can be very large.

---

#### Example Test Cases:

1. **Input:**  
   ```  
   n = 5  
   ```  
   **Output:**  
   ```  
   [1, 2, 0]  
   ```  

2. **Input:**  
   ```  
   n = 10  
   ```  
   **Output:**  
   ```  
   [3, 6, 2, 8, 8, 0, 0]  
   ```  

3. **Input:**  
   ```  
   n = 1  
   ```  
   **Output:**  
   ```  
   [1]  
   ```  

4. **Input:**  
   ```  
   n = 3  
   ```  
   **Output:**  
   ```  
   [6]  
   ```  

5. **Input:**  
   ```  
   n = 6  
   ```  
   **Output:**  
   ```  
   [7, 2, 0]  
   ```  

6. **Input:**  
   ```  
   n = 7  
   ```  
   **Output:**  
   ```  
   [5, 0, 4, 0]  
   ```  

7. **Input:**  
   ```  
   n = 8  
   ```  
   **Output:**  
   ```  
   [4, 0, 3, 2, 0]  
   ```  

8. **Input:**  
   ```  
   n = 12  
   ```  
   **Output:**  
   ```  
   [4, 7, 1, 9, 8, 0, 0]  
   ```  

9. **Input:**  
   ```  
   n = 15  
   ```  
   **Output:**  
   ```  
   [1, 3, 1, 2, 0, 0, 0, 0]  
   ```  

10. **Input:**  
    ```  
    n = 20  
    ```  
    **Output:**  
    ```  
    [2, 4, 3, 2, 9, 2, 0, 3, 2, 0, 0]  
    ```  

---

#### Solution:

```python
def factorial_digits(n):
    result = 1
    for i in range(2, n + 1):
        result *= i
    return [int(x) for x in str(result)]

n = int(input())
print(factorial_digits(n))
```
