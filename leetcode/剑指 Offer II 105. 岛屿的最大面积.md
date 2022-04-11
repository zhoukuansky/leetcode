# 剑指 Offer II 105. 岛屿的最大面积
难度：中等   
题目地址：https://leetcode-cn.com/   
完成时间：  2022/4/   
# 题目
给定一个由 0 和 1 组成的非空二维数组 grid ，用来表示海洋岛屿地图。

一个 岛屿 是由一些相邻的 1 (代表土地) 构成的组合，这里的「相邻」要求两个 1 必须在水平或者竖直方向上相邻。你可以假设 grid 的四个边缘都被 0（代表水）包围着。

找到给定的二维数组中最大的岛屿面积。如果没有岛屿，则返回面积为 0 。

 

**示例 1:**

![1](https://pic.leetcode-cn.com/1626667010-nSGPXz-image.png)
```
输入: grid = [[0,0,1,0,0,0,0,1,0,0,0,0,0],[0,0,0,0,0,0,0,1,1,1,0,0,0],[0,1,1,0,1,0,0,0,0,0,0,0,0],[0,1,0,0,1,1,0,0,1,0,1,0,0],[0,1,0,0,1,1,0,0,1,1,1,0,0],[0,0,0,0,0,0,0,0,0,0,1,0,0],[0,0,0,0,0,0,0,1,1,1,0,0,0],[0,0,0,0,0,0,0,1,1,0,0,0,0]]
输出: 6
解释: 对于上面这个给定矩阵应返回 6。注意答案不应该是 11 ，因为岛屿只能包含水平或垂直的四个方向的 1 。
```
**示例 2:**
```
输入: grid = [[0,0,0,0,0,0,0,0]]
输出: 0
```

**提示：**

+ m == grid.length
+ n == grid[i].length
+ 1 <= m, n <= 50
+ grid[i][j] is either 0 or 1
 

注意：本题与主站 695 题相同： https://leetcode-cn.com/problems/max-area-of-island/


# 思路
本题是题目[]()的前置题目。其力扣网址：

**总体思路：**

+ 深度优先搜索（递归 / 堆栈）
+ 广度优先搜索（队列）

**过程：**    

过程看代码即可。

# 代码  
java实现：   
```
class Solution {
    public int maxAreaOfIsland(int[][] grid) {
        int m = grid.length;
        int n = grid[0].length;

        // 深搜
        int res = 0;
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                int s = dfs(grid, i, j, m, n);
                res = Math.max(res, s);
            }
        }
        return res;

        // 广搜
        // return bfs(grid, m, n);
    }
    
    // 递归深搜
    public int dfs(int[][] grid, int i, int j, int m, int n) {
        if (i < 0 || j < 0 || i >= m || j >= n || grid[i][j] == 0) {
            return 0;
        }
        grid[i][j] = 0;
        int[] dx = {-1, 1, 0, 0};
        int[] dy = {0, 0, -1, 1};
        int res = 1;
        for (int k = 0; k < 4; k++) {
            res += dfs(grid, i + dx[k], j + dy[k], m, n);
        }
        return res;
    }

    // 广度优先搜索（队列实现）
    public int bfs(int[][] grid, int m, int n) {
        int res = 0;
        int[] dx = {-1, 1, 0, 0};
        int[] dy = {0, 0, -1, 1};
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                int now = 0;
                Queue<int[]> que = new LinkedList<int[]>();
                if (grid[i][j] == 0) {
                    continue;
                }
                que.offer(new int[]{i, j});
                while (!que.isEmpty()) {
                    int[] arr = que.poll();
                    int x = arr[0];
                    int y = arr[1];
                    if (x < 0 || y < 0 || x >= m || y >= n || grid[x][y] == 0) {
                        continue;
                    }
                    grid[x][y] = 0;
                    now++;
                    for (int k = 0; k < 4; k++) {
                        que.offer(new int[]{x + dx[k], y + dy[k]});
                    }
                }
                res = Math.max(res, now);
            }
        }
        return res;
    }
}
```
python实现：   
```

```
# 其他



