### Task 13: Remove Recursively Adjacent Duplicate Characters

#### Problem Statement:
Given a string `s`, remove all its adjacent duplicate characters recursively until there are no adjacent duplicate characters left.

- If the resultant string becomes empty, return an empty string.

#### Input Format:
- A single string `s`.

#### Output Format:
- A string with all adjacent duplicates removed recursively.
- If the resultant string is empty, return an empty string.

#### Constraints:
- \(1 \leq \text{s.size()} \leq 10^5\)
- The string will only contain lowercase English letters.

---

#### Examples and Test Cases:

1. **Input:**  
   ```  
   s = "campuscredential"  
   ```  
   **Output:**  
   ```  
   "cmpusrdeial"  
   ```  
   **Explanation:**  
   campuscrede**ntia**l → cmpusrdeial  

2. **Input:**  
   ```  
   s = "abcddcba"  
   ```  
   **Output:**  
   ```  
   ""  
   ```  
   **Explanation:**  
   ab**cd**d**c**ba → ab**bb**ba → a**ba** → **""**  

3. **Input:**  
   ```  
   s = "abccbccba"  
   ```  
   **Output:**  
   ```  
   ""  
   ```  
   **Explanation:**  
   ab**cc**b**cc**ba → abbba → a**bbb**a → aa → **aa** → ""  

4. **Input:**  
   ```  
   s = "abcd"  
   ```  
   **Output:**  
   ```  
   "abcd"  
   ```  
   **Explanation:**  
   There are no adjacent duplicate characters.  

5. **Input:**  
   ```  
   s = "campuscampus"  
   ```  
   **Output:**  
   ```  
   ""  
   ```  
   **Explanation:**  
   campuscampus → cmpscmps → **cmp**s → **""**  

---

#### Solution:

```python
def remove_adjacent_duplicates(s):
    def helper(s):
        stack = []
        for char in s:
            if stack and stack[-1] == char:
                stack.pop()
            else:
                stack.append(char)
        return "".join(stack)
    
    while True:
        new_s = helper(s)
        if new_s == s:
            break
        s = new_s
    return s

# Input
s = input().strip()

# Output
result = remove_adjacent_duplicates(s)
print(result)
```
