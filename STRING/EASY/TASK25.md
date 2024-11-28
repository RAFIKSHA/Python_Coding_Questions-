---

### Task 25: Extract Numbers from a String

**Problem Statement:**
Write a program to extract all numbers from a given string and print them.

**Input Format:**
A single line containing a string `s`.

**Output Format:**
Output the extracted numbers separated by spaces.

---

### Example 1:

**Input:**  
`"abc123def456"`  
**Output:**  
`123 456`

### Example 2:

**Input:**  
`"hello12world34python56"`  
**Output:**  
`12 34 56`

### Example 3:

**Input:**  
`"no_numbers_here"`  
**Output:**  
(empty output)

### Example 4:

**Input:**  
`"abc1xyz234abc567"`  
**Output:**  
`1 234 567`

### Example 5:

**Input:**  
`"456apple789orange"`  
**Output:**  
`456 789`

### Example 6:

**Input:**  
`"123abc456xyz789"`  
**Output:**  
`123 456 789`

### Example 7:

**Input:**  
`"data123science456"`  
**Output:**  
`123 456`

### Example 8:

**Input:**  
`"test12test34test56"`  
**Output:**  
`12 34 56`

### Example 9:

**Input:**  
`"1word2word3"`  
**Output:**  
`1 2 3`

### Example 10:

**Input:**  
`"no_numbers_here"`  
**Output:**  
(empty output)

### Example 11:

**Input:**  
`"a1b2c3d4"`  
**Output:**  
`1 2 3 4`

---

**Solution:**

```python
def extract_numbers(input_string):
    numbers = ""
    result = []
    
    for char in input_string:
        if char.isdigit():
            numbers += char
        elif numbers:
            result.append(numbers)
            numbers = ""
    
    if numbers:
        result.append(numbers)
    
    print(" ".join(result))

input_string = input()
extract_numbers(input_string)
```
