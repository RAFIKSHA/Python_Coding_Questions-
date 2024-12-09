### Task: **Group Anagrams Together**

#### Problem Statement:
You are given an array of strings. Your task is to group the strings that are anagrams together. Each group must be returned in lexicographical order, and the groups must appear in the order of their appearance in the original array.

#### Input:
- An array `arr[]` of strings, where:
  - `1 ≤ arr.size() ≤ 100`
  - `1 ≤ arr[i].size() ≤ 10`

#### Output:
- A list of lists, where each list contains strings that are anagrams of each other. The groups of anagrams should be sorted lexicographically, and the order of the groups should match their order of appearance in the input array.

---

### Example 1:

**Input:**
```
arr = ["act", "god", "cat", "dog", "tac"]
```

**Output:**
```
[["act", "cat", "tac"], ["god", "dog"]]
```

---

### Example 2:

**Input:**
```
arr = ["no", "on", "is"]
```

**Output:**
```
[["is"], ["no", "on"]]
```

---

### Example 3:

**Input:**
```
arr = ["listen", "silent", "enlist", "abc", "cab", "bac", "rat", "tar", "art"]
```

**Output:**
```
[["abc", "cab", "bac"], ["listen", "silent", "enlist"], ["rat", "tar", "art"]]
```

---

### Solution:

```python
from collections import defaultdict

def group_anagrams(arr):
    anagram_map = defaultdict(list)
    for word in arr:
        sorted_word = ''.join(sorted(word))
        anagram_map[sorted_word].append(word)
    result = [sorted(group) for group in anagram_map.values()]
    return result

arr = input().split()
print(group_anagrams(arr))
```
