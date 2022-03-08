# 剑指 Offer II 010. 和为 k 的子数组
难度：中等   
题目地址：https://leetcode-cn.com/problems/QTMn0o/   
完成时间：  2022/3/8   
# 题目

给定一个整数数组和一个整数 k ，请找到该数组中和为 k 的连续子数组的个数。

**示例 1 :**
```
输入:nums = [1,1,1], k = 2
输出: 2
解释: 此题 [1,1] 与 [1,1] 为两种不同的情况
```
**示例 2 :**
```
输入:nums = [1,2,3], k = 3
输出: 2
```

**提示:**

+ 1 <= nums.length <= 2 * 104
+ -1000 <= nums[i] <= 1000
+ -107 <= k <= 107

 

注意：本题与主站 560 题相同： https://leetcode-cn.com/problems/subarray-sum-equals-k/

# 思路

**总体思路：**

+ 暴力解法（枚举）
+ 优化方法：哈希表 + 前缀和

**过程：**    
本题的暴力解法，倒是不用多说，比较常规。   
本题的优化解法，还是比较有意思的。这道题**哈希表**存储的是**前缀和**。这也是我第一次遇见这种类型的题。


# 代码  
java实现：   
```
class Solution {
    public int subarraySum(int[] nums, int k) {
        // return normal(nums, k);

        return hashPreSum(nums, k);
    }

    // 暴力解法：枚举
    // 时间复杂度： O(n2)
    public int normal (int[] nums, int k) {
        int len = nums.length;
        int res = 0;
        for (int i = 0; i < len; i++) {
            int sum = 0;
            for (int j = i; j < len; j++) {
                sum += nums[j];
                if (sum == k) {
                    res++;
                }
            }
        }
        return res;
    }

    // 哈希表 + 前缀和
    // 时间复杂度: O(n)
    public int hashPreSum(int[] nums, int k) {
        Map<Integer, Integer> map = new HashMap<Integer, Integer>();
        int len = nums.length;
        int res = 0;
        // 记录第i位的前缀和
        int sum = 0;
        map.put(0, 1);
        for (int i = 0; i < len; i++) {
            sum += nums[i];
            res += map.getOrDefault(sum - k, 0);
            map.put(sum, map.getOrDefault(sum, 0) + 1);
        }
        return res;
    }
}
```
python实现：   
```
class Solution:
    def subarraySum(self, nums: List[int], k: int) -> int:
        mp = {}
        N = len(nums)
        res = 0
        
        count = 0
        mp[0] = 1
        for num in nums:
            count += num
            res += mp.get(count - k, 0)
            mp[count] = mp.get(count, 0) + 1
        return res
```
# 其他

记录本题的原因是，本题的优化方法使用的是，哈希表进行前缀和的存储。
