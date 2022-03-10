# 剑指 Offer II 016. 不含重复字符的最长子字符串
难度：中等   
题目地址：https://leetcode-cn.com/problems/wtcaE1/   
完成时间：  2022/3/10   
# 题目
给定一个字符串 s ，请你找出其中不含有重复字符的 最长连续子字符串 的长度。

 

**示例 1:**
```
输入: s = "abcabcbb"
输出: 3 
解释: 因为无重复字符的最长子字符串是 "abc"，所以其长度为 3。
```
**示例 2:**
```
输入: s = "bbbbb"
输出: 1
解释: 因为无重复字符的最长子字符串是 "b"，所以其长度为 1。
```
**示例 3:**
```
输入: s = "pwwkew"
输出: 3
解释: 因为无重复字符的最长子串是 "wke"，所以其长度为 3。
     请注意，你的答案必须是 子串 的长度，"pwke" 是一个子序列，不是子串。
```
**示例 4:**
```
输入: s = ""
输出: 0
```
 

**提示：**

+ 0 <= s.length <= 5 * 104
+ s 由英文字母、数字、符号和空格组成
 

注意：本题与主站 3 题相同： https://leetcode-cn.com/problems/longest-substring-without-repeating-characters/


# 思路

**总体思路：**

哈希字典（模拟） + 滑动窗口

**过程：**    

本题主要解法，我使用的是哈希字典+滑动窗口。然后通过思考题目过程，使用模拟的方式，解决此题。

# 代码  
java实现：   
```
class Solution {
    // 哈希字典（模拟）
    public int lengthOfLongestSubstring(String s) {
        Map<Character, Integer> map = new HashMap<Character, Integer>();
        int len = s.length();
        int res = 0, start = 0;
        for (int i = 0; i < len; i++) {
            char ch = s.charAt(i);
            // 模拟
            if (map.containsKey(ch)) {
                start = Math.max(start, map.get(ch) + 1);
            }
            res = Math.max(res, i - start + 1);
            map.put(ch, i);
        }
        return res;
    }
}
```
python实现：   
```

```
# 其他

记录本题的原因是因为，我看的官方题解以及其他一些解法，基本都使用的Set或者其他数据结构。我觉得使用哈希字典的方式会相对简单一些。


