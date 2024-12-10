### Task: **Longest Common Subsequence of Three Strings**

#### Problem Statement:
Given three real-world text strings `s1`, `s2`, and `s3`, your task is to find the length of the longest subsequence common to all three strings.

#### Input:
- Three strings `s1`, `s2`, and `s3`, where:
  - `1 ≤ |s1|, |s2|, |s3| ≤ 20`
  - All characters in the strings are lowercase English alphabets.

#### Output:
- An integer representing the length of the longest subsequence common to all three strings.

---

### Example 1:

**Input:**
```
developer
delight
deletion
```

**Output:**
```
4
```

---

### Example 2:

**Input:**
```
python
typhoon
potion
```

**Output:**
```
3
```

---

### Example 3:

**Input:**
```
database
dataentry
datapoint
```

**Output:**
```
4
```

---

### Example 4:

**Input:**
```
machinelearning
machinegun
machinery
```

**Output:**
```
7
```

---

### Example 5:

**Input:**
```
university
universal
unity
```

**Output:**
```
3
```

---

### Example 6:

**Input:**
```
artificial
artifact
artisan
```

**Output:**
```
5
```

---

### Example 7:

**Input:**
```
biology
biography
biophysics
```

**Output:**
```
3
```

---

### Example 8:

**Input:**
```
analytics
analysis
analyzer
```

**Output:**
```
6
```

---

### Example 9:

**Input:**
```
computerscience
computation
complete
```

**Output:**
```
7
```

---

### Example 10:

**Input:**
```
keyboard
keypad
keynote
```

**Output:**
```
3
```

---

### Solution:

```python
def lcs_of_three(s1, s2, s3):
    m, n, o = len(s1), len(s2), len(s3)
    dp = [[[0] * (o + 1) for _ in range(n + 1)] for _ in range(m + 1)]

    for i in range(1, m + 1):
        for j in range(1, n + 1):
            for k in range(1, o + 1):
                if s1[i - 1] == s2[j - 1] == s3[k - 1]:
                    dp[i][j][k] = dp[i - 1][j - 1][k - 1] + 1
                else:
                    dp[i][j][k] = max(dp[i - 1][j][k], dp[i][j - 1][k], dp[i][j][k - 1])
    
    return dp[m][n][o]

# Input: Each string is entered on a new line
s1 = input()
s2 = input()
s3 = input()

# Output: The length of the longest common subsequence
print(lcs_of_three(s1, s2, s3))
```
