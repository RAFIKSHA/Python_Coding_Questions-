### **Task 1: Find the Smallest Window in a String Containing All Characters of Another String**

---

### **Problem Statement**
Write a program that takes two strings as input, `s1` and `s2`, and finds the smallest substring in `s1` that contains all the characters of `s2` (including duplicates). If no such substring exists, return `"Not Possible"`.

---

### **Input Format**
1. A string `s1` which may contain letters, digits, spaces, and special characters.
2. A string `s2` which contains the characters that must be present in the substring of `s1`.

---

### **Output Format**
A single line containing the smallest substring of `s1` that contains all characters of `s2`.  
If no such substring exists, output `"Not Possible"`.

---

### **Constraints**
1. The length of `s1` and `s2` can each be between 1 and 100,000 characters.
2. Both strings may contain uppercase and lowercase letters, digits, spaces, and special characters.
3. The characters in `s2` may be repeated, and the substring in `s1` must contain all instances of those characters.

---

### **Examples**

#### **Example 1**  
**Input:**  
```
ADOBECODEBANC
ABC
```
**Output:**  
```
BANC
```

---

#### **Example 2**  
**Input:**  
```
AA
AA
```
**Output:**  
```
AA
```

---

#### **Example 3**  
**Input:**  
```
A
AA
```
**Output:**  
```
Not Possible
```

---

#### **Example 4**  
**Input:**  
```
This is a test string
tist
```
**Output:**  
```
t stri
```

---

#### **Example 5**  
**Input:**  
```
aabbcc
abc
```
**Output:**  
```
aabbc
```

---

#### **Example 6**  
**Input:**  
```
Hello World!
lo
```
**Output:**  
```
lo Wo
```

---

#### **Example 7**  
**Input:**  
```
aA
a
```
**Output:**  
```
aA
```

---

#### **Example 8**  
**Input:**  
```
abcdefg
xyz
```
**Output:**  
```
Not Possible
```

---

#### **Example 9**  
**Input:**  
```
aaabcbc
abc
```
**Output:**  
```
abcbc
```

---

#### **Example 10**  
**Input:**  
```
aAabb
aba
```
**Output:**  
```
aAab
```

---

### **Solution**



```python
def smallest_window(s1, s2):
    if not s1 or not s2:
        return "Not Possible"

    required_chars = {}
    for char in s2:
        required_chars[char] = required_chars.get(char, 0) + 1

    window_chars = {}
    l = 0
    min_window = float("inf")
    result = ""
    required = len(required_chars)

    for r in range(len(s1)):
        window_chars[s1[r]] = window_chars.get(s1[r], 0) + 1

        if s1[r] in required_chars and window_chars[s1[r]] == required_chars[s1[r]]:
            required -= 1

        while required == 0:
            current_window_length = r - l + 1
            if current_window_length < min_window:
                min_window = current_window_length
                result = s1[l:r+1]

            window_chars[s1[l]] -= 1
            if s1[l] in required_chars and window_chars[s1[l]] < required_chars[s1[l]]:
                required += 1

            l += 1

    return result if result else "Not Possible"

s1 = input()
s2 = input()
print(smallest_window(s1, s2))
```

---
