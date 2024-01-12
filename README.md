# Remove-Duplicates-from-Sorted-Array
Given an integer array nums sorted in non-decreasing order, remove the duplicates in-place such that each unique element appears only once. The relative order of the elements should be kept the same. 

class Solution:
    def removeDuplicates(self, nums):
        if not nums:
            return 0

        slow = 0

        for fast in range(1, len(nums)):
            if nums[fast] != nums[slow]:
                slow += 1
                nums[slow] = nums[fast]

        return slow + 1


sol = Solution()
nums1 = [1, 1, 2]
k1 = sol.removeDuplicates(nums1)
print(k1, nums1)  
nums2 = [0, 0, 1, 1, 1, 2, 2, 3, 3, 4]
k2 = sol.removeDuplicates(nums2)
print(k2, nums2)  


