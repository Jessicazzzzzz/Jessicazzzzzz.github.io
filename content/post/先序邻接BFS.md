+++
title = 'BFS'
date = 2024-09-28T17:38:03+10:00
draft = true
tags = ['algorithm','模版']
+++
### 先序邻接BFS
> 通过先序遍历来实现BFS,是众多代码的模版
```javascript

function BFS(root) {
  if(!root) return;
let depth = 0;
let queue = [root];
while(queue.length) {
  const next = [];  // 扩展节点
  for(let i = 0; i < queue.length; i++) {
    if(node.left) next.push(node.left);
    if(node.right) next.push(node.right);
  }
  depth++;
  queue = next;
}
}
```
