### Task 18: Replace All Spaces with Underscores

**Problem Statement:**

Write a program to replace all spaces in a string with underscores.

---

### Input Format:

A single line containing a string `s`.

---

### Output Format:

Print the updated string with spaces replaced by underscores.

---

### Constraints:

1. The string will have a length between 1 and 1000 characters.
2. The string may contain spaces, letters, digits, and other symbols.

---

### Example 1:

#### Input:
```
hello world
```

#### Output:
```
hello_world
```

---

### Example 2:

#### Input:
```
Python Programming
```

#### Output:
```
Python_Programming
```

---

### Example 3:

#### Input:
```
space here
```

#### Output:
```
space_here
```

---

### Example 4:

#### Input:
```
hello there, how are you?
```

#### Output:
```
hello_there,_how_are_you?
```

---

### Example 5:

#### Input:
```
Open AI GPT
```

#### Output:
```
Open_AI_GPT
```

---

### Example 6:

#### Input:
```
this is a test
```

#### Output:
```
this_is_a_test
```

---

### Example 7:

#### Input:
```
replace spaces with underscores
```

#### Output:
```
replace_spaces_with_underscores
```

---

### Example 8:

#### Input:
```
hello  world 
```

#### Output:
```
hello__world_
```

---

### Example 9:

#### Input:
```
Python is fun
```

#### Output:
```
Python_is_fun
```

---

### Example 10:

#### Input:
```
test this one
```

#### Output:
```
test_this_one
```

---

### Solution:

```python
def replace_spaces(s):
    return s.replace(" ", "_")

input_string = input()
print(replace_spaces(input_string))
```
