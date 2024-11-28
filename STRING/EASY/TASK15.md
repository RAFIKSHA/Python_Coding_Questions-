### Task 15: Find the First Non-Repeating Character

**Problem Statement:**

Write a program that finds the first non-repeating character in a string and prints it. If all characters are repeated, print "None."

---

### Input Format:

A single line containing a string `s`.

---

### Output Format:

Print the first non-repeating character or "None."

---

### Constraints:

1. The string will have a length between 1 and 1000 characters.

---

### Example 1:

#### Input:
```
swiss
```

#### Output:
```
w
```

---

### Example 2:

#### Input:
```
aabb
```

#### Output:
```
None
```

---

### Example 3:

#### Input:
```
programming
```

#### Output:
```
p
```

---

### Example 4:

#### Input:
```
aabcc
```

#### Output:
```
b
```

---

### Example 5:

#### Input:
```
xyzzyx
```

#### Output:
```
None
```

---

### Example 6:

#### Input:
```
banana
```

#### Output:
```
b
```

---

### Example 7:

#### Input:
```
civic
```

#### Output:
```
None
```

---

### Example 8:

#### Input:
```
apple
```

#### Output:
```
a
```

---

### Example 9:

#### Input:
```
moon
```

#### Output:
```
m
```

---

### Example 10:

#### Input:
```
abacaba
```

#### Output:
```
c
```

---

### Solution:

```python
def first_non_repeating(s):
    for char in s:
        if s.count(char) == 1:
            return char
    return "None"

input_string = input()
print(first_non_repeating(input_string))
```
