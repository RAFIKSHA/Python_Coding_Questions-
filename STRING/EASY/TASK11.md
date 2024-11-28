### Task 11: Count the Number of Vowels in a String

**Problem Statement:**

Write a program that takes a string as input and counts the number of vowels (a, e, i, o, u) in the string. Vowels should be counted regardless of case (i.e., both uppercase and lowercase vowels should be considered).

---

### Input Format:

A single line of input containing a string `s`, which may include letters, digits, spaces, and special characters.

---

### Output Format:

A single integer representing the number of vowels in the input string.

---

### Constraints:

1. The input string will have a length between 1 and 1000 characters.
2. The string may contain lowercase letters, uppercase letters, spaces, and special characters.
3. Only vowels (a, e, i, o, u) should be counted, regardless of case.

---

### Example 1:

#### Input:
```
Welcome to the future of AI
```

#### Output:
```
9
```

---

### Example 2:

#### Input:
```
Python3
```

#### Output:
```
1
```

---

### Example 3:

#### Input:
```
AEIOU
```

#### Output:
```
5
```

---

### Example 4:

#### Input:
```
Artificial Intelligence
```

#### Output:
```
8
```

---

### Example 5:

#### Input:
```
Data Science
```

#### Output:
```
4
```

---

### Example 6:

#### Input:
```
Coding is Fun!
```

#### Output:
```
4
```

---

### Example 7:

#### Input:
```
Vowels Are Important
```

#### Output:
```
8
```

---

### Example 8:

#### Input:
```
123 Hello World!
```

#### Output:
```
3
```

---

### Example 9:

#### Input:
```
Quantum Computing
```

#### Output:
```
6
```

---

### Example 10:

#### Input:
```
AI in Healthcare
```

#### Output:
```
7
```

---

### Solution:

```python
def count_vowels(s):
    vowels = "aeiouAEIOU"
    return sum(1 for char in s if char in vowels)

input_string = input()
print(count_vowels(input_string))
```

---
