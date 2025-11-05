class Solution(object):
    def firstMissingPositive(self, nums):
        num_set = set(nums)
        for i in range(1, len(nums) + 2):  
            if i not in num_set:
                return i
