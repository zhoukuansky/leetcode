# 剑指 Offer II 084. 含有重复元素集合的全排列 
难度：中等   
题目地址：https://leetcode-cn.com/problems/7p8L0Z/   
完成时间：  2022/4/5   
# 题目

给定一个可包含重复数字的整数集合 nums ，按任意顺序 返回它所有不重复的全排列。


**示例 1：**
```
输入：nums = [1,1,2]
输出：
[[1,1,2],
 [1,2,1],
 [2,1,1]]
```
**示例 2：**
```
输入：nums = [1,2,3]
输出：[[1,2,3],[1,3,2],[2,1,3],[2,3,1],[3,1,2],[3,2,1]]
```

**提示：**

+ 1 <= nums.length <= 8
+ -10 <= nums[i] <= 10

注意：本题与主站 47 题相同： https://leetcode-cn.com/problems/permutations-ii/


# 思路

[39. 组合总和](https://leetcode-cn.com/problems/combination-sum/)

[40. 组合总和 II](https://leetcode-cn.com/problems/combination-sum-ii/)

[46. 全排列](https://leetcode-cn.com/problems/permutations/)

[47. 全排列 II](https://leetcode-cn.com/problems/permutations-ii/)

这里都是递归回溯剪枝相关的题目，依次紧进阶。

**总体思路：**

+ 递归回溯剪枝

**过程：**    

值得注意的是，递归回溯剪枝：要把递归回溯算法（特别内部有for的结构），看成是树的来理解，不然很难理解。

# 代码  
java实现：   
```
class Solution {
    List<List<Integer>> res = new ArrayList<List<Integer>>();
    List<Integer> tt = new ArrayList<Integer>();
    // 记录某元素是否被使用过
    boolean [] visited;
    public List<List<Integer>> permuteUnique(int[] nums) {
        Arrays.sort(nums);
        visited = new boolean[nums.length];
        dfs(nums);
        return res;
    }

    // 递归回溯剪枝：要把递归回溯算法（特别内部有for的结构），看成是树的来理解，不然很难理解
    public void dfs(int[] nums) {
        if (tt.size() == nums.length) {
            res.add(new ArrayList<Integer>(tt));
            return;
        }
        for (int i = 0; i < nums.length; i++) {
            //（在上一题的基础上）在深搜回溯的基础上，对nums进行了排序。再设置下列条件，就能很好的防止重复
            if (i > 0 && nums[i] == nums[i - 1] && visited[i - 1]) {
                continue;
            }
            // 剪枝：元素重复
            if (visited[i]) {
                continue;
            }
            tt.add(nums[i]);
            visited[i] = true;
            dfs(nums);
            // 回溯
            tt.remove(tt.size() - 1);
            visited[i] = false;
        }
    }
}
```
python实现：   
```

```
# 其他



