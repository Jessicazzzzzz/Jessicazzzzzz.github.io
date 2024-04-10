---
title: 快速排序
summary: 快排实现一个整数数列的排序
tags:
  - acw基础
date: '2024-04-10'
---
给定你一个长度为 n 的整数数列。

请你使用快速排序对这个数列按照从小到大进行排序。

并将排好序的数列按顺序输出。

#### 输入格式

输入共两行，第一行包含整数 n。

第二行包含 n 个整数（所有整数均在 1∼1091∼109 范围内），表示整个数列。

#### 输出格式

输出共一行，包含 n个整数，表示排好序的数列。

#### 数据范围

1≤n≤1000001≤n≤100000

#### 输入样例：

```
5
3 1 2 4 5
```

#### 输出样例：

```
1 2 3 4 5
```

> 快排思路
> 首先是找到一个数p, 使得这个数所有左边的值都小于等于p,右边的数都大于等于p 
> 递归直到整个数组都有序

```java 
import java.util.*;
import java.io.*;
public class Main{
public static void main(String[] args) throws IOException{
   BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
 int n = Integer.parseInt(reader.readLine());
 String[] strs = reader.readLine().split(" ");
 int[] arr = new int[n];
 for(int i = 0;i<n;i++){
  arr[i] = Integer.parseInt(strs[i]);
 }
 reader.close();
 quickSort(arr,0,arr.length-1);
 for(int i = 0;i<n;i++){
 System.out.print(arr[i]+" ");
 }

}
  static void quickSort(int[] arr, int l,int r){
     // 递归返回值
     // 如果只有一个数了,那么就返回
     if(l>=r) return ;
     int i = l-1;
     int j = r+1;
     int pivot = arr[l+r >>1];
    
    while( i<j){
      while(arr[++i]<pivot); // 左边的值小,i++
      while(arr[--j]>pivot);  // 右边的值大,j--
      if(i<j){ // 在合法的区间,如果有不符合条件的值,就交换
        int tem = arr[i];
        arr[i] = arr[j];
        arr[j] = tem;
      }
    }
    quickSort(arr,l,j);
    quickSort(arr,j+1,r);
  }

}
```
