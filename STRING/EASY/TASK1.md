### Task 1: Case Conversion

**Problem Statement:**

You are provided with a string, and your task is to modify it by swapping the cases of all alphabetic characters. This means converting all lowercase letters to uppercase and all uppercase letters to lowercase.

---

### Input Format:

- A single line containing a string `s`.

---

### Output Format:

- A single line containing the string with the case of each alphabetic character swapped.

---

### Constraints:

- The string `s` can contain any printable characters, including digits, symbols, and spaces.

---

### Example:

#### Input 1:
```
Campus.Credentials.com
```

#### Output 1:
```
cAMPUS.cREDENTIALS.COM
```

---

#### Input 2:
```
Pythonist 2
```

#### Output 2:
```
pYTHONIST 2
```

---

### Explanation:

- For the input "Campus.Credentials.com", all lowercase characters will be converted to uppercase and all uppercase characters will be converted to lowercase. The symbols and digits remain unchanged.

- For the input "Pythonist 2", the case of the alphabetic characters is swapped, and the number `2` remains unaffected.

---

### Solution in Python:

```python
def swap_case(s):
    return s.swapcase()

# Taking input from the user
input_string = input()

# Calling the swap_case function and storing the result
output_string = swap_case(input_string)

# Printing the modified string
print(output_string)
```

---

### How the Code Works:

1. **`swap_case(s)`**: This function uses Python's built-in `swapcase()` method, which returns a new string where all lowercase letters are converted to uppercase, and vice versa.
  
2. **Input**: The program reads an input string using the `input()` function.
  
3. **Output**: It prints the modified string after calling the `swap_case` function.

---

### Sample Test Cases:

#### Test Case 1:
**Input**:
```
Campus.Credentials.com
```

**Output**:
```
cAMPUS.cREDENTIALS.COM
```

#### Test Case 2:
**Input**:
```
Pythonist 2
```

**Output**:
```
pYTHONIST 2
```

---

### Time Complexity:

- **Time Complexity**: O(n), where `n` is the length of the string `s`, since we process each character exactly once.

- **Space Complexity**: O(n), as a new string is created to store the result after swapping cases.

---


