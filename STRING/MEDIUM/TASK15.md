### Task 15 : **Summing Two Large Numbers Represented as Strings**

#### Problem Statement:
You are given two strings `X` and `Y` that represent non-negative integers. Your task is to calculate and return the sum of these two numbers.

#### Input Format:
- Two strings `X` and `Y` representing non-negative integers, where the lengths of the strings can vary, but they represent valid numerical values.

#### Output Format:
- Return the sum of the two numbers as a string.

---

#### Example Test Cases:

1. **Input:**  
   ```  
   X = "25", Y = "23"  
   ```  
   **Output:**  
   ```  
   48  
   ```  
   **Explanation:**  
   The sum of 25 and 23 is 48.

2. **Input:**  
   ```  
   X = "2500", Y = "23"  
   ```  
   **Output:**  
   ```  
   2523  
   ```  
   **Explanation:**  
   The sum of 2500 and 23 is 2523.

3. **Input:**  
   ```  
   X = "100", Y = "200"  
   ```  
   **Output:**  
   ```  
   300  
   ```  
   **Explanation:**  
   The sum of 100 and 200 is 300.

4. **Input:**  
   ```  
   X = "999", Y = "1"  
   ```  
   **Output:**  
   ```  
   1000  
   ```  
   **Explanation:**  
   The sum of 999 and 1 is 1000.

5. **Input:**  
   ```  
   X = "123456789", Y = "987654321"  
   ```  
   **Output:**  
   ```  
   1111111110  
   ```  
   **Explanation:**  
   The sum of 123456789 and 987654321 is 1111111110.

6. **Input:**  
   ```  
   X = "0", Y = "0"  
   ```  
   **Output:**  
   ```  
   0  
   ```  
   **Explanation:**  
   The sum of 0 and 0 is 0.

7. **Input:**  
   ```  
   X = "111", Y = "222"  
   ```  
   **Output:**  
   ```  
   333  
   ```  
   **Explanation:**  
   The sum of 111 and 222 is 333.

8. **Input:**  
   ```  
   X = "1234", Y = "876"  
   ```  
   **Output:**  
   ```  
   2110  
   ```  
   **Explanation:**  
   The sum of 1234 and 876 is 2110.

9. **Input:**  
   ```  
   X = "987", Y = "654321"  
   ```  
   **Output:**  
   ```  
   655308  
   ```  
   **Explanation:**  
   The sum of 987 and 654321 is 655308.

10. **Input:**  
    ```  
    X = "1000", Y = "1000"  
    ```  
    **Output:**  
    ```  
    2000  
    ```  
    **Explanation:**  
    The sum of 1000 and 1000 is 2000.

---

#### Solution:

```python
def sum_large_numbers(X, Y):
    return str(int(X) + int(Y))

X = input()
Y = input()
print(sum_large_numbers(X, Y))
```
