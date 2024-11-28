### Task 6: Find the Longest Word in a String  

#### Problem Statement:  
Write a program that identifies the longest word in a given string. If there are multiple words with the same maximum length, the program should return the first one.  

---

### Input:  
A single string `s` consisting of words separated by spaces.  

---

### Output:  
The longest word in the input string. If there are multiple longest words, return the first one.  

---

### Constraints:  
1. The input string will not be empty.  
2. The string contains only alphabets and spaces.  
3. The maximum length of the input string will be **1000 characters**.  

---

### Examples:  

#### Example 1:  
**Input:**  
```
I love programming  
```  
**Output:**  
```
programming  
```  

---

#### Example 2:  
**Input:**  
```
The quick brown fox jumps over the lazy dog  
```  
**Output:**  
```
jumps  
```  

---

#### Example 3:  
**Input:**  
```
hello world  
```  
**Output:**  
```
hello  
```  

---

#### Example 4:  
**Input:**  
```
a bb ccc dddd eeee  
```  
**Output:**  
```
dddd  
```  

---

#### Example 5:  
**Input:**  
```
one two three four five  
```  
**Output:**  
```
three  
```  

---

#### Example 6:  
**Input:**  
```
abcdefg abc abcdefghij abcde  
```  
**Output:**  
```
abcdefghij  
```  

---

#### Example 7:  
**Input:**  
```
equal long words test cases  
```  
**Output:**  
```
equal  
```  

---

#### Example 8:  
**Input:**  
```
abcdefghijklmnopqrstuvwxyz  
```  
**Output:**  
```
abcdefghijklmnopqrstuvwxyz  
```  

---

#### Example 9:  
**Input:**  
```
shortest longest mid shortestagain  
```  
**Output:**  
```
shortest  
```  

---

#### Example 10:  
**Input:**  
```
justoneword  
```  
**Output:**  
```
justoneword  
```  

---

### Solution:  

```python
def longest_word(s):
    words = s.split()
    return max(words, key=len)

s = input()
print(longest_word(s))
```  
