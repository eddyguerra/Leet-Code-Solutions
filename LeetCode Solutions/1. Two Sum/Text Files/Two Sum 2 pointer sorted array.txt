class Solution(object):
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        l, r = 0, len(nums) - 1

        while l < r:
            curSum = nums[l] + nums[r]

            if curSum > target:
                r -= 1
            elif curSum < target:
                l += 1
            else:
                return [l , r ]
        return [ ]
#Runs o(n) but if you sort it it will run 0(nlogn)