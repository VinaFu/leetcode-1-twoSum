# leetcode-1-twoSum

1)class Solution:

            def twoSum(self, nums:List[int],target:int):
                l = len(nums)
                for i in range(0, l-1):
                    for j in range(i+1, l):
                        if nums[i] + nums [j] ==target:
                            return [i, j]
2) hash_table: 哈希表格

            def twoSum(self, nums:List[int],target:int):
                l = len(nums)
                hash_table = {} 
        #         put index
                for i in range(l):
                    hash_table[nums[i]] = i
        #             map value to index, build a class to switch value and index

                for i in range(l):
                    if target - nums[i] in hash_table:
                        if hash_table[target - nums[i]] != i:
                        # ensure it is not itself.
                            return [i, hash_table[target-nums[i]]]

