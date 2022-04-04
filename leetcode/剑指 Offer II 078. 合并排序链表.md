# 剑指 Offer II 078. 合并排序链表
难度：困难   
题目地址：https://leetcode-cn.com/problems/vvXgSW/   
完成时间：  2022/4/4   
# 题目
给定一个链表数组，每个链表都已经按升序排列。

请将所有链表合并到一个升序链表中，返回合并后的链表。

 
**示例 1：**
```
输入：lists = [[1,4,5],[1,3,4],[2,6]]
输出：[1,1,2,3,4,4,5,6]
解释：链表数组如下：
[
  1->4->5,
  1->3->4,
  2->6
]
将它们合并到一个有序链表中得到。
1->1->2->3->4->4->5->6
```
**示例 2：**
```
输入：lists = []
输出：[]
```
**示例 3：**
```
输入：lists = [[]]
输出：[]
```
 

**提示：**

+ k == lists.length
+ 0 <= k <= 10^4
+ 0 <= lists[i].length <= 500
+ -10^4 <= lists[i][j] <= 10^4
+ lists[i] 按 升序 排列
+ lists[i].length 的总和不超过 10^4
 

注意：本题与主站 23 题相同： https://leetcode-cn.com/problems/merge-k-sorted-lists/

# 思路

**总体思路：**
+ 小顶堆（优先队列）

**过程：**   
具体实现，可参见代码。 

# 代码  
java实现：   
```
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    // 小顶堆
    public ListNode mergeKLists(ListNode[] lists) {
        int len = lists.length;
        // 按照元素val从小到大排序
        PriorityQueue<ListNode> pq = new PriorityQueue<ListNode>(len + 1, (ListNode l1, ListNode l2) -> {
            return l1.val - l2.val;
        });
        // 将lists数组的每个元素入队
        for (ListNode x : lists) {
            if (x != null) {
                pq.offer(x);
            }
        }

        ListNode res = new ListNode();
        ListNode node = res;
        while (!pq.isEmpty()) {
            ListNode now = pq.poll();
            node.next = now;
            node = node.next;
            if (now.next != null) {
                pq.offer(now.next);
            }
        }
        return res.next;
    }
}
```
python实现：   
```

```
# 其他



