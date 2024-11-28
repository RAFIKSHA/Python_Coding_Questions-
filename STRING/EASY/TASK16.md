### Task 16: Find the ASCII Value of Each Character in a String

**Problem Statement:**

Write a program that takes a string as input and prints the ASCII value of each character in the string.

---

### Input Format:

A single line containing a string `s`.

---

### Output Format:

Print the ASCII values of the characters in the string, separated by spaces.

---

### Constraints:

1. The string will have a length between 1 and 100 characters.

---

### Example 1:

#### Input:
```
abc
```

#### Output:
```
97 98 99
```

---

### Example 2:

#### Input:
```
A1
```

#### Output:
```
65 49
```

---

### Example 3:

#### Input:
```
hello
```

#### Output:
```
104 101 108 108 111
```

---

### Example 4:

#### Input:
```
Python
```

#### Output:
```
80 121 116 104 111 110
```

---

### Example 5:

#### Input:
```
123
```

#### Output:
```
49 50 51
```

---

### Example 6:

#### Input:
```
@#$
```

#### Output:
```
64 35 36
```

---

### Example 7:

#### Input:
```
aBcD
```

#### Output:
```
97 66 67 68
```

---

### Example 8:

#### Input:
```
space
```

#### Output:
```
115 112 97 99 101
```

---

### Example 9:

#### Input:
```
ABCD
```

#### Output:
```
65 66 67 68
```

---

### Example 10:

#### Input:
```
hello world!
```

#### Output:
```
104 101 108 108 111 32 119 111 114 108 100 33
```

---

### Solution:

```python
def ascii_values(s):
    result = []
    for char in s:
        result.append(str(ord(char)))
    return " ".join(result)

input_string = input()
print(ascii_values(input_string))
```
