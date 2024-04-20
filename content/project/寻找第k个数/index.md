---
title: find k
date: 2024-04-19
tags:
  - acw基础
  - quickSort
  - easy
---
给定一个长度为 n 的整数数列，以及一个整数 k，请用快速选择算法求出数列从小到大排序后的第 k个数。

#### 输入格式

第一行包含两个整数 n 和 k。

第二行包含 n 个整数（所有整数均在 1∼1091∼109 范围内），表示整数数列。

#### 输出格式

输出一个整数，表示数列的第 k小数。

#### 数据范围

1≤n≤100000,  
1≤k≤n1

#### 输入样例：

```
5 3
2 4 1 5 3
```

#### 输出样例：

```
3
```

#### 思路分析
用快排的方式找到第k个数,为什么可以找到? 因为每次j 的位置就是排好序的pivot 的最终位置,那么寻找第k 个数,我们只要比较它跟左区间(假设是len)的距离,如果小于 len 那么就在左区间寻找,如果>len,那么就在有区间寻找k- len 的区间
```java 
import java.io.*;
class Main{
    static int N = 100010;
    static int[] a = new int[N];
    public static void main(String[] args) throws IOException{
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String[] cur = reader.readLine().split(" ");
        int n = Integer.parseInt(cur[0]);
        int k = Integer.parseInt(cur[1]);
         String[] str = reader.readLine().split(" ");
        for(int i=0;i<n;i++){
            a[i] = Integer.parseInt(str[i]);
        }
        System.out.print(findK(a,0,n-1,k));
        
    }
    
    public static int findK(int[] arr,int l ,int r,int k){
       // 如果只有一个数,那么就是要寻找的数
        if(l>=r) return arr[l];
        int m = arr[(l+r)>>1];
        int i = l-1;
        int j = r+1;
        while(i<j){
            do{
                i++;
            }while(arr[i]<m);
            do{
                j--;
            }while(arr[j]>m);
            if(i<j){
                int tem = arr[i];
                arr[i] = arr[j];
                arr[j] = tem;
            }
        }
        //确定左区间的长度
        int len = j-l+1;
        if(k<=len){// k<=len ,那么就继续在左区间寻找
           return findK(arr,l,j,k); 
        }else {
          return  findK(arr,j+1,r,k-len);
        }
       
        
    }
}
```