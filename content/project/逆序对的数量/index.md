---
title: 逆序对的数量
date: 2024-04-19
tags:
  - acw基础
  - 归并排序
  - easy
---
给定一个长度为 n 的整数数列，请你计算数列中的逆序对的数量。

逆序对的定义如下：对于数列的第 i� 个和第 j� 个元素，如果满足 i<j 且 a[i]>a[j]，则其为一个逆序对；否则不是。

#### 输入格式

第一行包含整数 n，表示数列的长度。

第二行包含 n 个整数，表示整个数列。

#### 输出格式

输出一个整数，表示逆序对的个数。

#### 数据范围

1≤n≤100000，  
数列中的元素的取值范围 [1,109][1,109]。

#### 输入样例：

```
6
2 3 4 5 6 1
```

#### 输出样例：

```
5
```

> 思路
> 每次归并排序的时候, 
```java 
class Main{
public static void main(String[] args) throws IOException{

   BufferedReader reader = new BufferedReader(new InputStreamReader(System.in()));
   int n = Integer.parseInt(reader.readLine());
   String[] str = reader.readLine().split(" ");
   int[] arr = new int[n];
   for(int i =0;i<n;i++){
    arr[i] = Integer.parseInt(str[i]);
   }
   long r = mergeSort(arr,0,n-1);
   System.out.print(r);
}
static long mergeSort(int[] arr,int l, int r){
if(l>=r) return 0;
int m = (l+r)>>1;
Long res = mergeSort(arr,l,m)+mergeSort(arr,m+1,r);
int i = l;
int j = m+1;
int k = 0;
int[] temp = new int[r-l+1];
while(i<=m&& j <=r){
if(arr[i]<=arr[j]){
 temp[k++] = arr[i++];
}else{
 temp[k++] = arr[j++];
 res += m-i+1; // l-m 这个区间已经是有序的了并且i-m 之间的数都是大于arr[j]的
}
}
while(i<=m) temp[k++] = arr[i++];
while(j<=r) temp[k++] =arr[j++];
for(int h = 0;h<k;h++){ // 因为k是后++ ,所以最终的k 一定是数组的长度,所以不能是等于
 arr[h+l] = temp[h];
}
return res;
 }


}
```