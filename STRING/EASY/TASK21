### Task 21: Count the Number of Special Characters in a String

**Problem Statement:**

Write a program to count the number of special characters in a given string.

---

### Input Format:

A single line containing a string `s`.

---

### Output Format:

Print the total count of special characters in the string.

---

### Constraints:

1. The string will have a length between 1 and 1000 characters.
2. The string may contain letters, digits, spaces, and special characters.

---

### Example 1:

#### Input:
```
Hello! World@123
```

#### Output:
```
2
```

---

### Example 2:

#### Input:
```
Python_Programming!
```

#### Output:
```
1
```

---

### Example 3:

#### Input:
```
Welcome$2024
```

#### Output:
```
1
```

---

### Example 4:

#### Input:
```
Good#Morning!
```

#### Output:
```
2
```

---

### Example 5:

#### Input:
```
abc@123
```

#### Output:
```
1
```

---

### Example 6:

#### Input:
```
Python$&Java
```

#### Output:
```
2
```

---

### Solution:

```python
def count_special_characters(input_string):
    count = 0
    for char in input_string:
        if not char.isalnum() and char != ' ':
            count += 1
    print("Special Characters:", count)

input_string = input()
count_special_characters(input_string)
```
