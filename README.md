# LeetCode Problem Solving

This repository contains my solutions to LeetCode problems with:
- Clear explanations
- Python implementations
- Optimized approaches

## Topics Covered
- Arrays
- Linked Lists
- Strings
- Hashing
- Two Pointers
- Stack

# LeetCode Problem Solving (Python)

This repository documents my LeetCode problem-solving with explanations and code.

---

## 1️⃣ Two Sum (Easy)

🔗 https://leetcode.com/problems/two-sum/

### 💡 Explanation
- Take the first number
- Subtract it from the target
- Check if the constant exists using a hash map
- If found, return the pair

### ⏱ Complexity
- Time: O(n)
- Space: O(n)

### 🧠 Python Code
```python
def twoSum(nums, target):
    seen = {}
    for i, num in enumerate(nums):
        constant = target - num
        if constant in seen:
            return [seen[constant], i]
        seen[num] = i

