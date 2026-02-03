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
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        map = {}
        for i in range(len(nums)):
            complement = target-nums[i]
            if complement in map:
                return [i,map[complement]]
            map[nums[i]] = i
        return []
