---
title: 二进制中1的个数
date: 2024-04-20
tags:
  - acw基础
  - 位运算
---
给定一个长度为 n的数列，请你求出数列中每个数的二进制表示中 11 的个数。

#### 输入格式

第一行包含整数 n。

第二行包含 n 个整数，表示整个数列。

#### 输出格式

共一行，包含 n 个整数，其中的第 i 个数表示数列中的第 i 个数的二进制表示中 11 的个数。

#### 数据范围

1≤n≤100000,  
0≤数列中元素的值≤109

#### 输入样例：

```
5
1 2 3 4 5
```

#### 输出样例：

```
1 1 2 1 2
```


>  利用计算机的原理 
>  计算机中定义一个正整数为x , 负数为-x ,
>  负数-x 是反码+1 即为补码
>  x       111110
>  ~x    000001
>  ~x+1 00 0010 
>  x        1 1 1 1 10
>  &        000010 找到一个1 了 
>  那么就用x - 这个1 ,一直减到 0 ,那么就是有这么多个1
```java 
import java.io.*;

class Main{
    static final int N= 100010;
    static int[] a = new int[N];
    public static void main(String[] args ) throws IOException{
        BufferedReader in = new BufferedReader(new InputStreamReader(System.in));
        int len = Integer.parseInt(in.readLine());
        String[] str = in.readLine().split(" ");
     
        for(int i = 0; i< len;i++){
               int res = 0;
            a[i] = Integer.parseInt(str[i]);
             while(a[i]>0){
               a[i] -= lowbit(a[i]) ;
               res++;
            }
            System.out.print(res+" ");
        }
        
       
    }
    static int lowbit(int n){
        return n & -n;
    }
}
```