### Task 17: Check if a String Contains Only Digits

**Problem Statement:**

Write a program that checks whether a given string contains only digits.

---

### Input Format:

A single line containing a string `s`.

---

### Output Format:

Print "Yes" if the string contains only digits, otherwise print "No."

---

### Constraints:

1. The string will have a length between 1 and 100 characters.

---

### Example 1:

#### Input:
```
12345
```

#### Output:
```
Yes
```

---

### Example 2:

#### Input:
```
12abc34
```

#### Output:
```
No
```

---

### Example 3:

#### Input:
```
007
```

#### Output:
```
Yes
```

---

### Example 4:

#### Input:
```
000000
```

#### Output:
```
Yes
```

---

### Example 5:

#### Input:
```
123.45
```

#### Output:
```
No
```

---

### Example 6:

#### Input:
```
1A23
```

#### Output:
```
No
```

---

### Example 7:

#### Input:
```
9876543210
```

#### Output:
```
Yes
```

---

### Example 8:

#### Input:
```
0
```

#### Output:
```
Yes
```

---

### Example 9:

#### Input:
```
abc123
```

#### Output:
```
No
```

---

### Example 10:

#### Input:
```
987654
```

#### Output:
```
Yes
```

---

### Solution:

```python
def is_digit_only(s):
    return s.isdigit()

input_string = input()
if is_digit_only(input_string):
    print("Yes")
else:
    print("No")
```
