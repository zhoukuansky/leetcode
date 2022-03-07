# 剑指 Offer II 004. 只出现一次的数字 
难度：中等   
题目地址：https://leetcode-cn.com/problems/WGki4K/   
完成时间：  2022/3/7   
# 题目
剑指 Offer II 004. 只出现一次的数字 
给你一个整数数组 nums ，除某个元素仅出现 一次 外，其余每个元素都恰出现 三次 。请你找出并返回那个只出现了一次的元素。

 

**示例 1：**
```
输入：nums = [2,2,3,2]
输出：3
```
**示例 2：**
```
输入：nums = [0,1,0,1,0,1,100]
输出：100
```

**提示：**

+ 1 <= nums.length <= 3 * 104
+ -231 <= nums[i] <= 231 - 1
+ nums 中，除某个元素仅出现 一次 外，其余每个元素都恰出现 三次
 

进阶：你的算法应该具有线性时间复杂度。 你可以不使用额外空间来实现吗？

注意：本题与主站 137 题相同：https://leetcode-cn.com/problems/single-number-ii/

# 思路

**总体思路：**

哈希表 / 数字电路设计（位运算）

**过程：**    

本题的方法二中的位运算需要进行数字电路的推演，需注意。

# 代码  
java实现：   
```
class Solution {
    public int singleNumber(int[] nums) {
        // 哈希表
        // Map<Integer, Integer> map = new HashMap<Integer, Integer>();
        // for (int num : nums) {
        //     map.put(num, map.getOrDefault(num, 0) + 1);
        // }

        // int res = 0;
        // for (Map.Entry<Integer, Integer> entry : map.entrySet()) {
        //     int num = entry.getKey();
        //     int value = entry.getValue();
        //     if (value == 1) {
        //         res = num;
        //         break;
        //     }
        // }
        // return res;

        // 数字电路设计
        int a = 0, b = 0;
        for (int num : nums)
        {
            a = (a ^ num) & ~b;
            b = (b ^ num) & ~a;
        }
        return a;
    }
}
```
python实现：   
```
class Solution:
    def singleNumber(self, nums: List[int]) -> int:
        # 哈希表
        # mp = collections.Counter(nums)
        # res = 0
        # for  key, value in mp.items():
        #     if value == 1:
        #         res = key
        #         break
        # return res

        # 数字电路设计
        a, b = 0, 0
        for num in nums:
            a = (a ^ num) & ~b
            b = (b ^ num) & ~a
        return a
```
# 其他

记录本题的原因是，数字电路设计本科学过，现在忘得差不多了。哈哈哈......

