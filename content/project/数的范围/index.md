---
title: 寻找数的范围
date: 2024-04-20
tags:
  - acw基础
  - easy
  - 二分
---
给定一个按照升序排列的长度为 n 的整数数组，以及 q 个查询。

对于每个查询，返回一个元素 k的起始位置和终止位置（位置从 00 开始计数）。

如果数组中不存在该元素，则返回 `-1 -1`。

#### 输入格式

第一行包含整数 n和 q，表示数组长度和询问个数。

第二行包含 n个整数（均在 1∼100001∼10000 范围内），表示完整数组。

接下来 q 行，每行包含一个整数 k，表示一个询问元素。

#### 输出格式

共 q 行，每行包含两个整数，表示所求元素的起始位置和终止位置。

如果数组中不存在该元素，则返回 `-1 -1`。

#### 数据范围

1≤n≤100000
1≤q≤10000
1≤k≤10000

#### 输入样例：

```
6 3
1 2 2 3 3 4
3
4
5
```

#### 输出样例：

```
3 4
5 5
-1 -1
```


```java 

import java.io.*;
class Main{
    public static void main(String[] args) throws IOException{
     BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
     String[] str1 = reader.readLine().split(" ");
     String[] str2 = reader.readLine().split(" ");
     int n = Integer.parseInt(str1[0]);
     int m = Integer.parseInt(str1[1]);
     int[] arr = new int[n];
     for(int i = 0;i< n ;i++){
         arr[i] = Integer.parseInt(str2[i]);
     }
      while(m-->0){
        int j = Integer.parseInt(reader.readLine());
        find(arr,0,n-1,j);
     }
 static void find(int[] arr,int l,int r,int n){
    int i = l;
    int j = r;
    while(i<j){  // 寻找最左边的数
  int m = i+j>>1;
   if(arr[m]>=n)j=m; 
   else i = m+1;
    }
    if(arr[i]!=n)System.out.print("-1 -1"); // 当找到最后一个数的时候,不等于n ,就表示不存在
    else {
     int left = l;// keep the left number
     i = l ;
     j = r;
     while(i<j){ // 寻找最右边的数
    int  m = i+j+1>>1;
     if(arr[m]<=n) i = m;
     else j = m-1; 
     
     
     }
    System.out.print(left+" "+i);
     
    }
   
   
	 }
 }

```