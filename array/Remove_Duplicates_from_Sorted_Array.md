# 26. Remove Duplicates from Sorted Array

## 问题

Given a sorted array, remove the duplicates in-place such that each element appear only once and return the new length.

Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

Example:

```
Given nums = [1,1,2],

Your function should return length = 2, with the first two elements of nums being 1 and 2 respectively.
It doesn't matter what you leave beyond the new length.
```

## 思路
使用两个 pointer，一个用来寻找不重复的，一个代表原来位置。找到不重复的后就替换原来位置的

```python
class Solution(object):
    def removeDuplicates(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        if(not nums): return 0
    
        i = 0
        j = i + 1
        nums_len = len(nums)

        while(j < nums_len):
            if (nums[i] != nums[j]):
                i += 1
                nums[i] = nums[j]
            j += 1
            
        return i + 1
```                
                
                    
        