### 题目描述
> 给定一棵二叉搜索树，请找出其中的第k小的结点。例如， （5，3，7，2，4，6，8）    中，按结点数值大小顺序第三小结点的值为4。

### 代码
```javascript
/* function TreeNode(x) {
    this.val = x;
    this.left = null;
    this.right = null;
} */
function KthNode(root, k)
{
    if(!root) return;
    var arr = [];
     
    inorder(root,arr)
    //第k个元素就是arr[k-1]存储的节点指针
    return arr[k-1];
}
//中序遍历后就是有序序列
function inorder(root,arr) {
    if(!root) return;
     
    inorder(root.left,arr);
    arr.push(root)
    inorder(root.right,arr);
}
```