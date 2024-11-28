### Task 4: Check for Anagrams  

#### Problem Statement:  
Write a program to check if two given strings are anagrams of each other. Two strings are considered anagrams if they contain the same characters with the same frequency, regardless of the order of the characters.  

---

### Input:  
1. Two strings, `s1` and `s2`, which may contain alphanumeric characters.  
2. The strings can have different lengths.  

---

### Output:  
Return `True` if the two strings are anagrams of each other, and `False` otherwise.  

---

### Constraints:  
1. The strings contain only alphanumeric characters.  
2. The maximum length of each string is **1000 characters**.  

---

### Examples:  

#### Example 1:  
**Input:**  
```
listen  
silent
```  
**Output:**  
```
True
```  

---

#### Example 2:  
**Input:**  
```
hello  
world
```  
**Output:**  
```
False
```  

---

#### Example 3:  
**Input:**  
```
triangle  
integral
```  
**Output:**  
```
True
```  

---

#### Example 4:  
**Input:**  
```
Anagram  
nagaram
```  
**Output:**  
```
True
```  

---

#### Example 5:  
**Input:**  
```
rat  
car
```  
**Output:**  
```
False
```  

---

#### Example 6:  
**Input:**  
```
Test123  
123Test
```  
**Output:**  
```
True
```  

---

#### Example 7:  
**Input:**  
```
space case  
case space
```  
**Output:**  
```
True
```  

---

#### Example 8:  
**Input:**  
```
aabbcc  
ccbbaa
```  
**Output:**  
```
True
```  

---

#### Example 9:  
**Input:**  
```
12345  
54321
```  
**Output:**  
```
True
```  

---

#### Example 10:  
**Input:**  
```
abc123  
123abc4
```  
**Output:**  
```
False
```  

---

### Solution:  

```python
def are_anagrams(s1, s2):
    s1 = s1.replace(" ", "").lower()
    s2 = s2.replace(" ", "").lower()
    return sorted(s1) == sorted(s2)

s1 = input()
s2 = input()
print(are_anagrams(s1, s2))
```  
