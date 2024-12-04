### Task: Remove the kth Occurrence of a Character

#### Problem Statement:
Write a program that removes the **kth occurrence** of a specific character `ch` from a given string `s`. If the character `ch` does not appear `k` times, return the string unchanged.

#### Input Format:
- A string `s`.
- A character `ch` to be removed.
- An integer `k` denoting the occurrence number of the character to remove.

#### Output Format:
- Return the string after removing the **kth occurrence** of the character `ch`. If the `kth` occurrence doesn't exist, return the original string unchanged.

#### Constraints:
- The string will contain only alphabets and spaces.
- 1 ≤ Length of string ≤ 1000.
- `k` will be a positive integer and is guaranteed to be within the length of the string.

---

#### Examples and Test Cases:

1. **Input:**  
   ```  
   s = "hello world"
   ch = "l"
   k = 2
   ```  
   **Output:**  
   ```  
   "helo world"
   ```

2. **Input:**  
   ```  
   s = "abracadabra"
   ch = "a"
   k = 3
   ```  
   **Output:**  
   ```  
   "abrcadabra"
   ```

3. **Input:**  
   ```  
   s = "banana"
   ch = "a"
   k = 1
   ```  
   **Output:**  
   ```  
   "bnana"
   ```

4. **Input:**  
   ```  
   s = "mississippi"
   ch = "s"
   k = 4
   ```  
   **Output:**  
   ```  
   "missipipi"
   ```

5. **Input:**  
   ```  
   s = "abcd"
   ch = "c"
   k = 1
   ```  
   **Output:**  
   ```  
   "abd"
   ```

6. **Input:**  
   ```  
   s = "apple pie"
   ch = "p"
   k = 2
   ```  
   **Output:**  
   ```  
   "aple pie"
   ```

7. **Input:**  
   ```  
   s = "hello"
   ch = "z"
   k = 1
   ```  
   **Output:**  
   ```  
   "hello"
   ```

8. **Input:**  
   ```  
   s = "this is a test"
   ch = "t"
   k = 2
   ```  
   **Output:**  
   ```  
   "this is a est"
   ```

9. **Input:**  
   ```  
   s = "bob"
   ch = "b"
   k = 1
   ```  
   **Output:**  
   ```  
   "ob"
   ```

10. **Input:**  
    ```  
    s = "aabbcc"
    ch = "b"
    k = 2
    ```  
    **Output:**  
    ```  
    "aabcc"
    ```

---

#### Solution:

```python
def remove_kth_occurrence(s, ch, k):
    count = 0
    result = []
    
    for char in s:
        if char == ch:
            count += 1
            if count == k:
                continue
        result.append(char)
    
    return ''.join(result)

s = input()
ch = input()
k = int(input())
result = remove_kth_occurrence(s, ch, k)
print(result)
```
