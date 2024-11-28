
---

### Task 24: Count Words in a String Without Using Split

**Problem Statement:**
Write a program to count the number of words in a string without using the `split()` method.

**Input Format:**
A single line containing a string `s`.

**Output Format:**
Output the number of words in the string.

---

### Example 1:

**Input:**  
`"The quick brown fox jumps"`  
**Output:**  
`5`

### Example 2:

**Input:**  
`"Data Science is the future"`  
**Output:**  
`5`

### Example 3:

**Input:**  
`"Artificial Intelligence"`  
**Output:**  
`2`

### Example 4:

**Input:**  
`"Machine learning at scale"`  
**Output:**  
`4`

### Example 5:

**Input:**  
`"Big data analysis techniques"`  
**Output:**  
`4`

### Example 6:

**Input:**  
`"Automated systems are essential"`  
**Output:**  
`4`

### Example 7:

**Input:**  
`"Hello there!"`  
**Output:**  
`2`

### Example 8:

**Input:**  
`"Cloud computing is evolving"`  
**Output:**  
`4`

### Example 9:

**Input:**  
`"Digital transformation in business"`  
**Output:**  
`4`

### Example 10:

**Input:**  
`"Global warming effects"`  
**Output:**  
`3`

### Example 11:

**Input:**  
`"Welcome to the jungle"`  
**Output:**  
`4`

---

**Solution:**

```python
def count_words(input_string):
    if input_string:
        count = 1
    else:
        count = 0
    count += input_string.count(" ")
    print(count)

input_string = input()
count_words(input_string)
```
