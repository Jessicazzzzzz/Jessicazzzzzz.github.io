---
title: 归并排序
date: 2024-04-17
tags:
  - acw基础
  - 归并排序
  - easy
---
给定你一个长度为 n 的整数数列。

请你使用归并排序对这个数列按照从小到大进行排序。

并将排好序的数列按顺序输出。

#### 输入格式

输入共两行，第一行包含整数 n。

第二行包含 n个整数（所有整数均在 1∼1091∼109 范围内），表示整个数列。

#### 输出格式

输出共一行，包含 n� 个整数，表示排好序的数列。

#### 数据范围

1≤n≤100000

#### 输入样例：

```
5
3 1 2 4 5
```

#### 输出样例：

```
1 2 3 4 5
```

```java
import java.io.*;
public class Main{
    
    public static void main(String[] args) throws IOException{
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(reader.readLine());
        String[] str = reader.readLine().split(" ");
        int[] arr = new int[n];
        for(int i = 0;i<n;i++){
        
           arr[i] = Integer.parseInt(str[i]);
        }
        mergeSort(arr,0,n-1);
        for(int i= 0;i<n;i++){
            
            System.out.print(arr[i]+" ");
        }
        reader.close();
    }
    
    public static void mergeSort(int[] arr,int l,int r){
        // 如果相等,就返回
        if(l>=r) return;
        int m = l+r>>1;
        // 递归,相当于是分治
        mergeSort(arr,l,m);
        mergeSort(arr,m+1,r);
        // 定义左右指针
        int i = l;
        int j = m+1;
        int k = 0;
        // 定义临时数组
        int[] temp = new int[r-l+1];
        // 将左右两个区间按从小到大的顺序排序
        while(i<=m && j <= r) {
            if(arr[i]<arr[j]){
                temp[k++] = arr[i++];
            }else{
                temp[k++] = arr[j++];
            }
            
        }
        // 左右数组若有剩余,需要继续扫入数组
        while(i<=m) temp[k++] = arr[i++];
        while(j<=r) temp[k++] =arr[j++];
        // 再将临时数组中的数据复原
        for(int h=0;h<k;h++){
            arr[h+l] = temp[h];
        }
   
    }
    
    
}
```