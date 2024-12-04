### Task: Find the Minimum Number of Flips to Make a String Alternating

#### Problem Statement:
Given a binary string, determine the **minimum number of flips** required to make the string alternate between '0' and '1'. An alternating string is a string where no two adjacent characters are the same, e.g., "010101" or "101010".

You need to find the minimum number of bit flips to convert the given string into one of the two possible alternating patterns: either "010101..." or "101010...".

#### Input Format:
- A binary string `s` consisting of '0' and '1'.

#### Output Format:
- Return the **minimum number of flips** needed to convert the string into an alternating string.

#### Constraints:
- The length of `s` will be between 1 and 1000.

---

#### Examples and Test Cases:

1. **Input:**  
   ```  
   s = "0100"
   ```  
   **Output:**  
   ```  
   1
   ```  
   *(Flipping the last '0' to '1' will make the string "0101")*

2. **Input:**  
   ```  
   s = "1111"
   ```  
   **Output:**  
   ```  
   2
   ```  
   *(Flipping the second and fourth '1's to '0's will make the string "1010")*

3. **Input:**  
   ```  
   s = "010101"
   ```  
   **Output:**  
   ```  
   0
   ```  
   *(The string is already alternating, so no flips are needed)*

4. **Input:**  
   ```  
   s = "1001"
   ```  
   **Output:**  
   ```  
   1
   ```  
   *(Flipping the second '0' to '1' will make the string "1010")*

5. **Input:**  
   ```  
   s = "0000"
   ```  
   **Output:**  
   ```  
   2
   ```  
   *(Flipping the second and fourth '0's to '1's will make the string "0101")*

6. **Input:**  
   ```  
   s = "1"
   ```  
   **Output:**  
   ```  
   0
   ```  
   *(The string is already alternating, so no flips are needed)*

7. **Input:**  
   ```  
   s = "10"
   ```  
   **Output:**  
   ```  
   0
   ```  
   *(The string is already alternating, so no flips are needed)*

8. **Input:**  
   ```  
   s = "110"
   ```  
   **Output:**  
   ```  
   1
   ```  
   *(Flipping the second '1' to '0' will make the string "101")*

9. **Input:**  
   ```  
   s = "0101010101"
   ```  
   **Output:**  
   ```  
   0
   ```  
   *(The string is already alternating, so no flips are needed)*

10. **Input:**  
    ```  
    s = "111101"
    ```  
    **Output:**  
    ```  
    2
    ```  
    *(Flipping the second and fourth '1's to '0's will make the string "101010")*

---

#### Solution:

```python
def min_flips_to_alternate(s):
    # Option 1: starts with '0'
    flips1 = sum(1 for i in range(len(s)) if s[i] != ('0' if i % 2 == 0 else '1'))
    # Option 2: starts with '1'
    flips2 = sum(1 for i in range(len(s)) if s[i] != ('1' if i % 2 == 0 else '0'))
    
    return min(flips1, flips2)

s = input()
result = min_flips_to_alternate(s)
print(result)
```
