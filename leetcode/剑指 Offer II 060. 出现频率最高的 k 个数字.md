# 剑指 Offer II 060. 出现频率最高的 k 个数字
难度：中等   
题目地址：https://leetcode-cn.com/problems/g5c51o/   
完成时间：  2022/3/28   
# 题目

给定一个整数数组 nums 和一个整数 k ，请返回其中出现频率前 k 高的元素。可以按 任意顺序 返回答案。

 

**示例 1:**
```
输入: nums = [1,1,1,2,2,3], k = 2
输出: [1,2]
```
**示例 2:**
```
输入: nums = [1], k = 1
输出: [1]
```

**提示：**

+ 1 <= nums.length <= 105
+ k 的取值范围是 [1, 数组中不相同的元素的个数]
+ 题目数据保证答案唯一，换句话说，数组中前 k 个高频元素的集合是唯一的
 

进阶：所设计算法的时间复杂度 必须 优于 O(n log n) ，其中 n 是数组大小。

 

注意：本题与主站 347 题相同：https://leetcode-cn.com/problems/top-k-frequent-elements/


# 思路

**总体思路：**

+ 小顶堆 + 哈希字典

**过程：**  

见代码

# 代码  
java实现：   
```
class Solution {
    // 小顶堆 + 哈希字典
    public int[] topKFrequent(int[] nums, int k) {
        int len = nums.length;
        Map<Integer, Integer> map = new HashMap<Integer, Integer>();
        for (int x : nums) {
            map.put(x, map.getOrDefault(x, 0) + 1);
        }
        // int[] 的第一个元素代表数组的值，第二个元素代表了该值出现的次数
        PriorityQueue<int[]> pq = new PriorityQueue<int[]>((int[] a, int[] b) -> {
            return a[1] - b[1];
        });
        // 遍历字典
        for (Map.Entry<Integer, Integer> entry : map.entrySet()) {
            int key = entry.getKey();
            int val = entry.getValue();
            if (pq.size() == k) {
                if (pq.peek()[1] < val) {
                    pq.poll();
                    pq.offer(new int[]{key, val});
                }
            } else {
                pq.offer(new int[]{key, val});
            }
        }
        int[] res = new int[k];
        for (int i = 0; i < k; i++) {
            res[i] = pq.poll()[0];
        }
        return res;
    }
}
```
python实现：   
```

```
# 其他


关于java 的 PriorityQueue，它有一个容量的概念。
>如果初始化，不设置容量，源码会填充默认值，即11。

关于达到容量上限后的，扩容操作：

>当容量小于64时，库容为原来的两倍加2，否则扩容为原来的1.5倍
