### Task: Split a String into Balanced Parentheses

#### Problem Statement:
Write a program that splits a given string containing only parentheses `(` and `)` into the maximum number of balanced substrings. A balanced substring is one where every opening parenthesis `(` has a corresponding closing parenthesis `)`.

#### Input Format:
- A single string `s` containing only `(` and `)`.

#### Output Format:
- The number of balanced substrings in the given string.

#### Constraints:
- The string will only contain parentheses characters (`(` and `)`).
- The length of the string will be between 1 and 1000.

---

#### Examples and Test Cases:

1. **Input:**  
   ```
   (()())
   ```  
   **Output:**  
   ```
   2
   ```

2. **Input:**  
   ```
   ()()()
   ```  
   **Output:**  
   ```
   3
   ```

3. **Input:**  
   ```
   (()
   ```  
   **Output:**  
   ```
   0
   ```

4. **Input:**  
   ```
   (()())(())()
   ```  
   **Output:**  
   ```
   4
   ```

5. **Input:**  
   ```
   (((())))
   ```  
   **Output:**  
   ```
   1
   ```

6. **Input:**  
   ```
   ))((
   ```  
   **Output:**  
   ```
   0
   ```

7. **Input:**  
   ```
   ()(()())()
   ```  
   **Output:**  
   ```
   4
   ```

8. **Input:**  
   ```
   (((()
   ```  
   **Output:**  
   ```
   0
   ```

9. **Input:**  
   ```
   ))(()()(
   ```  
   **Output:**  
   ```
   0
   ```

10. **Input:**  
    ```
    (()(()()))
    ```  
    **Output:**  
    ```
    3
    ```

---

#### Solution:

```python
def count_balanced_substrings(s):
    balance = 0
    count = 0
    
    for char in s:
        if char == '(':
            balance += 1
        elif char == ')':
            balance -= 1
        
        if balance == 0:
            count += 1
    
    return count

s = input()
result = count_balanced_substrings(s)
print(result)
``` 
