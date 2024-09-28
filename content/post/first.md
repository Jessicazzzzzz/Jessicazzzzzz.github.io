+++
title = 'Hugo 搭建博客'
date = 2024-09-28T13:08:22+10:00
draft = true
+++
### hugo搭建博客执行步骤
下载 hugo
1. brew install hugo
创建站点
1. hugo new site myblog
2. cd myblog
3. git init
4. 找到自己想要的主题,根据步骤安装
创建博客
1. hugo new post/first.md 
2. hugo server -D
   
### 部署到gitPage 
> 先在github 上创建一个仓库,名字必须是username.github.io
> 这种方式只是将static文件直接上传到github上，而不是将整个文件夹上传,所以不用gitaction 来部署
1. cd myblog/public
2. git init
3. git add .
4. git commit -m "first commit"
5. git remote add origin https://github.com/useraname/username.github.io.git
6. git push -u origin main

