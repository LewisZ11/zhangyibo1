
以下8个门类是面试中最常考的算法与数据结构知识点。

**排序类（Sort）：**

* 基础知识：快速排序（Quick Sort）， 归并排序（Merge Sort）的原理与代码实现。需要能讲明白代码中每一行的目的。快速排序时间复杂度平均状态下O（NlogN），空间复杂度O（1），归并排序最坏情况下时间复杂度O（NlogN），空间复杂度O（N）
* 入门题目：
* 进阶题目：

注意：后两题是与快速排序非常相似的快速选择（Quick Select）算法，面试中很常考

**链表类（Linked List）：**

* 基础知识：链表如何实现，如何遍历链表。链表可以保证头部尾部插入删除操作都是O（1），查找任意元素位置O（N）
* 基础题目：

注意：快慢指针和链表反转几乎是所有链表类问题的基础，尤其是反转链表，代码很短，建议直接背熟。

* 进阶题目:

**堆（Heap or Priority Queue）、栈（Stack）、队列（Queue）、哈希表类（Hashmap、Hashset）：**

* 基础知识：各个数据结构的基本原理，增删查改复杂度。
* Queue题目：
* Stack题目：
  * 再做一下 Leetcode 224. Basic Calculator II (I, II, III, IV)
* Hashmap/ Hashset题目：
  * Leetcode 146. LRU Cache (Python中可以使用OrderedDict来代替)
  * 想一下思路 可以再写一下 Leetcode 128. Longest Consecutive Sequence
* Heap／Priority Queue题目：
  * 要再做一下 用动态规划做会更好 Leetcode 264. Ugly Number II
  * 再做一遍 Leetcode 378. Kth Smallest Element in a Sorted Matrix
  * 再做一下 想一下那个思路 Leetcode 767. Reorganize String
  * 单调队列尝试再做一下 想一下思路 Leetcode 1438. Longest Continuous Subarray With Absolute Diff Less Than or Equal to Limit (这个题用单调双端队列、TreeMap、双heap都可以)


**二分法（Binary Search）：**

* 基础知识：二分法是用来解法基本模板，时间复杂度logN；常见的二分法题目可以分为两大类，显式与隐式，即是否能从字面上一眼看出二分法的特点：要查找的数据是否可以分为两部分，前半部分为X，后半部分为O
* 显式二分法：
  * Leetcode 33. Search in Rotated Sorted Array
  * Leetcode 74. Search a 2D Matrix
  * 再写一下练手 和二分法关系不大 Leetcode 240. Search a 2D Matrix II
* 隐式二分法：
  * Leetcode 69. Sqrt(x)
  * Leetcode 644. Maximum Average Subarray II
  * 再做一下 Leetcode 1060. Missing Element in Sorted Array

**双指针（2 Pointer）：**

* 基础知识：常见双指针算法分为三类，同向（即两个指针都相同一个方向移动），背向（两个指针从相同或者相邻的位置出发，背向移动直到其中一根指针到达边界为止），相向（两个指针从两边出发一起向中间移动直到两个指针相遇）
* 背向双指针：(基本上全是回文串的题)
* 相向双指针：(以two sum为基础的一系列题)
  * 再做一下 不会写 Leetcode 277. Find the Celebrity
