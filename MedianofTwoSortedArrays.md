# Median of Two Sorted Arrays — LeetCode Problem

### Problem Statement
Given two sorted arrays `nums1` and `nums2` of size `m` and `n` respectively, return the **median** of the two sorted arrays.

**The overall run time complexity should be O(log (m+n)).**

class Solution(object):
    def findMedianSortedArrays(self, nums1, nums2):
        out = sorted(nums1 + nums2)
        i = len(out)
        if i % 2 == 1:
            return out[i // 2]
        else:
            return (out[i // 2 - 1] + out[i // 2]) / 2.0
