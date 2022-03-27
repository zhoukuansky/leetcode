# 剑指 Offer II 057. 值和下标之差都在给定的范围内
难度：中等   
题目地址：https://leetcode-cn.com/problems/7WqeDu/   
完成时间：  2022/3/27   
# 题目

给你一个整数数组 nums 和两个整数 k 和 t 。请你判断是否存在 两个不同下标 i 和 j，使得 abs(nums[i] - nums[j]) <= t ，同时又满足 abs(i - j) <= k 。

如果存在则返回 true，不存在返回 false。

 

**示例 1：**
```
输入：nums = [1,2,3,1], k = 3, t = 0
输出：true
```
**示例 2：**
```
输入：nums = [1,0,1,1], k = 1, t = 2
输出：true
```
**示例 3：**
```
输入：nums = [1,5,9,1,5,9], k = 2, t = 3
输出：false
```

**提示：**

+ 0 <= nums.length <= 2 * 104
+ -231 <= nums[i] <= 231 - 1
+ 0 <= k <= 104
+ 0 <= t <= 231 - 1
 

注意：本题与主站 220 题相同： https://leetcode-cn.com/problems/contains-duplicate-iii/

# 思路
本题是题目[]()的前置题目。其力扣网址：

**总体思路：**
+ 有序集合 + 滑动窗口
+ 优化：桶计数 + 滑动窗口（本质是将有序集合换为哈希字典减少时间复杂度）

**过程：**    

过程请详看代码

# 代码  
java实现：   
```
class Solution {
    // 有序集合 + 滑动窗口
    public boolean containsNearbyAlmostDuplicate(int[] nums, int k, int t) {
        // 这里必须用long型，否则越界
        TreeSet<Long> set = new TreeSet<Long>();
        int len = nums.length;
        for (int i = 0; i < len; i++) {
            // 判断滑动窗口中是否存在某个数 x 落在区间 [nums[i] - t, nums[i] + t]中
            Long x = set.ceiling((long)nums[i] - (long)t);
            // 若存在，则说明有两个元素满足题目条件
            if (x != null && x <= (long)nums[i] + (long)t) {
                return true;
            }
            set.add((long)nums[i]);
            if (i >= k) {
                set.remove((long)nums[i - k]);
            }
        }
        return false;
    }
}
```
python实现：   
```

```
# 其他



