# 剑指 Offer II 008. 和大于等于 target 的最短子数组
难度：中等   
题目地址：https://leetcode-cn.com/problems/2VG8Kg/   
完成时间：  2022/3/7   
# 题目
剑指 Offer II 008. 和大于等于 target 的最短子数组
给定一个含有 n 个正整数的数组和一个正整数 target 。

找出该数组中满足其和 ≥ target 的长度最小的 连续子数组 [numsl, numsl+1, ..., numsr-1, numsr] ，并返回其长度。如果不存在符合条件的子数组，返回 0 。

 

**示例 1：**
```
输入：target = 7, nums = [2,3,1,2,4,3]
输出：2
解释：子数组 [4,3] 是该条件下的长度最小的子数组。
```
**示例 2：**
```
输入：target = 4, nums = [1,4,4]
输出：1
```
**示例 3：**
```
输入：target = 11, nums = [1,1,1,1,1,1,1,1]
输出：0
```

**提示：**

+ 1 <= target <= 109
+ 1 <= nums.length <= 105
+ 1 <= nums[i] <= 105
 

**进阶：**

如果你已经实现 O(n) 时间复杂度的解法, 请尝试设计一个 O(n log(n)) 时间复杂度的解法。
 

注意：本题与主站 209 题相同：https://leetcode-cn.com/problems/minimum-size-subarray-sum/

# 思路
本题是题目[]()的前置题目。其力扣网址：

**总体思路：**

+ 前缀和（相当于暴力解法）
+ 滑动窗口

**过程：**

本题的滑动窗口，需要注意下，最好使用这种格式。   
如果使用，sum < target 作为判断条件的话，会导致right提前达到终止条件。结果错误。

# 代码  
java实现：   
```
class Solution {
    public int minSubArrayLen(int target, int[] nums) {
        //return sum(target, nums);
        return windows(target, nums);
    }

    // 滑动窗口
    // 时间复杂度：O(n)
    public int windows(int target, int[] nums) {
        int len = nums.length;
        int res = 100001;
        int left = 0, right = 0;
        int sum = 0;
        while (right < len) {
            sum += nums[right];
            while (sum >= target) {
                res = Math.min(res, right - left + 1);
                sum -= nums[left];
                left++;
            }
            right++;
        }
        return res == 100001 ? 0 : res;
    }

    
    // 前缀和（和暴力法时间复杂度相同）
    // 时间复杂度：O(n2)
    public int sum(int target, int[] nums) {
        int len = nums.length;
        int res = 100001;
        int[] pos = new int[len + 1];
        for (int i = 1; i <= len; i++) {
            pos[i] = pos[i - 1] + nums[i - 1];
        }
        for (int i = 0; i <= len; i++) {
            for (int j = i + 1; j <= len; j++) {
                int sum = pos[j] - pos[i];
                if (sum >= target) {
                    res = Math.min(res, j - i);
                    break;
                }
            }
        }
        return res == 100001 ? 0 : res;
    }
}
```
python实现：   
```

```
# 其他



