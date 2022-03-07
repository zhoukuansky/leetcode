# 剑指 Offer II 005. 单词长度的最大乘积
难度：中等   
题目地址：https://leetcode-cn.com/problems/aseY1I/   
完成时间：  2022/3/7   
# 题目
给定一个字符串数组 words，请计算当两个字符串 words[i] 和 words[j] 不包含相同字符时，它们长度的乘积的最大值。假设字符串中只包含英语的小写字母。如果没有不包含相同字符的一对字符串，返回 0。

 
**示例 1:**
```
输入: words = ["abcw","baz","foo","bar","fxyz","abcdef"]
输出: 16 
解释: 这两个单词为 "abcw", "fxyz"。它们不包含相同字符，且长度的乘积最大。
```
**示例 2:**
```
输入: words = ["a","ab","abc","d","cd","bcd","abcd"]
输出: 4 
解释: 这两个单词为 "ab", "cd"。
```
**示例 3:**
```
输入: words = ["a","aa","aaa","aaaa"]
输出: 0 
解释: 不存在这样的两个单词。
```

**提示：**

+ 2 <= words.length <= 1000
+ 1 <= words[i].length <= 1000
+ words[i] 仅包含小写字母
 

注意：本题与主站 318 题相同：https://leetcode-cn.com/problems/maximum-product-of-word-lengths/


# 思路

**总体思路：**

位运算：   
本题的难点是如何记录一个字符串中出现过的字母。   
本题使用的方法是：使用一个32位整数记录一个字符串中出现过的字母（只有英文小写字母）。

**过程：**    



# 代码  
java实现：   
```
class Solution {
    // 位运算
    public int maxProduct(String[] words) {
        int len = words.length;
        /**
        全是小写字母, 可以用一个32位整数表示一个word中出现的字母, 
        hash[i]存放第i个单词出现过的字母, a对应32位整数的最后一位,
        b对应整数的倒数第二位, 依次类推. 时间复杂度O(N^2)
        判断两两单词按位与的结果, 如果结果为0且长度积大于最大积则更新
        **/
        int[] hash = new int[len];
        int res = 0;
        for (int i = 0; i < len; i++) {
            for (char ch : words[i].toCharArray()) {
                hash[i] |= 1 << (ch - 'a');
            }
        }
        for (int i = 0; i < len; i++) {
            for (int j = i + 1; j < len; j++) {
                if ((hash[i] & hash[j]) == 0) {
                    res = Math.max(res, words[i].length() * words[j].length());
                }
            }
        }
        return res;
    }
}
```
python实现：   
```
class Solution:
    # 位运算
    def maxProduct(self, words: List[str]) -> int:
        N = len(words)
        hash = [0] * N
        res = 0
        for i in range(N):
            for ch in words[i]:
                hash[i] |= 1 << ord(ch) - ord('a')
        for i in range(N):
            for j in range(i + 1, N):
                if hash[i] & hash[j] == 0:
                    res = max(res, len(words[i]) * len(words[j]))
        return res
```
# 其他


记录本题主要是觉得，使用一个32位整数记录一个字符串出现过的英文字符，很有意思。
