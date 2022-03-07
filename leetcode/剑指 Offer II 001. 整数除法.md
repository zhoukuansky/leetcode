# 剑指 Offer II 001. 整数除法
难度：   中等   
题目地址：https://leetcode-cn.com/problems/xoh6Oh/   
完成时间：  2022/2/26   
# 题目
剑指 Offer II 001. 整数除法
给定两个整数 a 和 b ，求它们的除法的商 a/b ，要求不得使用乘号 '*'、除号 '/' 以及求余符号 '%' 。


**注意：**

+ 整数除法的结果应当截去（truncate）其小数部分，例如：truncate(8.345) = 8 以及 truncate(-2.7335) = -2
+ 假设我们的环境只能存储 32 位有符号整数，其数值范围是 [−2(31), 2(31)−1]。本题中，如果除法结果溢出，则返回 2(31) − 1
 

**示例 1：**
```
输入：a = 15, b = 2
输出：7
解释：15/2 = truncate(7.5) = 7
```
**示例 2：**
```
输入：a = 7, b = -3
输出：-2
解释：7/-3 = truncate(-2.33333..) = -2
```
**示例 3：**
```
输入：a = 0, b = 1
输出：0
```
**示例 4：**
```
输入：a = 1, b = 1
输出：1
```

**提示:**

+ -231 <= a, b <= 231 - 1
+ b != 0
 

注意：本题与主站 29 题相同：https://leetcode-cn.com/problems/divide-two-integers/

# 思路
本题是题目[]()的前置题目。其力扣网址：

**总体思路：**  
本题仍然是**位运算**的相关操作。  
本题的解法本质就是减法代替除法，然后引出了快速加法的优化。所以，本题有以下解法：  

+ 减法代替除法   
   时间复杂度： O(n)
+ 优化一：快速乘法  
    时间复杂度： O(logn*logn)
+ 优化二：位运算优化   
    时间复杂度： O(1)

**过程：**    
主要参考：   
https://leetcode-cn.com/problems/xoh6Oh/solution/jian-dan-yi-dong-javac-pythonjs-zheng-sh-e8r6/   

顺带需要查看题目[50.Pow(x, n)](https://leetcode-cn.com/problems/powx-n/)

# 代码  
java实现：   
```
class Solution {
    public int divide(int a, int b) {
        //return sub(a, b);

        //return optimization(a, b);

        return optimizationBit(a, b);
    }

    // 减法代替除法
    // 时间复杂度 O(n)
    public int sub (int a, int b) {
        int res = 0;
        if (a == Integer.MIN_VALUE && b == -1) {
            return Integer.MAX_VALUE;
        }
        // 符号 ^ 是异或
        int sign = (a > 0) ^ (b > 0) ? -1 : 1;
        a = -Math.abs(a);
        b = -Math.abs(b);
        while (a <= b) {
            a -= b;
            res++;
        }
        // 不能出现乘法
        return sign == 1 ? res : -res;
    }

    // 优化一：快速乘法
    // 时间复杂度 logn*logn 
    public int optimization (int a, int b) {
        int res = 0;
        if (a == Integer.MIN_VALUE && b == -1) {
            return Integer.MAX_VALUE;
        }
        // 如果不要这个 后续的res += k有越界的可能
        if (a == Integer.MIN_VALUE && b == 1) {
            return Integer.MIN_VALUE;
        }
        // 符号 ^ 是异或
        int sign = (a > 0) ^ (b > 0) ? -1 : 1;
        a = -Math.abs(a);
        b = -Math.abs(b);
        
        while (a <= b) {
            int value = b;
            int k = 1;
            // 0xc0000000 是十进制 -2^30 的十六进制的表示
            // 而 a 的值不可能比 -2^31 还要小，所以 value 不可能比 0xc0000000 小
            while (value >= 0xc0000000  && a <= value + value) {
                value += value;
                k += k;
            }
            a -= value;
            res += k;
        }
        // 不能出现乘法
        return sign == 1 ? res : -res;
    }

    // 优化二：位运算优化
    // 时间复杂度 O(1)
    public int optimizationBit (int a, int b) {
        int res = 0;
        if (a == Integer.MIN_VALUE && b == -1) {
            return Integer.MAX_VALUE;
        }
        // 如果不要这个 后续的res += k有越界的可能
        if (a == Integer.MIN_VALUE && b == 1) {
            return Integer.MIN_VALUE;
        }
        // 符号 ^ 是异或
        int sign = (a > 0) ^ (b > 0) ? -1 : 1;
        a = Math.abs(a);
        b = Math.abs(b);
        for (int i = 31; i >= 0; i--) {
            // 注意，这里不能是 (a >>> i) >= b 而应该是 (a >>> i) - b >= 0
            if ((a >>> i) - b >= 0) {
                a -= (b << i);
                res += (1 << i);
            }
        }
        // 不能出现乘法
        return sign == 1 ? res : -res;
    }
}
```
python实现：   
```

```
# 其他


