### Task 14: Remove All Occurrences of a Character in a String

**Problem Statement:**

Write a program that takes a string and a character as input and removes all occurrences of the given character from the string.

---

### Input Format:

- The first line contains a string `s`.
- The second line contains a character `c` to remove from the string.

---

### Output Format:

- A single line containing the string after removing all occurrences of the character `c`.

---

### Constraints:

1. The string will have a length between 1 and 1000 characters.
2. The character to remove will be a single lowercase or uppercase letter.

---

### Example 1:

#### Input:
```
hello world
o
```

#### Output:
```
hell wrld
```

---

### Example 2:

#### Input:
```
Python3
3
```

#### Output:
```
Python
```

---

### Example 3:

#### Input:
```
space here
e
```

#### Output:
```
spac hr
```

---

### Example 4:

#### Input:
```
Data Science
e
```

#### Output:
```
Data Scinc
```

---

### Example 5:

#### Input:
```
123123456789
1
```

#### Output:
```
23456789
```

---

### Example 6:

#### Input:
```
AABBCDDDE
D
```

#### Output:
```
AABBCDEE
```

---

### Example 7:

#### Input:
```
!@#$$%^&*!!@#$$%
$
```

#### Output:
```
!@#%^&*&@#%%
```

---

### Example 8:

#### Input:
```
hello universe
l
```

#### Output:
```
heo universe
```

---

### Example 9:

#### Input:
```
The quick brown fox
q
```

#### Output:
```
The uick brown fox
```

---

### Example 10:

#### Input:
```
Welcome to the party
t
```

#### Output:
```
Welcome o he pary
```

---

### Solution:

```python
def remove_char(s, c):
    return s.replace(c, '')

input_string = input()
char_to_remove = input()
print(remove_char(input_string, char_to_remove))
```
