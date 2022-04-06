# 剑指 Offer II 087. 复原 IP    
难度：中等   
题目地址：https://leetcode-cn.com/problems/0on3uN/   
完成时间：  2022/4/6   
# 题目

给定一个只包含数字的字符串 s ，用以表示一个 IP 地址，返回所有可能从 s 获得的 有效 IP 地址 。你可以按任何顺序返回答案。

有效 IP 地址 正好由四个整数（每个整数位于 0 到 255 之间组成，且不能含有前导 0），整数之间用 '.' 分隔。

例如："0.1.2.201" 和 "192.168.1.1" 是 有效 IP 地址，但是 "0.011.255.245"、"192.168.1.312" 和 "192.168@1.1" 是 无效 IP 地址。

**示例 1：**
```
输入：s = "25525511135"
输出：["255.255.11.135","255.255.111.35"]
```
**示例 2：**
```
输入：s = "0000"
输出：["0.0.0.0"]
```
**示例 3：**
```
输入：s = "1111"
输出：["1.1.1.1"]
```
**示例 4：**
```
输入：s = "010010"
输出：["0.10.0.10","0.100.1.0"]
```
**示例 5：**
```
输入：s = "10203040"
输出：["10.20.30.40","102.0.30.40","10.203.0.40"]
```

**提示：**

+ 0 <= s.length <= 3000
+ s 仅由数字组成
 

注意：本题与主站 93 题相同：https://leetcode-cn.com/problems/restore-ip-addresses/ 



# 思路

**总体思路：**

+ 递归回溯剪枝

**过程：**    

具体看代码。

# 代码  
java实现：   
```
class Solution {
    // 代表ip总共由四部分组成
    static final int IP_COUNT = 4;
    List<String> res = new ArrayList<String>();
    // 记录ip的四个部分
    int[] ip = new int[4];
    public List<String> restoreIpAddresses(String s) {
        dfs(s, 0, 0);
        return res;
    }

    // 递归回溯剪枝
    // 参数start：代表当前部分开始的位置。参数ip_count：代表当前是第几部分
    // 要把递归回溯算法（特别内部有for的结构），看成是树的来理解，不然很难理解
    public void dfs(String s, int start, int ip_count) {
        // 如果找到了 4 段 IP 地址并且遍历完了字符串，那么就是一种答案
        if (ip_count == IP_COUNT) {
            if (start == s.length()) {
                StringBuilder sb = new StringBuilder();
                sb.append(ip[0]);
                for (int i = 1; i < IP_COUNT; i++) {
                    sb.append('.');
                    sb.append(ip[i]);
                }
                res.add(sb.toString());
            }
            return;
        }

        // 如果还没有找到 4 段 IP 地址就已经遍历完了字符串，那么提前回溯
        if (start == s.length()) {
            return;
        }

        // 由于不能有前导零，如果当前数字为 0，那么这一段 IP 地址只能为 0
        if(s.charAt(start) == '0') {
            ip[ip_count] = 0;
            dfs(s, start + 1, ip_count + 1);
        }

        // 一般情况，枚举每一种可能性并递归
        int num = 0;
        for (int i = start; i < s.length(); i++) {
            num = num * 10 + s.charAt(i) - '0';
            if (num > 0 && num <= 255) {
                ip[ip_count] = num;
                dfs(s, i + 1, ip_count + 1);
            } else {
                break;
            }
        }
    }
}
```
python实现：   
```

```
# 其他



