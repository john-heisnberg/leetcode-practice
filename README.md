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

## 1️ Two Sum (Easy)

### Explanation

1. Initialize an empty dictionary (`map`) to store numbers and their indices.
2. Iterate through the array using an index `i`.
3. For each element, calculate the complement:
   complement = target - nums[i]
4. Check if the complement already exists in the dictionary.
- If it exists, return the current index and the stored index of the complement.
5. If the complement is not found, store the current number as a key and its index as the value in the dictionary.
6. Continue until a valid pair is found or the array is fully traversed.
7. Return an empty list if no valid pair exists.

###  Python Code
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
