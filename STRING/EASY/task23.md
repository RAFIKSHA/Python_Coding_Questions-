### Task 23: Check if All Characters Are Unique

**Problem Statement:**

Write a program to check if all characters in a string are unique.

---

### Input Format:

A single line containing a string `s`.

---

### Output Format:

Print `True` if all characters in the string are unique, otherwise print `False`.

---

### Constraints:

1. The string will have a length between 1 and 1000 characters.
2. The string may contain letters, digits, spaces, and special characters.

---

### Example 1:

#### Input:
```
abcde
```

#### Output:
```
True
```

---

### Example 2:

#### Input:
```
hello
```

#### Output:
```
False
```

---

### Example 3:

#### Input:
```
Python
```

#### Output:
```
True
```

---

### Example 4:

#### Input:
```
123123
```

#### Output:
```
False
```

---

### Example 5:

#### Input:
```
abcdefg
```

#### Output:
```
True
```

---

### Example 6:

#### Input:
```
aa
```

#### Output:
```
False
```

---

### Example 7:

#### Input:
```
XYZ
```

#### Output:
```
True
```

---

### Example 8:

#### Input:
```
OpenAI
```

#### Output:
```
True
```

---

### Example 9:

#### Input:
```
hello123
```

#### Output:
```
False
```

---

### Example 10:

#### Input:
```
12345
```

#### Output:
```
True
```

---

### Example 11:

#### Input:
```
!@#$
```

#### Output:
```
True
```

---

### Solution:

```python
def are_characters_unique(s):
    print(len(set(s)) == len(s))

input_string = input()
are_characters_unique(input_string)
```
