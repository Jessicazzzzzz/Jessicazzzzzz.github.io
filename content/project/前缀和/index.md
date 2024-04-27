---
title: 前缀和
date: 2024-04-20
summary: 通过前缀和，快速求区间和
tags:
  - acw基础
  - easy
  - 前缀和
---
输入一个长度为 n 的整数序列。

接下来再输入 m 个询问，每个询问输入一对 l,r。

对于每个询问，输出原序列中从第 l 个数到第 r 个数的和。

#### 输入格式

第一行包含两个整数 n和 m。

第二行包含 n个整数，表示整数数列。

接下来 m 行，每行包含两个整数 l 和 r，表示一个询问的区间范围。

#### 输出格式

共 m 行，每行输出一个询问的结果。

#### 数据范围

1≤l≤r≤n,  
1≤n,m≤100000,  
−1000≤数列中元素的值≤1000−1000≤数列中元素的值≤1000

#### 输入样例：

```
5 3
2 1 3 6 4
1 2
1 3
2 4
```

#### 输出样例：

```
3
6
10
```


> 前缀和
> 将数组中的值转换到另一个数组中,使得新的数组中的值是元素数组的和 
> arr = [1,3,,4,5]
> s[0] = 0  设置这个是防止下标越界,可以少做个判断
> s[1] = arr[0]+s[0]
> s[2] = arr[1]+s[1]
> s[3] = arr[2]+s[2]
> ...
> s[i] = arr[i-1]+s[i-1];
> 为什么要这么做? 这样做是为了优化求区间和
> 如果我们想起arr的下标为3-1之间的数的和,正常的做法是循环一遍每个都加一个,那么时间复杂度就是logN ,但是如果我们有了前缀和,那么就可以使用s[3]-s[0]得到,时间复杂度将是log1
> s[r] = a[0]+a[1]+a[2]+...+a[l-1]+a[l]+a[l+1]+...+a[r-1];
> s[l-1] = a[0]+a[1]+a[2]+...+a[l-1]
> s[r]-s[l-1] = a[l]+...a[r-1];


```java 
import java.io.*;
class Main{
    public static void main(String[] args) throws IOException{
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String[] s1 = reader.readLine().split(" ");
        int n = Integer.parseInt(s1[0]);
        int q = Integer.parseInt(s1[1]);
        String[] s2 = reader.readLine().split(" ");
        int[] arr = new int[n];
        int[] sum = new int[n+1];
        sum[0] = 0;
        for(int i = 0;i < n;i++){
            arr[i] = Integer.parseInt(s2[i]);
            sum[i+1] = sum[i]+arr[i];
        }
        for(int j = 0;j <= n;j++){
            System.out.print(sum[j]+" ");
        }
       while(q-->0){
           String[] s = reader.readLine().split(" ");
           int l= Integer.parseInt(s[0]);
            int r= Integer.parseInt(s[1]);
          int res = sum[r]-sum[l-1];
          System.out.println(res);
       }
        
    }
    
}
```