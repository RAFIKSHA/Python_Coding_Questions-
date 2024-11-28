### Task 19: Count the Frequency of Each Character in a String

**Problem Statement:**

Write a program to count the frequency of each character in a string.

---

### Input Format:

A single line containing a string `s`.

---

### Output Format:

Print each character and its frequency in the string.

---

### Constraints:

1. The string will have a length between 1 and 1000 characters.
2. The string may contain letters, digits, spaces, and other symbols.

---

### Example 1:

#### Input:
```
hello
```

#### Output:
```
h: 1
e: 1
l: 2
o: 1
```

---

### Example 2:

#### Input:
```
abcabc
```

#### Output:
```
a: 2
b: 2
c: 2
```

---

### Example 3:

#### Input:
```
python
```

#### Output:
```
p: 1
y: 1
t: 1
h: 1
o: 1
n: 1
```

---

### Example 4:

#### Input:
```
test
```

#### Output:
```
t: 2
e: 1
s: 1
```

---

### Example 5:

#### Input:
```
aabbcc
```

#### Output:
```
a: 2
b: 2
c: 2
```

---

### Example 6:

#### Input:
```
programming
```

#### Output:
```
p: 1
r: 2
o: 1
g: 2
a: 1
m: 2
i: 1
n: 1
```

---

### Example 7:

#### Input:
```
hello world
```

#### Output:
```
h: 1
e: 1
l: 3
o: 2
w: 1
r: 1
d: 1
```

---

### Example 8:

#### Input:
```
test123
```

#### Output:
```
t: 2
e: 1
s: 1
1: 1
2: 1
3: 1
```

---

### Example 9:

#### Input:
```
abc123abc
```

#### Output:
```
a: 2
b: 2
c: 2
1: 1
2: 1
3: 1
```

---

### Example 10:

#### Input:
```
apple
```

#### Output:
```
a: 1
p: 2
l: 1
e: 1
```

---

### Solution:

```python
def char_frequency(input_string):
    for char in set(input_string):
        print(f"{char}: {input_string.count(char)}")

input_string = input()
char_frequency(input_string)
```
