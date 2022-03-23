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

[剑指 Offer II 025. 链表中的两数相加](https://leetcode-cn.com/problems/lMSNwu/)>>>>>[445. 两数相加 II](https://leetcode-cn.com/problems/add-two-numbers-ii/)
+ 反转链表（迭代 / 递归）
+ 堆栈

[剑指 Offer II 026. 重排链表](https://leetcode-cn.com/problems/LGjMqU/)>>>>>[143. 重排链表](https://leetcode-cn.com/problems/reorder-list/)
+ 线性表

[剑指 Offer II 027. 回文链表](https://leetcode-cn.com/problems/aMhZSa/)>>>>>[234. 回文链表](https://leetcode-cn.com/problems/palindrome-linked-list/)
+ 动态数组 + 双指针
+ 递归

[剑指 Offer II 028. 展平多级双向链表](https://leetcode-cn.com/problems/Qv1Da2/)>>>>>[430. 扁平化多级双向链表](https://leetcode-cn.com/problems/flatten-a-multilevel-doubly-linked-list/)
+ 堆栈方法
+ 二叉树法(将题目看成一棵二叉树)

[剑指 Offer II 029. 排序的循环链表](https://leetcode-cn.com/problems/4ueAj6/)>>>>>会员专享无法查看
+ 模拟（硬生生模拟）

# 第七部分 场景模拟（）
[剑指 Offer II 030. 插入、删除和随机访问都是 O(1) 的容器](https://leetcode-cn.com/problems/FortPu/)>>>>>[380. O(1) 时间插入、删除和获取随机元素](https://leetcode-cn.com/problems/insert-delete-getrandom-o1/)
+ 哈希字典 + 动态数组

[剑指 Offer II 031. 最近最少使用缓存](https://leetcode-cn.com/problems/OrIXps/)>>>>>[146. LRU 缓存](https://leetcode-cn.com/problems/lru-cache/submissions/)
+ 哈希字典 + 双向链表

# 第八部分 排序的应用
[剑指 Offer II 032. 有效的变位词](https://leetcode-cn.com/problems/dKk3P7/)>>>>>[242. 有效的字母异位词](https://leetcode-cn.com/problems/valid-anagram/)
+ 简单桶计数

[剑指 Offer II 033. 变位词组](https://leetcode-cn.com/problems/sfvd7V/)>>>>>[49. 字母异位词分组](https://leetcode-cn.com/problems/group-anagrams/)
+ 哈希字典 + 排序

[剑指 Offer II 034. 外星语言是否排序](https://leetcode-cn.com/problems/lwyVBB/)>>>>>[953. 验证外星语词典](https://leetcode-cn.com/problems/verifying-an-alien-dictionary/)
+ 模拟

[剑指 Offer II 035. 最小时间差](https://leetcode-cn.com/problems/569nqc/)>>>>>[539. 最小时间差](https://leetcode-cn.com/problems/minimum-time-difference/)
+ 模拟+ 排序

# 第九部分 堆栈
[剑指 Offer II 036. 后缀表达式](https://leetcode-cn.com/problems/8Zf90G/)>>>>>[150. 逆波兰表达式求值](https://leetcode-cn.com/problems/evaluate-reverse-polish-notation/)
+ 堆栈

[剑指 Offer II 037. 小行星碰撞](https://leetcode-cn.com/problems/XagZNi/)>>>>>[735. 行星碰撞](https://leetcode-cn.com/problems/asteroid-collision/)
+ 堆栈 + 模拟

[剑指 Offer II 038. 每日温度](https://leetcode-cn.com/problems/iIQa4I/)>>>>>[739. 每日温度](https://leetcode-cn.com/problems/daily-temperatures/)
+ 单调递减栈

[剑指 Offer II 039. 直方图最大矩形面积](https://leetcode-cn.com/problems/0ynMMM/)>>>>>[84. 柱状图中最大的矩形](https://leetcode-cn.com/problems/largest-rectangle-in-histogram/)
+ 暴力解法(双指针/中心扩散)
+ 单调递增栈 + 哨兵

[剑指 Offer II 040. 矩阵中最大的矩形](https://leetcode-cn.com/problems/PLYXKQ/)>>>>>[85. 最大矩形](https://leetcode-cn.com/problems/maximal-rectangle/)
+ 暴力解法：柱状图
+ 单调递增栈

# 第十部分 滑动窗口
[剑指 Offer II 041. 滑动窗口的平均值](https://leetcode-cn.com/problems/qIsx9U/)>>>>>会员专享无法查看
+ 滑动窗口

[剑指 Offer II 042. 最近请求次数](https://leetcode-cn.com/problems/H8086Q/)>>>>>[933. 最近的请求次数](https://leetcode-cn.com/problems/number-of-recent-calls/)
+ 滑动窗口

# 第十一部分 层序遍历二叉树
[剑指 Offer II 043. 往完全二叉树添加节点](https://leetcode-cn.com/problems/NaqhDT/)>>>>>[919. 完全二叉树插入器](https://leetcode-cn.com/problems/complete-binary-tree-inserter/)
+ 层序遍历（两次运用队列）

[剑指 Offer II 044. 二叉树每层的最大值](https://leetcode-cn.com/problems/hPov7L/)>>>>>[515. 在每个树行中找最大值](https://leetcode-cn.com/problems/find-largest-value-in-each-tree-row/submissions/)
+ 迭代(层序遍历) / 递归深搜

[剑指 Offer II 045. 二叉树最底层最左边的值](https://leetcode-cn.com/problems/LwUNpT/)>>>>>[513. 找树左下角的值](https://leetcode-cn.com/problems/find-bottom-left-tree-value/)
+ 迭代(层序遍历) / 递归深搜

[剑指 Offer II 046. 二叉树的右侧视图](https://leetcode-cn.com/problems/WNC0Lk/)>>>>>[199. 二叉树的右视图](https://leetcode-cn.com/problems/binary-tree-right-side-view/)
+ 迭代(层序遍历) / 递归深搜

[剑指 Offer II 047. 二叉树剪枝](https://leetcode-cn.com/problems/pOCWxh/)>>>>>[814. 二叉树剪枝](https://leetcode-cn.com/problems/binary-tree-pruning/)
+ 递归深搜

[剑指 Offer II 048. 序列化与反序列化二叉树](https://leetcode-cn.com/problems/h54YBf/)>>>>>[297. 二叉树的序列化与反序列化](https://leetcode-cn.com/problems/serialize-and-deserialize-binary-tree/)
+ 递归深搜 / 层序迭代

[剑指 Offer II 049. 从根节点到叶节点的路径数字之和](https://leetcode-cn.com/problems/3Etpl5/)>>>>>[129. 求根节点到叶节点数字之和](https://leetcode-cn.com/problems/sum-root-to-leaf-numbers/)
+ 递归深搜

[剑指 Offer II 050. 向下的路径节点之和](https://leetcode-cn.com/problems/6eUYwP/)>>>>>[437. 路径总和 III](https://leetcode-cn.com/problems/path-sum-iii/)
+ 暴力： 递归深搜 + 枚举遍历
+ 优化： 递归深搜 + 哈希字典 + 前缀和

[剑指 Offer II 051. 节点之和最大的路径](https://leetcode-cn.com/problems/jC7MId/)>>>>>[124. 二叉树中的最大路径和](https://leetcode-cn.com/problems/binary-tree-maximum-path-sum/)
+ 递归


