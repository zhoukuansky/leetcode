# 剑指 Offer II 003. 前 n 个数字二进制中 1 的个数
难度：简单       
题目地址：https://leetcode-cn.com/problems/w3tCBm/        
完成时间：  2022/3/7   
# 题目
给定一个非负整数 n ，请计算 0 到 n 之间的每个数字的二进制表示中 1 的个数，并输出一个数组。

**示例 1:**
```
输入: n = 2
输出: [0,1,1]
解释: 
0 --> 0
1 --> 1
2 --> 10
```
**示例 2:**
```
输入: n = 5
输出: [0,1,1,2,1,2]
解释:
0 --> 0
1 --> 1
2 --> 10
3 --> 11
4 --> 100
5 --> 101
```

**说明 :**

+ 0 <= n <= 105
 

进阶:

+ 给出时间复杂度为 O(n*sizeof(integer)) 的解答非常容易。但你可以在线性时间 O(n) 内用一趟扫描做到吗？
+ 要求算法的空间复杂度为 O(n) 。
+ 你能进一步完善解法吗？要求在C++或任何其他语言中不使用任何内置函数（如 C++ 中的 __builtin_popcount ）来执行此操作。

注意：本题与主站 338 题相同：https://leetcode-cn.com/problems/counting-bits/

# 思路

**总体思路：**
位运算 + 动规（优化）。


**过程：**      

+ 本题重要的是Brian Kernighan 算法。其核心为:  
    +  x = x & (x−1)，该运算将 x 的二进制表示的最后一个 1 变成 0。  
+ 位运算是本题基础。  
+ 动规加以优化。

# 代码  
java实现：   
```java
class Solution {
    public int[] countBits(int n) {
        //return countBrian(n);
        //return countHighBit(n);
        //return countLowBit(n);
        return countSetBit(n);
    }

    // Brian Kernighan 算法
    // 时间复杂度：O(nlogn)
    public int[] countBrian(int n) {
        int[] res = new int[n + 1];
        for (int i = 1; i <= n; i++) {
            int k = i, count = 0;
            while (k > 0) {
            // Brian Kernighan 算法核心
            // x = x & (x−1)，该运算将 x 的二进制表示的最后一个 1 变成 0
                k &= k - 1;
                count++;
            }
            res[i] = count;
        }
        return res;
    }

    // 动态规划——最高有效位：本题中使用highBit记录上一个最高有效位的位置（最高有效位指的是2的幂所在位置）
    // 时间复杂度：O(n)
    public int[] countHighBit(int n) {
        int[] res = new int[n + 1];
        int highBit = 0;
        for (int i = 1; i <= n; i++) {
            if ((i & (i - 1)) == 0) {
                highBit = i;
            }
            res[i] = res[i - highBit] + 1;
        }
        return res;
    }

    // 动态规划——最低有效位：bits[x] 的值等于bit[x / 2]的值加上 xx 除以 2 的余数
    // 如果 xx 是偶数，则 bits[x]=bits[x/2]
    // 如果 xx 是偶数，则 bits[x]=bits[x/2]+1
    // 时间复杂度：O(n)
    public int[] countLowBit(int n) {
        int[] res = new int[n + 1];
        for (int i = 1; i <= n; i++) {
            res[i] = res[i / 2] + (i & 1);
        }
        return res;
    }

    // 动态规划——最低设置位（原理）：x = x & (x−1)，该运算将 x 的二进制表示的最后一个 1 变成 0
    // 时间复杂度：O(n)
    public int[] countSetBit(int n) {
        int[] res = new int[n + 1];
        for (int i = 1; i <= n; i++) {
            res[i] = res[i & (i - 1)] + 1;
        }
        return res;
    }
}
```
python实现：   
```

```
# 其他