* 同向双指针：（个人觉得最难的一类题，可以参考下这里 [TimothyL：Leetcode 同向双指针/滑动窗口类代码模板](https://zhuanlan.zhihu.com/p/390570255)）
  * 重新再写一遍 Leetcode 395. Longest Substring with At Least K Repeating Characters
  * 再写一遍 Leetcode 76. Minimum Window Substring

 **宽度优先搜索（BFS）：** 面试中最常考的

* 基础知识：
  * 常见的BFS用来解决什么问题？(1) 简单图（有向无向皆可）的最短路径长度，注意是长度而不是具体的路径（2）拓扑排序 （3） 遍历一个图（或者树）
* BFS基本模板（需要记录层数或者不需要记录层数）
* 多数情况下时间复杂度空间复杂度都是O（N+M），N为节点个数，M为边的个数
* 基于树的BFS：不需要专门一个set来记录访问过的节点
  * DFS/BFS多尝试 多做几遍 Leetcode 297 Serialize and Deserialize Binary Tree （很好的BFS和双指针结合的题）
* 基于图的BFS：（一般需要一个set来记录访问过的节点）
  * 再做一下 练手 Leetcode 127. Word Ladder
  * 再做一下 Leetcode 815. Bus Routes
  * Leetcode 417. Pacific Atlantic Water Flow
* 拓扑排序：（[https://**zh.wikipedia.org/wiki/%**E6%8B%93%E6%92%B2%E6%8E%92%E5%BA%8F](https://link.zhihu.com/?target=https%3A//zh.wikipedia.org/wiki/%25E6%258B%2593%25E6%2592%25B2%25E6%258E%2592%25E5%25BA%258F)）
  * 不会做 Leetcode 444 Sequence Reconstruction

 **深度优先搜索（DFS）：** 面试中最常考的（分类的稍微有点粗糙了，没有细分出回溯/分治来，准备找个时间给每个DFS的题标记下是哪种DFS）

* 基础知识：
  * 常见的DFS用来解决什么问题？(1) 图中（有向无向皆可）的符合某种特征（比如最长）的路径以及长度（2）排列组合（3） 遍历一个图（或者树）（4）找出图或者树中符合题目要求的全部方案
  * DFS基本模板（需要记录路径，不需要返回值 and 不需要记录路径，但需要记录某些特征的返回值）
  * 除了遍历之外多数情况下时间复杂度是指数级别，一般是O(方案数×找到每个方案的时间复杂度)
  * 递归题目都可以用非递归迭代的方法写，但一般实现起来非常麻烦
* 基于树的DFS：需要记住递归写前序中序后序遍历二叉树的模板
  * 再做一遍 挺值得思考的题目 Leetcode 1485 Clone Binary Tree With Random Pointer
  * 再做一遍 Leetcode 863 All Nodes Distance K in Binary Tree
* 二叉搜索树（BST）：BST特征：中序遍历为单调递增的二叉树，换句话说，根节点的值比左子树任意节点值都大，比右子树任意节点值都小，增删查改均为O（h）复杂度，h为树的高度；注意不是所有的BST题目都需要递归，有的题目只需要while循环即可
  * Leetcode 235 Lowest Common Ancestor of a Binary Search Tree
  * 做过不会 分治 Leetcode 669 Trim a Binary Search Tree (分治)
  * 再做一下 n的solution Leetcode 333 Largest BST Subtree (与98类似) (分治)
  * 再做一下的题目 Leetcode 285 Inorder Successor in BST (I, II)
* 基于图的DFS: 和BFS一样一般需要一个set来记录访问过的节点，避免重复访问造成死循环; Word XXX 系列面试中非常常见，例如word break，word ladder，word pattern，word search。
  * 可以再做一下 Leetcode 394 Decode String
  * 可以再做一下练手 Leetcode 51 N-Queens (I II基本相同)
  * 不会做 再做一遍 Leetcode 291 Word Pattern II (I为简单的Hashmap题)
  * 不会做 再看一遍 Leetcode 126 Word Ladder II （I为BFS题目）
  * 再做 不太会 和stack相关 Leetcode 856 Score of Parentheses
  * Leetcode 301 Remove Invalid Parentheses
  * Leetcode 212 Word Search II （I, II）
  * 再看一下思路 Leetcode 399 Evaluate Division
  * 再做一遍 练手 Leetcode 1274 Number of Ships in a Rectangle
  * 转化成树的结构 Leetcode 1376 Time Needed to Inform All Employees
  * 可以再写一下 练手Leetcode 694 Number of Distinct Islands
  * 好做 可以再做一下练手 Leetcode 131 Palindrome Partitioning
* 基于排列组合的DFS: 其实与图类DFS方法一致，但是排列组合的特征更明显
  * 可以再做一下练手 Leetcode 698 Partition to K Equal Sum Subsets
  * 排列问题 Leetcode 526 Beautiful Arrangement (similar to 46)
* 记忆化搜索（DFS + Memoization Search）：算是用递归的方式实现动态规划，递归每次返回时同时记录下已访问过的节点特征，避免重复访问同一个节点，可以有效的把指数级别的DFS时间复杂度降为多项式级别; 注意这一类的DFS必须在最后有返回值（分治法），不可以用回溯法; for循环的dp题目都可以用记忆化搜索的方式写，但是不是所有的记忆化搜索题目都可以用for循环的dp方式写。
  * Leetcode 1235 [Maximum Profit in Job Scheduling](https://link.zhihu.com/?target=https%3A//leetcode.com/explore/item/3950)
  * 做过的题目 有点难写 多做几遍 Leetcode 1335 Minimum Difficulty of a Job Schedule
  * Leetcode 403 Frog Jump

**前缀和（Prefix Sum）**

* 基础知识：前缀和本质上是在一个list当中，用O（N）的时间提前算好从第0个数字到第i个数字之和，在后续使用中可以在O（1）时间内计算出第i到第j个数字之和，一般很少单独作为一道题出现，而是很多题目中的用到的一个小技巧
* 常见题目：
  * 再做一遍 Leetcode 1031 Maximum Sum of Two Non-Overlapping Subarrays

---

以上内容皆为面试中高频的知识点，以下知识点和题目在面试中属于中等频率（大概面10道题会遇到一次），时间不足的情况下，请以准备上面的知识点为主。

**并查集（Union Find）：把两个或者多个集合合并为一个集合**

* 基础知识：如果数据不是实时变化，本类问题可以用BFS或者DFS的方式遍历，如果数据实时变化（data stream）则并查集每次的时间复杂度可以视为O（1）；需要牢记合并与查找两个操作的模板
* 常见题目：
  * Leetcode 721 Accounts Merge
  * Leetcode 547 Number of Provinces
  * Leetcode 737 Sentence Similarity II
  * Leetcode 305 Number of Islands II

**字典树（Trie）**

* 基础知识：（[https://**zh.wikipedia.org/wiki/T**rie](https://link.zhihu.com/?target=https%3A//zh.wikipedia.org/wiki/Trie)）；多数情况下可以通过用一个set来记录所有单词的prefix来替代，时间复杂度不变，但空间复杂度略高
* 常见题目：
  * Leetcode 208 Implement Trie (Prefix Tree)
  * Leetcode 211 Design Add and Search Words Data Structure
  * 再做一下 Leetcode 212 Word Search II
  * Leetcode 1166 Design File System

**单调栈与单调队列（Monotone Stack／Queue）**

* 基础知识：单调栈一般用于解决数组中找出每个数字的第一个大于／小于该数字的位置或者数字；单调队列只见过一道题需要使用；不论单调栈还是单调队列，单调的意思是保留在栈或者队列中的数字是单调递增或者单调递减的
* 常见题目：
  * Leetcode 85 Maximum Rectangle
  * 再做一下的题目 练熟template Leetcode 84 Largest Rectangle in Histogram
  * 再做一下题目 Leetcode 907 Sum of Subarray Minimums (与84类似)
  * 和84类似 Leetcode 739 Daily Temperatures
  * 可以再练一下 Leetcode 901 Online Stock Span
  * Leetcode 503 Next Greater Element II
  * Leetcode 239 Sliding Window Maximum （唯一的单调队列题）

**扫描线算法（Sweep Line）**

* 基础知识：一个很巧妙的解决时间安排冲突的算法，本身比较容易些也很容易理解
* 常见题目：
  * Leetcode 253 Meeting Room II（Meeting Room I也可以使用）
  * Leetcode 1094 Car Pooling
  * Leetcode 218 The Skyline Problem
  * Leetcode 759 Employee Free Time

**TreeMap**

* 基础知识：基于红黑树（平衡二叉搜索树）的一种树状 hashmap，增删查改、找求大最小均为logN复杂度，Python当中可以使用SortedDict替代；SortedDict继承了普通的dict全部的方法，除此之外还可以peekitem(k)来找key里面第k大的元素，popitem(k)来删除掉第k大的元素，弥补了Python自带的heapq没法logN时间复杂度内删除某个元素的缺陷；最近又在刷一些hard题目时候突然发现TreeMap简直是个神技，很多用别的数据结构写起来非常麻烦的题目，TreeMap解决起来易如反掌。
* 常见题目：
* Leetcode 729 My Calendar I
* Leetcode 981 Time Based Key-Value Store
* Leetcode 846 Hand of Straights
* Leetcode 218 The Skyline Problem
* Leetcode 480. Sliding Window Median (这个题用TreeMap超级方便)
* Leetcode 318 Count of Smaller Numbers After Self (这个题线段树、二分索引树、TreeMap都可以)

**动态规划（Dynamic Programming）**

* 基础知识：这里指的是用for循环方式的动态规划，非Memoization Search方式。DP可以在多项式时间复杂度内解决DFS需要指数级别的问题。常见的题目包括找最大最小，找可行性，找总方案数等，一般结果是一个Integer或者Boolean。动态规划有很多分支，暂时还没想好怎么去写这部分，后面想好了再具体写吧。
* 常见题目：
  * Leetcode 674 Longest Continuous Increasing Subsequence (接龙型dp)
  * Leetcode 368 Largest Divisible Subset (接龙型dp)
  * Leetcode 300 Longest Increasing Subsequence (接龙型dp)
  * 再做一遍的题目 Leetcode 354 Russian Doll Envelopes (接龙型dp， 300的2D版)
  * Leetcode 121 Best Time to Buy and Sell Stock
  * 可以再做一遍 Leetcode 132 Palindrome Partitioning II
  * Leetcode 312 Burst Balloons (区间型dp)
  * 看一下思路即可 Leetcode 1143 Longest Common Subsequence (前缀型dp)
  * 可以再练习一下二分法 和1143感觉没什么关系 Leetcode 1062 Longest Repeating Substring (dp方法与longest common substring一致)
  * 思考718和1143的区别和corner case 一个是必须接上 Leetcode 718 Maximum Length of Repeated Subarray (和1062本质上一样)
  * 再做一遍 考虑 Leetcode 174 Dungeon Game
  * 再做一遍 思考 718，1143，115 关系Leetcode 115 Distinct Subsequences
  * 承接 想一下思路Leetcode 91 Decode Ways
  * 再做一遍 Leetcode 639 Decode Ways II
  * Leetcode 712 Minimum ASCII Delete Sum for Two Strings
  * 可能在下面出现0 有点triky Leetcode 221 Maximal Square
  * 可以再写一遍 练手感 Leetcode 1277 Count Square Submatrices with All Ones (可以使用221一样的解法)
  * Leetcode 87 Scramble String
  * Leetcode 1140 Stone Game II
  * Leetcode 1048 Longest String Chain
  * 和72之类的很像 都是编辑字符串的题目 Leetcode 44 [Wildcard Matching](https://link.zhihu.com/?target=https%3A//leetcode.com/problems/wildcard-matching)
  * Leetcode 10 [Regular Expression Matching](https://link.zhihu.com/?target=https%3A//leetcode.com/problems/regular-expression-matching)
  * Leetcode 32 Longest Valid Parentheses
  * 再做一遍 再思考的题目 Leetcode 1235 Maximum Profit in Job Scheduling (DP + binary search)
  * 再做一遍 第一遍没看清题目意思 Leetcode 1043 Partition Array for Maximum Sum
  * 想想思路 和dp不太像 Leetcode 926 Flip String to Monotone Increasing
