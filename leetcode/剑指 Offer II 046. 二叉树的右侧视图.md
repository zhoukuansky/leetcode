# 剑指 Offer II 046. 二叉树的右侧视图
难度：中等   
题目地址：https://leetcode-cn.com/problems/WNC0Lk/   
完成时间：  2022/3/22   
# 题目

给定一个二叉树的 根节点 root，想象自己站在它的右侧，按照从顶部到底部的顺序，返回从右侧所能看到的节点值。

**示例 1:**
```
输入: [1,2,3,null,5,null,4]
输出: [1,3,4]
```
**示例 2:**
```
输入: [1,null,3]
输出: [1,3]
```
**示例 3:**
```
输入: []
输出: []
```

**提示:**

+ 二叉树的节点个数的范围是 [0,100]
+ -100 <= Node.val <= 100 
 

注意：本题与主站 199 题相同：https://leetcode-cn.com/problems/binary-tree-right-side-view/


# 思路

**总体思路：**

+ 迭代(层序遍历) / 递归

**过程：**    

详细过程，请看代码实现

# 代码  
java实现：   
```
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode() {}
 *     TreeNode(int val) { this.val = val; }
 *     TreeNode(int val, TreeNode left, TreeNode right) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
class Solution {
    List<Integer> res = new ArrayList<Integer>();
    public List<Integer> rightSideView(TreeNode root) {
        if (root == null) {
            return res;
        }

        dfs(root, 0);

        //iteration(root);
        return res;
    }

    // 迭代(层序遍历)
    public void iteration(TreeNode root) {
        Queue<TreeNode> que = new LinkedList<TreeNode>();
        que.offer(root);
        while (!que.isEmpty()) {
            int size = que.size();
            for (int i = 0; i < size; i++) {
                TreeNode node = que.poll();
                if (i == size - 1) {
                    res.add(node.val);
                }
                if (node.left != null) {
                    que.offer(node.left);
                }
                if (node.right != null) {
                    que.offer(node.right);
                }
            }
        }
    }

    // 递归
    public void dfs(TreeNode root, int depth) {
        if (root == null) {
            return;
        }
        if (depth == res.size()) {
            res.add(root.val);
        }
        // 由于是右视图，所以先右节点，后左节点
        dfs(root.right, depth + 1);
        dfs(root.left, depth + 1);
    }
}
```
python实现：   
```

```
# 其他



