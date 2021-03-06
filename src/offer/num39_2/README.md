# 平衡二叉树

**题目**

输入一棵二叉树，判断该二叉树是否是平衡二叉树。

**测试地址**
[平衡二叉树](https://www.nowcoder.com/practice/8b3b95850edb4115918ecebdf1b4d222?tpId=13&tqId=11192&rp=2&ru=/ta/coding-interviews&qru=/ta/coding-interviews/question-ranking)

## 解题思路

最容易想到的思路是参考39_1得到二叉树的深度的思路，我们已经得到了二叉树的深度，那么只需要去比较左右子树的深度的差值是否大于1即可。

但是该方法，会对节点进行重复的遍历。因此是从上到下遍历，下层的节点每次统计平衡时候，会多次统计。

最佳解法是利用后序遍历，左、右、根的形式去查找节点，这样的话，就是从底部向上，不会有重复节点被统计。

但是因为Java的特性，无法按照剑指Offer中给出的C++那样直接去实现。`IsBalanced_Solution2`方法是牛客网`一直奔跑的蜗牛`实现的方式。
在统计深度的时候，就计算是否平衡，但也是要在外部保存一个变量在记录全局的平衡性。
此外，是否平衡也要全部都遍历一遍才清楚，对于一开始就不平衡的情况，浪费时间。

`IsBalanced_Solution3`方法是牛客网`Aurora1`提供的思路，以Java的形式去实现剑指Offer上的算法





