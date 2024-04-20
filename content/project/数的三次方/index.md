---
title: 求一个浮点数的三次方
date: 2024-04-20
tags:
  - acw基础
  - easy
  - 二分
---
给定一个浮点数 n，求它的三次方根。

#### 输入格式

共一行，包含一个浮点数 n。

#### 输出格式

共一行，包含一个浮点数，表示问题的解。

注意，结果保留 6 位小数。

#### 数据范围

−10000≤n≤10000

#### 输入样例：

```
1000.00
```

#### 输出样例：

```
10.000000
```

```java 

import java.io.*;


class Main {

 public static void main(String[] args ) throws IOException{
    BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
    double n = Double.parseDouble(reader.readLine());
    double l = -10000;
    double r = 10000;
    while(r-l>1e-8){
    double m = (l+r)/2; // 浮点数注意不要习惯性使用>>1 
     if(m*m*m>n)r = m;
     else l = m;
    }
    System.out.printf("%.6f",l);
 
 }

}

```