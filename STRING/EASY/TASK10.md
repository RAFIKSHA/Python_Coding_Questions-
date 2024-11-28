### Task 10: Reverse a String

**Problem Statement:**

Reversing a string is a common operation in programming. Your task is to write a program that takes a string as input and outputs its reverse. The reversed string should preserve the case of letters and include any special characters or spaces.

---

### Input Format:

A single line of input containing a string `s`, which may include letters, digits, spaces, or special characters.

---

### Output Format:

A single line of output containing the reverse of the input string.

---

### Constraints:

1. The input string will have a length between 1 and 1000 characters.
2. The string may contain lowercase letters, uppercase letters, digits, spaces, and special characters.
3. The order of characters in the output must be the reverse of the input.

---

### Example 1:

#### Input:
```
hello world
```

#### Output:
```
dlrow olleh
```

---

### Example 2:

#### Input:
```
Python3!
```

#### Output:
```
!3nohtyP
```

---

### Example 3:

#### Input:
```
space here
```

#### Output:
```
ereh ecaps
```

---

### Example 4:

#### Input:
```
12345
```

#### Output:
```
54321
```

---

### Example 5:

#### Input:
```
OpenAI is great!
```

#### Output:
```
!taerg si IAnepO
```

---

### Example 6:

#### Input:
```
@hello!
```

#### Output:
```
!olleh@
```

---

### Example 7:

#### Input:
```
abc123
```

#### Output:
```
321cba
```

---

### Example 8:

#### Input:
```
reverse me
```

#### Output:
```
em esrever
```

---

### Example 9:

#### Input:
```
Good Morning
```

#### Output:
```
gninroM dooG
```

---

### Example 10:

#### Input:
```
welcome to the world!
```

#### Output:
```
!dlrow eht ot emoclew
```

---

### Solution:

```python
def reverse_string(s):
    return s[::-1]

input_string = input()
print(reverse_string(input_string))
```

---

