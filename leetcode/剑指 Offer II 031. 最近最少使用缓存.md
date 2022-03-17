# 剑指 Offer II 031. 最近最少使用缓存
难度：中等   
题目地址：https://leetcode-cn.com/OrIXps/   
完成时间：  2022/3/17   
# 题目
运用所掌握的数据结构，设计和实现一个  LRU (Least Recently Used，最近最少使用) 缓存机制 。

实现 LRUCache 类：

+ LRUCache(int capacity) 以正整数作为容量 capacity 初始化 LRU 缓存
+ int get(int key) 如果关键字 key 存在于缓存中，则返回关键字的值，否则返回 -1 。
+ void put(int key, int value) 如果关键字已经存在，则变更其数据值；如果关键字不存在，则插入该组「关键字-值」。当缓存容量达到上限时，它应该在写入新数据之前删除最久未使用的数据值，从而为新的数据值留出空间。
 

**示例：**
```
输入
["LRUCache", "put", "put", "get", "put", "get", "put", "get", "get", "get"]
[[2], [1, 1], [2, 2], [1], [3, 3], [2], [4, 4], [1], [3], [4]]
输出
[null, null, null, 1, null, -1, null, -1, 3, 4]

解释
LRUCache lRUCache = new LRUCache(2);
lRUCache.put(1, 1); // 缓存是 {1=1}
lRUCache.put(2, 2); // 缓存是 {1=1, 2=2}
lRUCache.get(1);    // 返回 1
lRUCache.put(3, 3); // 该操作会使得关键字 2 作废，缓存是 {1=1, 3=3}
lRUCache.get(2);    // 返回 -1 (未找到)
lRUCache.put(4, 4); // 该操作会使得关键字 1 作废，缓存是 {4=4, 3=3}
lRUCache.get(1);    // 返回 -1 (未找到)
lRUCache.get(3);    // 返回 3
lRUCache.get(4);    // 返回 4
```

**提示：**

+ 1 <= capacity <= 3000
+ 0 <= key <= 10000
+ 0 <= value <= 105
+ 最多调用 2 * 105 次 get 和 put
 

进阶：是否可以在 O(1) 时间复杂度内完成这两种操作？



# 思路

**总体思路：**

哈希字典 + 双向链表

**过程：**    

本题的场景是模拟LRU缓存机制，关键点在于对数据结构的选取和实现。

# 代码  
java实现：   
```
// 哈希字典 + 双向链表
class LRUCache {
    class ListNode {
        int key;
        int value;
        ListNode prev;
        ListNode next;
        public ListNode() {}
        public ListNode(int _key, int _value) {
            this.key = _key;
            this.value = _value;
        }
    }

    Map<Integer, ListNode> map = new HashMap<Integer, ListNode>();
    ListNode head, last;
    int size;
    int capacity;

    public LRUCache(int capacity) {
        this.capacity = capacity;
        head = new ListNode();
        last = new ListNode();
        head.next = last;
        last.prev = head;
    }
    
    public int get(int key) {
        if (!map.containsKey(key)) {
            return -1;
        }
        ListNode node = map.get(key);
        moveToHead(node);
        return node.value;
    }
    
    public void put(int key, int value) {
        if (map.containsKey(key)) {
            ListNode node = map.get(key);
            node.value = value;
            moveToHead(node);
        } else {
            ListNode newNode = new ListNode(key, value);
            map.put(key, newNode);
            addHead(newNode);
            this.size++; 
            if (this.size > this.capacity) {
                size = capacity;
                ListNode removeNode = removeLast();
                map.remove(removeNode.key);
            }
        }
    }
    
    // 将节点加入到头节点处
    public void addHead(ListNode node) {
        node.prev = head;
        node.next = head.next;
        head.next.prev = node;
        head.next = node;
    }

    // 删除某节点
    public void remove(ListNode node) {
        node.prev.next = node.next;
        node.next.prev = node.prev;
    }

    // 将节点移至头节点处
    public void moveToHead(ListNode node) {
        remove(node);
        addHead(node);
    }

    // 当size > capacity时，超过容量，则移除末尾元素
    public ListNode removeLast() {
        ListNode node = last.prev;
        remove(node);
        return node;
    }
}

/**
 * Your LRUCache object will be instantiated and called as such:
 * LRUCache obj = new LRUCache(capacity);
 * int param_1 = obj.get(key);
 * obj.put(key,value);
 */
```
python实现：   
```

```
# 其他



