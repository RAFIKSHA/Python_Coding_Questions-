### Task 22: Remove All Non-Alphabetic Characters

**Problem Statement:**

Write a program to remove all non-alphabetic characters from a string.

---

### Input Format:

A single line containing a string `s`.

---

### Output Format:

Print the string after removing all non-alphabetic characters.

---

### Constraints:

1. The string will have a length between 1 and 1000 characters.
2. The string may contain letters, digits, spaces, and special characters.

---

### Example 1:

#### Input:
```
Hello@123
```

#### Output:
```
Hello
```

---

### Example 2:

#### Input:
```
Python#Rocks!
```

#### Output:
```
PythonRocks
```

---

### Example 3:

#### Input:
```
12345
```

#### Output:
```
(Empty String)
```

---

### Example 4:

#### Input:
```
Coding_4_Life!
```

#### Output:
```
CodingLife
```

---

### Solution:

```python
def remove_non_alphabets(s):
    result = ""
    for char in s:
        if char.isalpha():
            result += char
    print(result)

# Input the string
input_string = input()
remove_non_alphabets(input_string)
```
