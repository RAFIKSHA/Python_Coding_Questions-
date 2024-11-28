### Task: Remove Vowels from a String  

#### Problem Statement:  
Write a program that removes all vowels (`a, e, i, o, u`) from a given string while maintaining the order of the remaining characters.  

---

### Input:  
A single string `s` containing alphanumeric characters and spaces.  

---

### Output:  
A string with all vowels removed, preserving the order of the remaining characters.  

---

### Constraints:  
1. The string will contain only lowercase or uppercase alphabetic characters and spaces.  
2. The maximum length of the string will be **1000 characters**.  

---

### Examples:  

#### Example 1:  
**Input:**  
```
hello world  
```  
**Output:**  
```
hll wrld  
```  

---

#### Example 2:  
**Input:**  
```
programming  
```  
**Output:**  
```
prgrmmng  
```  

---

#### Example 3:  
**Input:**  
```
aeiou  
```  
**Output:**  
```
  
```  

---

#### Example 4:  
**Input:**  
```
Python is Fun  
```  
**Output:**  
```
Pythn s Fn  
```  

---

#### Example 5:  
**Input:**  
```
12345abcde  
```  
**Output:**  
```
12345bcd  
```  

---

#### Example 6:  
**Input:**  
```
VOWELS ARE REMOVED  
```  
**Output:**  
```
VWLS R RMVD  
```  

---

#### Example 7:  
**Input:**  
```
The quick brown fox jumps over the lazy dog  
```  
**Output:**  
```
Th qck brwn fx jmps vr th lzy dg  
```  

---

#### Example 8:  
**Input:**  
```
A E I O U  
```  
**Output:**  
```
  
```  

---

#### Example 9:  
**Input:**  
```
Space 123 !@#  
```  
**Output:**  
```
Spc 123 !@#  
```  

---

#### Example 10:  
**Input:**  
```
aeIoU_Consonants_123  
```  
**Output:**  
```
_Cnsnnts_123  
```  

---

### Solution:  

```python
def remove_vowels(s):
    for vowel in "aeiouAEIOU":
        s = s.replace(vowel, "")
    return s

s = input()
print(remove_vowels(s))
```  
