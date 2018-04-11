# two sum

## 问题

Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

Example:

```
Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
```

## 思路
转化问题为两个数的组合, 因此用两个循环就能解决了

```python
class Solution(object):
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        i = 0
        nums_length = len(nums)
        while(i < nums_length):
            j = i + 1
            while(j < nums_length):
                if(nums[i] + nums[j] == target):
                    return [i, j]
                j += 1
            i += 1
```