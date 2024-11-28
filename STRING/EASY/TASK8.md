### Task 8: Calculate Character Frequency

#### Problem Statement:  
Write a program that calculates the frequency of each character in a given string and returns the result as a dictionary where the keys are the characters and the values are their respective counts. The program should handle alphanumeric characters, spaces, and special symbols.

---

### Input:  
A string `s` that contains alphabets, spaces, and other characters.

---

### Output:  
A dictionary where each key is a character from the string, and the value is the count of occurrences of that character.

---

### Constraints:  
1. The string will not be empty.  
2. The string contains alphanumeric characters and spaces.  
3. The maximum length of the string will be **1000 characters**.

---

### Example 1:

#### Input:
```
hello world
```

#### Output:
```
{'h': 1, 'e': 1, 'l': 3, 'o': 2, ' ': 1, 'w': 1, 'r': 1, 'd': 1}
```

---

### Example 2:

#### Input:
```
programming
```

#### Output:
```
{'p': 1, 'r': 2, 'o': 1, 'g': 2, 'a': 1, 'm': 2, 'i': 1, 'n': 1}
```

---

### Example 3:

#### Input:
```
abc 123
```

#### Output:
```
{'a': 1, 'b': 1, 'c': 1, ' ': 1, '1': 1, '2': 1, '3': 1}
```

---

### Example 4:

#### Input:
```
aabbcc
```

#### Output:
```
{'a': 2, 'b': 2, 'c': 2}
```

---

### Example 5:

#### Input:
```
hello! how are you?
```

#### Output:
```
{'h': 2, 'e': 2, 'l': 2, 'o': 3, '!': 1, ' ': 4, 'w': 1, 'a': 1, 'r': 1, 'y': 1, 'u': 1, '?: 1}
```

---

### Solution:

```python
def char_frequency(s):
    freq = {}
    for char in s:
        if char in freq:
            freq[char] += 1
        else:
            freq[char] = 1
    return freq

s = input()
print(char_frequency(s))
```
