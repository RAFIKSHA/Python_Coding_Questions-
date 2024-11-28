### Problem Statement:

Spaces in strings are often unnecessary in certain contexts, such as when processing input data or formatting text for storage. Your task is to write a program that takes a string as input and removes all spaces from it, producing a clean, uninterrupted string of characters.

---

### Input Format:

A single line of input containing a string `s`, which may include spaces in any position.

---

### Output Format:

A single line of output containing the same string `s`, but with all spaces removed.

---

### Constraints:

1. The input string will have a length between 1 and 1000 characters.
2. The string may contain lowercase letters, uppercase letters, digits, and spaces.
3. The output must preserve the order of all non-space characters.

---

### Example 1:

#### Input:
```
hello world
```

#### Output:
```
helloworld
```

---

### Example 2:

#### Input:
```
python is fun
```

#### Output:
```
pythonisfun
```

---

### Example 3:

#### Input:
```
space here
```

#### Output:
```
spacehere
```

---

### Example 4:

#### Input:
```
a b c
```

#### Output:
```
abc
```

---

### Example 5:

#### Input:
```
remove spaces please
```

#### Output:
```
removespacesplease
```

---

### Example 6:

#### Input:
```
no spaces in this string
```

#### Output:
```
nospacesinthisstring
```

---

### Example 7:

#### Input:
```
this is a test
```

#### Output:
```
thisisatest
```

---

### Example 8:

#### Input:
```
spaces  are   everywhere
```

#### Output:
```
spacesareeverywhere
```

---

### Example 9:

#### Input:
```
hello   world   again
```

#### Output:
```
helloworldagain
```

---

### Example 10:

#### Input:
```
oneword
```

#### Output:
```
oneword
```

---

### Example 11:

#### Input:
```
   multiple  spaces
```

#### Output:
```
multiplespaces
```

---

### Solution:

```python
def remove_spaces(s):
    return s.replace(" ", "")

input_string = input()
print(remove_spaces(input_string))
```
