# 第一部分 位运算

[剑指 Offer II 001. 整数除法](https://leetcode-cn.com/problems/xoh6Oh/)>>>>>[29. 两数相除](https://leetcode-cn.com/problems/divide-two-integers/)  
+ 位运算：减法代替除法

[剑指 Offer II 002. 二进制加法](https://leetcode-cn.com/problems/JFETK5/)>>>>>[67. 二进制求和](https://leetcode-cn.com/problems/add-binary/)
+ 位运算：简单模拟

[剑指 Offer II 003. 前 n 个数字二进制中 1 的个数](https://leetcode-cn.com/problems/w3tCBm/)>>>>>[338. 比特位计数](https://leetcode-cn.com/problems/counting-bits/)
+ 位运算：Brian Kernighan 算法
  + x = x & (x−1)，该运算将 x 的二进制表示的最后一个 1 变成 0
+ 优化： 动态规划

[剑指 Offer II 004. 只出现一次的数字](https://leetcode-cn.com/problems/WGki4K/)>>>>>[137. 只出现一次的数字 II](https://leetcode-cn.com/problems/single-number-ii/)
+ 暴力：哈希表
+ 优化：位运算 + 数字电路设计

[剑指 Offer II 005. 单词长度的最大乘积](https://leetcode-cn.com/problems/aseY1I/)>>>>>[318. 最大单词长度乘积](https://leetcode-cn.com/problems/maximum-product-of-word-lengths/)
+ 位运算（存储方式有些小独特，值得借鉴）

# 第二部分 双指针 / 滑动窗口（数组）

[剑指 Offer II 006. 排序数组中两个数字之和](https://leetcode-cn.com/problems/kLl5u1/)>>>>>[167. 两数之和 II - 输入有序数组](https://leetcode-cn.com/problems/two-sum-ii-input-array-is-sorted/)
+ 哈希字典
+ 优化：双指针

[剑指 Offer II 007. 数组中和为 0 的三个数
](https://leetcode-cn.com/problems/1fGaJU/)>>>>>[15. 三数之和](https://leetcode-cn.com/problems/3sum/)
+ 暴力：模拟
+ 优化：双指针

[剑指 Offer II 008. 和大于等于 target 的最短子数组](https://leetcode-cn.com/problems/2VG8Kg/)>>>>>[209. 长度最小的子数组](https://leetcode-cn.com/problems/minimum-size-subarray-sum/)
+ 暴力：前缀和
+ 优化：滑动窗口

[剑指 Offer II 009. 乘积小于 K 的子数组](https://leetcode-cn.com/problems/ZVAVXX/)>>>>>[713. 乘积小于K的子数组](https://leetcode-cn.com/problems/subarray-product-less-than-k/)
+ 滑动窗口

# 第三部分 哈希表 + 前缀和（数组）

[剑指 Offer II 010. 和为 k 的子数组](https://leetcode-cn.com/problems/QTMn0o/)>>>>>[560. 和为 K 的子数组](https://leetcode-cn.com/problems/subarray-sum-equals-k/)
+ 暴力：枚举
+ 优化：哈希表 + 前缀和

[剑指 Offer II 011. 0 和 1 个数相同的子数组](https://leetcode-cn.com/problems/A1NYOS/)>>>>>[525. 连续数组](https://leetcode-cn.com/problems/contiguous-array/solution/)
+ 哈希表 + 前缀和

[剑指 Offer II 012. 左右两边子数组的和相等](https://leetcode-cn.com/problems/tvdfij/)>>>>>[724. 寻找数组的中心下标](https://leetcode-cn.com/problems/find-pivot-index/)
+ 前缀和

[剑指 Offer II 013. 二维子矩阵的和](https://leetcode-cn.com/problems/O4NDxx/)>>>>>[304. 二维区域和检索 - 矩阵不可变](https://leetcode-cn.com/problems/range-sum-query-2d-immutable/)
+ 前缀和

# 第四部分 桶计数 + 滑动窗口（字符串处理）

[剑指 Offer II 014. 字符串中的变位词](https://leetcode-cn.com/problems/MPnaiL/)>>>>>[567. 字符串的排列](https://leetcode-cn.com/problems/permutation-in-string/)
+ 桶计数 + 滑动窗口
+ 优化：单滑窗

[剑指 Offer II 015. 字符串中的所有变位词](https://leetcode-cn.com/problems/VabMRr/)>>>>>[438. 找到字符串中所有字母异位词](https://leetcode-cn.com/problems/find-all-anagrams-in-a-string/)
+ 桶计数 + 滑动窗口
+ 优化：单滑窗

[剑指 Offer II 016. 不含重复字符的最长子字符串](https://leetcode-cn.com/problems/wtcaE1/)>>>>>[3. 无重复字符的最长子串](https://leetcode-cn.com/problems/longest-substring-without-repeating-characters/)
+ 哈希字典（模拟） + 滑动窗口

[剑指 Offer II 017. 含有所有字符的最短字符串](https://leetcode-cn.com/problems/M1oyTv/)>>>>>[76. 最小覆盖子串](https://leetcode-cn.com/problems/minimum-window-substring/)
+ 桶计数 + 滑动窗口

# 第五部分 回文字符串处理（双指针）

[剑指 Offer II 018. 有效的回文](https://leetcode-cn.com/problems/XltzEq/)>>>>>[125. 验证回文串](https://leetcode-cn.com/problems/valid-palindrome/)
+ 双指针

[剑指 Offer II 019. 最多删除一个字符得到回文](https://leetcode-cn.com/problems/RQku0D/)>>>>>[680. 验证回文字符串 Ⅱ](https://leetcode-cn.com/problems/valid-palindrome-ii/)
+ 双指针

[剑指 Offer II 020. 回文子字符串的个数](https://leetcode-cn.com/problems/a7VOhD/)>>>>>[647. 回文子串](https://leetcode-cn.com/problems/palindromic-substrings/)
+ 基本：双指针（中心扩展算法） / 动态规划(dp)
+ 优化;马拉车算法 （一般用于求字符串的最大回文子串，这里也能用）
+ 总时间效率：马拉车 > 中心扩散 > 动态规划

# 第六部分 链表处理（）
[剑指 Offer II 021. 删除链表的倒数第 n 个结点](https://leetcode-cn.com/problems/SLwz0R/)>>>>>[19. 删除链表的倒数第 N 个结点](https://leetcode-cn.com/problems/remove-nth-node-from-end-of-list/submissions/)
+ 前后双指针 / 递归 / 堆栈

[剑指 Offer II 022. 链表中环的入口节点](https://leetcode-cn.com/problems/c32eOV/)>>>>>[142. 环形链表 II](https://leetcode-cn.com/problems/linked-list-cycle-ii/)
+ 哈希表
+ 快慢指针（龟兔赛跑）解法：Floyd 判圈算法

[剑指 Offer II 023. 两个链表的第一个重合节点](https://leetcode-cn.com/problems/3u1WK4/)>>>>>[160. 相交链表](https://leetcode-cn.com/problems/intersection-of-two-linked-lists/)
+ 哈希表
+ 双指针

[剑指 Offer II 024. 反转链表](https://leetcode-cn.com/problems/UHnkqh/)>>>>>[206. 反转链表](https://leetcode-cn.com/problems/reverse-linked-list/submissions/)
+ 迭代 / 递归



