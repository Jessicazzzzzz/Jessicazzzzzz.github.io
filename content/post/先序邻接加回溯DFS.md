+++
title = '先序邻接加回溯DFS'
date = 2024-09-28T19:38:01+10:00
draft = true
tags = ['algorithm','模版']
+++
### 先序邻接加回溯DFS
> 通过先序遍历来实现DFS，是众多代码的模版

```javascript
var maxDepth= function(root) {
  let maxDepth = 0;
  let depth = 0;
const dfs = (node) => {
  // catch 1
// 没有无效节点,就无法使用,只能用catch2
  if(!node) return maxDepth = Math.max(depth, maxDepth);
  // forward
  depth++;
// catch 2 
//  maxDepth = Math.max(depth, maxDepth
  dfs(node.left);
  dfs(node.right);
// backward 
  depth--;
}
dfs(root);
return maxDepth;

}