# 剑指 Offer II 022. 链表中环的入口节点
难度：中等   
题目地址：https://leetcode-cn.com/problems/c32eOV/   
完成时间：  2022/3/   
# 题目
给定一个链表，返回链表开始入环的第一个节点。 从链表的头节点开始沿着 next 指针进入环的第一个节点为环的入口节点。如果链表无环，则返回 null。

为了表示给定链表中的环，我们使用整数 pos 来表示链表尾连接到链表中的位置（索引从 0 开始）。 如果 pos 是 -1，则在该链表中没有环。注意，pos 仅仅是用于标识环的情况，并不会作为参数传递到函数中。

说明：不允许修改给定的链表。

**示例 1：**
```
输入：head = [3,2,0,-4], pos = 1
输出：返回索引为 1 的链表节点
解释：链表中有一个环，其尾部连接到第二个节点。
```
**示例 2：**
```
输入：head = [1,2], pos = 0
输出：返回索引为 0 的链表节点
解释：链表中有一个环，其尾部连接到第一个节点。
```
**示例 3：**
```
输入：head = [1], pos = -1
输出：返回 null
解释：链表中没有环。
```
**提示：**

+ 链表中节点的数目范围在范围 [0, 104] 内
+ -105 <= Node.val <= 105
+ pos 的值为 -1 或者链表中的一个有效索引

进阶：是否可以使用 O(1) 空间解决此题？ 

注意：本题与主站 142 题相同： https://leetcode-cn.com/problems/linked-list-cycle-ii/

# 思路

**总体思路：**

+ 哈希表
+ 快慢指针（龟兔赛跑）解法：Floyd 判圈算法

**过程：**    

快慢指针的（龟兔赛跑）解法是比较有意思的。主要参考：https://leetcode-cn.com/problems/linked-list-cycle-ii/solution/huan-xing-lian-biao-ii-by-leetcode-solution/

其里面的核心观点是：  
>规律：当发现slow与fast相遇时，我们再额外使用一个指针res。起始，它指向链表头部；随后，它和slow 每次向后移动一个位置。最终，它们会在入环点相遇。

# 代码  
java实现：   
```
/**
 * Definition for singly-linked list.
 * class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
    public ListNode detectCycle(ListNode head) {
        return floyd(head);
        // return hash(head);
    }

    //快慢指针（龟兔赛跑）解法：Floyd 判圈算法
    public ListNode floyd(ListNode head){
        ListNode slow = head;
        ListNode fast = head;
        ListNode res = head;
        while(fast != null){
            if(fast.next == null){
                return null;
            }
            slow = slow.next;
            fast = fast.next.next;
            // 规律：当发现slow与fast相遇时，我们再额外使用一个指针res。起始，它指向链表头部；随后，它和slow 每次向后移动一个位置。最终，它们会在入环点相遇。
            // 参考：https://leetcode-cn.com/problems/linked-list-cycle-ii/solution/huan-xing-lian-biao-ii-by-leetcode-solution/
            if(slow == fast){
                while(res != slow){
                    res = res.next;
                    slow = slow.next;
                }
                return res;
            }
        }
        return null;
    }

    //哈希表解法
    public ListNode hash(ListNode head){
        Set<ListNode> set = new HashSet<ListNode>();
        while(head != null){
            if(!set.add(head)){
                return head;
            }
            head = head.next;
        }
        return null;
    }
}
```
python实现：   
```

```
# 其他



