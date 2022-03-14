# 剑指 Offer II 020. 回文子字符串的个数
难度：中等   
题目地址：https://leetcode-cn.com/a7VOhD/   
完成时间：  2022/3/14   
# 题目
给定一个字符串 s ，请计算这个字符串中有多少个回文子字符串。

具有不同开始位置或结束位置的子串，即使是由相同的字符组成，也会被视作不同的子串。

 

**示例 1：**
```
输入：s = "abc"
输出：3
解释：三个回文子串: "a", "b", "c"
```
**示例 2：**
```
输入：s = "aaa"
输出：6
解释：6个回文子串: "a", "a", "a", "aa", "aa", "aaa"
```

**提示：**

+ 1 <= s.length <= 1000
+ s 由小写英文字母组成
 

注意：本题与主站 647 题相同：https://leetcode-cn.com/problems/palindromic-substrings/ 


# 思路

**总体思路：**

+ 动态规划
+ 中心扩散（实质是双指针）
+ 马拉车算法（参考：https://zhuanlan.zhihu.com/p/70532099）

总时间效率：马拉车 > 中心扩散 > 动态规划

**过程：**    

本题目前只实现了前两者，前两者的时间复杂度都是O(n2)，而马拉车算法时间复杂度O(n)。

# 代码  
java实现：   
```
class Solution {
    int res = 0;
    int len;
    // 总时间效率：马拉车 > 中心扩散 > 动态规划
    public int countSubstrings(String s) {
        len = s.length();
        
        // return centerAlgorithm(s);

        return ddpp(s);
    }

    // 动态规划
    public int ddpp(String s) {
        // dp[i][j] 表示从字符串从i到j构成的子串
        boolean[][] dp = new boolean[len][len];
        for (int j = 0; j < len; j++) {
            for (int i = 0; i <= j; i++) {
                if (s.charAt(i) == s.charAt(j) && (j - i <= 1 || dp[i + 1][j - 1])) {
                    dp[i][j] = true;
                    res++;
                }
            }
        }
        return res;
    }

    // 中心扩展算法（本质双指针）
    public int centerAlgorithm(String s) {
        for (int i = 0; i < len; i++) {
            twoPair(s, i, i);
            if (i < len - 1) {
                if (s.charAt(i) == s.charAt(i + 1)) {
                    twoPair(s, i, i + 1);
                }
            }
        }
        return res;
    }
    public void twoPair(String s, int left, int right) {
        while (left >= 0 && right < s.length() && s.charAt(left) == s.charAt(right)) {
            res++;
            left--;
            right++;
        }
    }
}
```
python实现：   
```

```
# 其他



