+++
title = '后序邻接DFS'
date = 2024-09-28T19:54:30+10:00
draft = true
tags = ['algorithm','模版']
+++
### 后序邻接DFS
> 树的高度,后序模版,由未知点到已知节点的路径

```javascript
function maxDepth(root) {
  const dfs = (node) => {
    if(!node) return 0;
    const left = dfs(node.left);
    const right = dfs(node.right);
    return Math.max(left, right) + 1;
  }
return dfs(root);
}

```

