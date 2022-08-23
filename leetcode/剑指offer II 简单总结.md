# 第一部分 位运算

[剑指 Offer II 001. 整数除法](https://leetcode-cn.com/problems/xoh6Oh/)>>>>>[29. 两数相除](https://leetcode-cn.com/problems/divide-two-integers/)  
+ 位运算：减法代替除法
+ 优化1：快速乘法
+ 优化2：位运算优化

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

# 第十二部分 二叉搜索树
[剑指 Offer II 052. 展平二叉搜索树](https://leetcode-cn.com/problems/NYBBNL/)>>>>>[897. 递增顺序搜索树](https://leetcode-cn.com/problems/increasing-order-search-tree/)
+ 递归中序遍历

[剑指 Offer II 053. 二叉搜索树中的中序后继](https://leetcode-cn.com/problems/P5rCT8/)>>>>>会员专享无法查看   
+ 中序遍历：并未利用到二叉搜索树的性质
+ 模拟：利用二叉搜索树性质

[剑指 Offer II 054. 所有大于等于节点的值之和](https://leetcode-cn.com/problems/w6cpku/)>>>>>[538. 把二叉搜索树转换为累加树](https://leetcode-cn.com/problems/convert-bst-to-greater-tree/)>>>>>[1038. 从二叉搜索树到更大和树](https://leetcode-cn.com/problems/binary-search-tree-to-greater-sum-tree/)
+ 中序遍历（倒过来）

[剑指 Offer II 055. 二叉搜索树迭代器](https://leetcode-cn.com/problems/kTOapQ/)>>>>>[173. 二叉搜索树迭代器
](https://leetcode-cn.com/problems/binary-search-tree-iterator/)
+ 中序遍历 + 动态数组

[剑指 Offer II 056. 二叉搜索树中两个节点之和](https://leetcode-cn.com/problems/opLdQZ/)>>>>>[653. 两数之和 IV - 输入 BST](https://leetcode-cn.com/problems/two-sum-iv-input-is-a-bst/)
+ 哈希集合：并未利用到二叉搜索树的性质（优化解法暂时不写）

# 第十三部分 有序集合 / 有序字典 / 优先队列（大小顶堆）
[剑指 Offer II 057. 值和下标之差都在给定的范围内](https://leetcode-cn.com/problems/7WqeDu/)>>>>>[220. 存在重复元素 III
](https://leetcode-cn.com/problems/contains-duplicate-iii/)
+ 有序集合 + 滑动窗口
+ 优化：桶计数 + 滑动窗口（本质是将有序集合换为哈希字典减少时间复杂度）

[剑指 Offer II 058. 日程表](https://leetcode-cn.com/problems/fi9suh/)>>>>>[729. 我的日程安排表 I](https://leetcode-cn.com/problems/my-calendar-i/)
+ 有序字典

[剑指 Offer II 059. 数据流的第 K 大数值](https://leetcode-cn.com/problems/jBjn9C/)>>>>>[703. 数据流中的第 K 大元素](https://leetcode-cn.com/problems/kth-largest-element-in-a-stream/)
+ 优先队列：小顶堆

[剑指 Offer II 060. 出现频率最高的 k 个数字](https://leetcode-cn.com/problems/g5c51o/)>>>>>[347. 前 K 个高频元素](https://leetcode-cn.com/problems/top-k-frequent-elements/)
+ 小顶堆 + 哈希字典

[剑指 Offer II 061. 和最小的 k 个数对](https://leetcode-cn.com/problems/qn8gGX/)>>>>>[373. 查找和最小的 K 对数字](https://leetcode-cn.com/problems/find-k-pairs-with-smallest-sums/)
+ 大顶堆


# 第十四部分 字典树
[剑指 Offer II 062. 实现前缀树](https://leetcode-cn.com/problems/QC3q1f/)>>>>>[208. 实现 Trie (前缀树)](https://leetcode-cn.com/problems/implement-trie-prefix-tree/)
+ 前缀字典树构造

[剑指 Offer II 063. 替换单词](https://leetcode-cn.com/problems/UhWRSj/)>>>>>[648. 单词替换](https://leetcode-cn.com/problems/replace-words/)
+ 构造前缀字典树

[剑指 Offer II 064. 神奇的字典](https://leetcode-cn.com/problems/US1pGT/)>>>>>[676. 实现一个魔法字典](https://leetcode-cn.com/problems/implement-magic-dictionary/)
+ 哈希字典 + 动态数组
+ 前缀字典树 + 递归（未实现）

[剑指 Offer II 065. 最短的单词编码](https://leetcode-cn.com/problems/iSwD2y/)>>>>>[820. 单词的压缩编码](https://leetcode-cn.com/problems/short-encoding-of-words/)
+ 暴力：哈希表存储后缀
+ 优化：后缀字典树

[剑指 Offer II 066. 单词之和](https://leetcode-cn.com/problems/z1R5dt/)>>>>>[677. 键值映射](https://leetcode-cn.com/problems/map-sum-pairs/)
+ 哈希字典
+ 前缀字典树

[剑指 Offer II 067. 最大的异或](https://leetcode-cn.com/problems/ms70jA/)>>>>>[421. 数组中两个数的最大异或值](https://leetcode-cn.com/problems/maximum-xor-of-two-numbers-in-an-array/)
+ 哈希表
+ 前缀字典树

# 第十五部分 二分法
[剑指 Offer II 068. 查找插入位置](https://leetcode-cn.com/problems/N6YdxV/)>>>>>[35. 搜索插入位置](https://leetcode-cn.com/problems/search-insert-position/)
+ 二分法

[剑指 Offer II 069. 山峰数组的顶部](https://leetcode-cn.com/problems/B1IidL/)>>>>>[852. 山脉数组的峰顶索引](https://leetcode-cn.com/problems/peak-index-in-a-mountain-array/)
+ 暴力法：模拟
+ 优化：二分法

[剑指 Offer II 070. 排序数组中只出现一次的数字](https://leetcode-cn.com/problems/skFtm2/)>>>>>[540. 有序数组中的单一元素](https://leetcode-cn.com/problems/single-element-in-a-sorted-array/)
+ 二分法

[剑指 Offer II 071. 按权重生成随机数](https://leetcode-cn.com/problems/cuyjEf/)>>>>>[528. 按权重随机选择](https://leetcode-cn.com/problems/random-pick-with-weight/submissions/)
+ 前缀和 + 二分查找

[剑指 Offer II 072. 求平方根](https://leetcode-cn.com/problems/jJ0w9p/)>>>>>[69. x 的平方根](https://leetcode-cn.com/problems/sqrtx/)
+ 二分查找（除法代替乘法）

[剑指 Offer II 073. 狒狒吃香蕉](https://leetcode-cn.com/problems/nZZqjQ/)>>>>>[875. 爱吃香蕉的珂珂](https://leetcode-cn.com/problems/koko-eating-bananas/)
+ 二分查找


# 第十六部分 排序
[剑指 Offer II 074. 合并区间](https://leetcode-cn.com/problems/SsGoHC/)>>>>>[56. 合并区间](https://leetcode-cn.com/problems/merge-intervals/)
+ 排序 + 模拟

[剑指 Offer II 075. 数组相对排序](https://leetcode-cn.com/problems/0H97ZC/)>>>>>[1122. 数组的相对排序
](https://leetcode-cn.com/problems/relative-sort-array/)
+ 自定义排序(java实现较为复杂)
+ 计数排序

[剑指 Offer II 076. 数组中的第 k 大的数字](https://leetcode-cn.com/problems/xx4gT2/)>>>>>[215. 数组中的第K个最大元素](https://leetcode-cn.com/problems/kth-largest-element-in-an-array/)
+ 排序/最小堆

[剑指 Offer II 077. 链表排序](https://leetcode-cn.com/problems/7WHec2/)>>>>>[148. 排序链表](https://leetcode-cn.com/problems/sort-list/)
+ 暴力排序
+ 归并排序（未实现和理解）

[剑指 Offer II 078. 合并排序链表](https://leetcode-cn.com/problems/vvXgSW/)>>>>>[23. 合并K个升序链表](https://leetcode-cn.com/problems/merge-k-sorted-lists/)
+ 小顶堆


# 第十七部分 递归回溯剪枝
[剑指 Offer II 079. 所有子集](https://leetcode-cn.com/problems/TVdhkn/)>>>>>[78. 子集](https://leetcode-cn.com/problems/subsets/)
+ 迭代回溯枚举 / 递归回溯枚举

[剑指 Offer II 080. 含有 k 个元素的组合](https://leetcode-cn.com/problems/uUsW3B/)>>>>>[77. 组合](https://leetcode-cn.com/problems/combinations/)
+ 递归回溯剪枝

[剑指 Offer II 081. 允许重复选择元素的组合](https://leetcode-cn.com/problems/Ygoe9J/)>>>>>[39. 组合总和](https://leetcode-cn.com/problems/combination-sum/)
+ 递归回溯剪枝

[剑指 Offer II 082. 含有重复元素集合的组合](https://leetcode-cn.com/problems/4sjJUc/)>>>>>[40. 组合总和 II](https://leetcode-cn.com/problems/combination-sum-ii/)
+ 递归回溯剪枝

[剑指 Offer II 083. 没有重复元素集合的全排列](https://leetcode-cn.com/problems/VvJkup/)>>>>>[46. 全排列](https://leetcode-cn.com/problems/permutations/)
+ 递归回溯剪枝

[剑指 Offer II 084. 含有重复元素集合的全排列 ](https://leetcode-cn.com/problems/7p8L0Z/)>>>>>[47. 全排列 II](https://leetcode-cn.com/problems/permutations-ii/)
+ 递归回溯剪枝

[剑指 Offer II 085. 生成匹配的括号](https://leetcode-cn.com/problems/IDBivT/)>>>>>[22. 括号生成](https://leetcode-cn.com/problems/generate-parentheses/)+
+ 递归回溯剪枝

[剑指 Offer II 086. 分割回文子字符串](https://leetcode-cn.com/problems/M99OJA/)>>>>>[131. 分割回文串](https://leetcode-cn.com/problems/palindrome-partitioning/)
+ 动态规划 + 递归回溯剪枝

[剑指 Offer II 087. 复原 IP ](https://leetcode-cn.com/problems/0on3uN/)>>>>>[93. 复原 IP 地址](https://leetcode-cn.com/problems/restore-ip-addresses/)
+ 递归回溯剪枝

# 第十八部分 动态规划
[剑指 Offer II 088. 爬楼梯的最少成本](https://leetcode-cn.com/problems/GzCJIP/)>>>>>[746. 使用最小花费爬楼梯](https://leetcode-cn.com/problems/min-cost-climbing-stairs/)
+ 动态规划

[剑指 Offer II 089. 房屋偷盗](https://leetcode-cn.com/problems/Gu0c2T/)>>>>>[198. 打家劫舍](https://leetcode-cn.com/problems/house-robber/)
+ 动态规划

[剑指 Offer II 090. 环形房屋偷盗](https://leetcode-cn.com/problems/PzWKhm/)>>>>>[213. 打家劫舍 II](https://leetcode-cn.com/problems/house-robber-ii/)
+ 动态规划

[剑指 Offer II 091. 粉刷房子](https://leetcode-cn.com/problems/JEj789/)>>>>>会员专享无法查看
+ 动态规划（二维）

[剑指 Offer II 092. 翻转字符](https://leetcode-cn.com/problems/cyJERH/)>>>>>[926. 将字符串翻转到单调递增](https://leetcode-cn.com/problems/flip-string-to-monotone-increasing/)
+ 动态规划

[剑指 Offer II 093. 最长斐波那契数列](https://leetcode-cn.com/problems/Q91FMA/)>>>>>[873. 最长的斐波那契子序列的长度](https://leetcode-cn.com/problems/length-of-longest-fibonacci-subsequence/)
+ 暴力：哈希集合
+ 优化：动态规划

[剑指 Offer II 094. 最少回文分割](https://leetcode-cn.com/problems/omKAoA/)>>>>>[132. 分割回文串 II](https://leetcode-cn.com/problems/palindrome-partitioning-ii/)
+ 动态规划（两次使用）

[剑指 Offer II 095. 最长公共子序列](https://leetcode-cn.com/problems/qJnOS7/)>>>>>[1143. 最长公共子序列](https://leetcode-cn.com/problems/longest-common-subsequence/)
+ 动态规划（二维）

[剑指 Offer II 096. 字符串交织](https://leetcode-cn.com/problems/IY6buf/)>>>>>[97. 交错字符串](https://leetcode-cn.com/problems/interleaving-string/)
+ 动态规划（二维）

[剑指 Offer II 097. 子序列的数目](https://leetcode-cn.com/problems/21dk04/)>>>>>[115. 不同的子序列](https://leetcode-cn.com/problems/distinct-subsequences/)
+ 动态规划（二维）

[剑指 Offer II 098. 路径的数目](https://leetcode-cn.com/problems/2AoeFn/)>>>>>[62. 不同路径](https://leetcode-cn.com/problems/unique-paths/)
+ 简单  动态规划
+ 数学方案（高中知识）：组合

[剑指 Offer II 099. 最小路径之和](https://leetcode-cn.com/problems/0i0mDW/)>>>>>[64. 最小路径和](https://leetcode-cn.com/problems/minimum-path-sum/)
+ 动态规划

[剑指 Offer II 100. 三角形中最小路径之和](https://leetcode-cn.com/problems/IlPe0q/)>>>>>[120. 三角形最小路径和](https://leetcode-cn.com/problems/triangle/)
+ 动态规划

# 第十九部分 动态规划（背包问题）

[剑指 Offer II 101. 分割等和子集](https://leetcode-cn.com/problems/NUPfPr/)>>>>>[416. 分割等和子集](https://leetcode-cn.com/problems/partition-equal-subset-sum/)
+ 动态规划：背包问题

[剑指 Offer II 102. 加减的目标值](https://leetcode-cn.com/problems/YaVDxD/)>>>>>[494. 目标和](https://leetcode-cn.com/problems/target-sum/)
+ 递归迭代
+ 动态规划：0-1背包问题

[剑指 Offer II 103. 最少的硬币数目](https://leetcode-cn.com/problems/gaM7Ch/)>>>>>[322. 零钱兑换](https://leetcode-cn.com/problems/coin-change/)
+ 动态规划：完全规划问题

[剑指 Offer II 104. 排列的数目](https://leetcode-cn.com/problems/D0F0SV/)>>>>>[377. 组合总和 Ⅳ](https://leetcode-cn.com/problems/combination-sum-iv/)
+ 动态规划：背包问题变种

# 第二十部分 深搜 / 广搜 / 并查集

[剑指 Offer II 105. 岛屿的最大面积](https://leetcode-cn.com/problems/ZL6zAn/)>>>>>[695. 岛屿的最大面积](https://leetcode-cn.com/problems/max-area-of-island/)
+ 深度优先搜索（递归 / 堆栈）
+ 广度优先搜索（队列）
+ 并查集（未实现）

[剑指 Offer II 106. 二分图](https://leetcode-cn.com/problems/vEAB3K/)>>>>>[785. 判断二分图](https://leetcode-cn.com/problems/is-graph-bipartite/)
+ 深度优先搜索（递归染色法）
+ 广度优先搜索（队列）

[剑指 Offer II 107. 矩阵中的距离](https://leetcode-cn.com/problems/2bCMpM/)>>>>>[542. 01 矩阵](https://leetcode-cn.com/problems/01-matrix/)
+ 广度优先搜索
+ 动态规划

[剑指 Offer II 108. 单词演变](https://leetcode-cn.com/problems/om3reC/)>>>>>[127. 单词接龙](https://leetcode-cn.com/problems/word-ladder/)
+ 广度优先遍历
+ 先建图，再广搜

[剑指 Offer II 109. 开密码锁](https://leetcode-cn.com/problems/zlDJc7/)>>>>>[752. 打开转盘锁](https://leetcode-cn.com/problems/open-the-lock/)
+ 广度优先搜索

[剑指 Offer II 110. 所有路径](https://leetcode-cn.com/problems/bP4bmD/)>>>>>[797. 所有可能的路径](https://leetcode-cn.com/problems/all-paths-from-source-to-target/)
+ 深度优先搜索

[剑指 Offer II 112. 最长递增路径](https://leetcode-cn.com/problems/fpTFWP/)>>>>>[329. 矩阵中的最长递增路径](https://leetcode-cn.com/problems/longest-increasing-path-in-a-matrix/)
+ 记忆化深度优先搜索

# 第二十一部分 拓扑排序

[剑指 Offer II 113. 课程顺序](https://leetcode-cn.com/problems/QA2IGt/)>>>>>[210. 课程表 II](https://leetcode-cn.com/problems/course-schedule-ii/)
+ 拓扑排序（深度优先搜索）

[剑指 Offer II 114. 外星文字典](https://leetcode-cn.com/problems/Jf1JuT/)>>>>>会员专享无法查看
+ 拓扑排序（广度优先搜索）