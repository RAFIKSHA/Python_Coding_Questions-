### Task 12: Remove Duplicates from a String

**Problem Statement:**

Write a program to remove all duplicate characters from a given string, keeping only the first occurrence of each character.

---

### Input Format:

A single line of input containing a string `s`, which may contain letters, digits, spaces, and special characters.

---

### Output Format:

A single line of output containing the string with all duplicate characters removed, preserving the order of their first occurrence.

---

### Constraints:

1. The input string will have a length between 1 and 1000 characters.
2. The string may contain lowercase letters, uppercase letters, digits, spaces, and special characters.
3. Only the first occurrence of each character is kept in the output string.

---

### Example 1:

#### Input:
```
hello world
```

#### Output:
```
helo wrd
```

---

### Example 2:

#### Input:
```
Python
```

#### Output:
```
Python
```

---

### Example 3:

#### Input:
```
aaabbbccc
```

#### Output:
```
abc
```

---

### Example 4:

#### Input:
```
Data Science is Amazing
```

#### Output:
```
Dat Sceinm
```

---

### Example 5:

#### Input:
```
123123456789
```

#### Output:
```
123456789
```

---

### Example 6:

#### Input:
```
AABBCDDDE
```

#### Output:
```
ABCDE
```

---

### Example 7:

#### Input:
```
!@#$$%^&*!!@#$$%
```

#### Output:
```
!@#$%^&*
```

---

### Solution:

```python
def remove_duplicates(s):
    result = ""
    for char in s:
        if char not in result:
            result += char
    return result

input_string = input()
print(remove_duplicates(input_string))
```

---
