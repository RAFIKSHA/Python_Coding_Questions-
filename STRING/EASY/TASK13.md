### Task 13: Convert a String to Uppercase

**Problem Statement:**

Write a program to convert a given string to uppercase.

---

### Input Format:

- A single line of input containing a string `s`.

---

### Output Format:

- A single line of output with all the characters in uppercase.

---

### Constraints:

1. The input string will have a length between 1 and 1000 characters.

---

### Example 1:

#### Input:
```
Hello
```

#### Output:
```
HELLO
```

---

### Example 2:

#### Input:
```
Python
```

#### Output:
```
PYTHON
```

---

### Example 3:

#### Input:
```
mixed CASE
```

#### Output:
```
MIXED CASE
```

---

### Example 4:

#### Input:
```
hello world
```

#### Output:
```
HELLO WORLD
```

---

### Example 5:

#### Input:
```
python3
```

#### Output:
```
PYTHON3
```

---

### Example 6:

#### Input:
```
Data Science
```

#### Output:
```
DATA SCIENCE
```

---

### Example 7:

#### Input:
```
123abc
```

#### Output:
```
123ABC
```

---

### Example 8:

#### Input:
```
cOdE
```

#### Output:
```
CODE
```

---

### Example 9:

#### Input:
```
good morning!
```

#### Output:
```
GOOD MORNING!
```

---

### Example 10:

#### Input:
```
javaSCRIPT
```

#### Output:
```
JAVASCRIPT
```

### Solution:

```python
def to_uppercase(s):
    return s.upper()

input_string = input()
print(to_uppercase(input_string))
```

