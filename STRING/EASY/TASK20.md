### Task 20: Count the Number of Lowercase and Uppercase Letters in a String

**Problem Statement:**

Write a program to count the number of lowercase and uppercase letters in a string.

---

### Input Format:

A single line containing a string `s`.

---

### Output Format:

Print the number of lowercase and uppercase letters in the string.

---

### Constraints:

1. The string will have a length between 1 and 1000 characters.
2. The string may contain letters, digits, spaces, and special characters.

---

### Example 1:

#### Input:
```
Hello World
```

#### Output:
```
Lowercase: 8, Uppercase: 2
```

---

### Example 2:

#### Input:
```
Python Programming
```

#### Output:
```
Lowercase: 15, Uppercase: 2
```

---

### Example 3:

#### Input:
```
OpenAI
```

#### Output:
```
Lowercase: 3, Uppercase: 3
```

---

### Example 4:

#### Input:
```
abcDEF
```

#### Output:
```
Lowercase: 3, Uppercase: 3
```

---

### Example 5:

#### Input:
```
HELLO
```

#### Output:
```
Lowercase: 0, Uppercase: 5
```

---

### Example 6:

#### Input:
```
a b C d E
```

#### Output:
```
Lowercase: 4, Uppercase: 2
```

---

### Solution:

```python
def count_case(input_string):
    lowercase = 0
    uppercase = 0
    
    for char in input_string:
        if char.islower():
            lowercase += 1
        elif char.isupper():
            uppercase += 1
    
    print("Lowercase:", lowercase, "Uppercase:", uppercase)

input_string = input()
count_case(input_string)
```
