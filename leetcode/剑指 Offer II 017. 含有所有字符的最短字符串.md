# 剑指 Offer II 017. 含有所有字符的最短字符串
难度：困难   
题目地址：https://leetcode-cn.com/problems/M1oyTv/   
完成时间：  2022/3/11
# 题目

给定两个字符串 s 和 t 。返回 s 中包含 t 的所有字符的最短子字符串。如果 s 中不存在符合条件的子字符串，则返回空字符串 "" 。

如果 s 中存在多个符合条件的子字符串，返回任意一个。

**注意：** 对于 t 中重复字符，我们寻找的子字符串中该字符数量必须不少于 t 中该字符数量。

**示例 1：**
```
输入：s = "ADOBECODEBANC", t = "ABC"
输出："BANC" 
解释：最短子字符串 "BANC" 包含了字符串 t 的所有字符 'A'、'B'、'C'
```
**示例 2：**
```
输入：s = "a", t = "a"
输出："a"
```
**示例 3：**
```
输入：s = "a", t = "aa"
输出：""
解释：t 中两个字符 'a' 均应包含在 s 的子串中，因此没有符合条件的子字符串，返回空字符串。
```

**提示：**
+ 1 <= s.length, t.length <= 105
+ s 和 t 由英文字母组成

进阶：你能设计一个在 o(n) 时间内解决此问题的算法吗？


注意：本题与主站 76 题相似（本题答案不唯一）：https://leetcode-cn.com/problems/minimum-window-substring/

# 思路

**总体思路：**

桶计数 + 滑动窗口

**过程：**    

原理请参考：https://leetcode-cn.com/problems/minimum-window-substring/solution/tong-su-qie-xiang-xi-de-miao-shu-hua-dong-chuang-k/

过程详见代码，即可。


# 代码  
java实现：   
```
class Solution {
    // 桶计数 + 滑动窗口
    // 原理请看：https://leetcode-cn.com/problems/minimum-window-substring/solution/tong-su-qie-xiang-xi-de-miao-shu-hua-dong-chuang-k/
    public String minWindow(String s, String t) {
        int sLen = s.length();
        int tLen = t.length();

        // res 用于记录最小满足条件滑窗起始值
        int minSize = Integer.MAX_VALUE, res = 0;
        // ASCII码共计128个字符
        int[] need = new int[128];
        for (int i = 0; i < tLen; i++) {
            need[t.charAt(i)]++;
        }
        int left = 0;
        // 用于记录滑窗中和目标字符串的差别
        int count = tLen;
        // 这里也可以使用while，只是把此处的i设置成了变量right
        for (int i = 0; i < sLen; i++) {
            char ch = s.charAt(i);
            if (need[ch] > 0) {
                count--;
            }
            need[ch]--;

            // 每当滑窗中字符满足条件时，就开始执行下列逻辑
            if (count == 0) {
                // 左移滑窗左边界，找到符合条件的滑窗
                while (left < i && need[s.charAt(left)] < 0) {
                    need[s.charAt(left)]++;
                    left++;
                }
                // 记录最短满足条件的滑窗
                if (i - left + 1 < minSize) {
                    minSize = i - left + 1;
                    res = left;
                }
                count++;
                need[s.charAt(left)]++;
                left++;
            }
        }
        return minSize == Integer.MAX_VALUE ? "" : s.substring(res, res + minSize);
    }
}
```
python实现：   
```

```
# 其他



