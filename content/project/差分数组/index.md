---
title: 差分矩阵
date: 2024-04-20
tags:
  - acw基础
  - easy
  - 差分
  - 前缀和
---
输入一个 n 行 m列的整数矩阵，再输入 q个操作，每个操作包含五个整数 x1,y1,x2,y2,c，其中 (x1,y1)和 (x2,y2)表示一个子矩阵的左上角坐标和右下角坐标。

每个操作都要将选中的子矩阵中的每个元素的值加上 c。

请你将进行完所有操作后的矩阵输出。

#### 输入格式

第一行包含整数 n,m,q。

接下来 n 行，每行包含 m 个整数，表示整数矩阵。

接下来 q 行，每行包含 55 个整数 x1,y1,x2,y2,c，表示一个操作。

#### 输出格式

共 n 行，每行 m个整数，表示所有操作进行完毕后的最终矩阵。

#### 数据范围

1≤n,m≤1000,  
1≤q≤100000,  
1≤x1≤x2≤n,  
1≤y1≤y2≤m,  
−1000≤c≤1000,  
−1000≤矩阵内元素的值≤1000−1000≤矩阵内元素的值≤1000

#### 输入样例：

```
3 4 3
1 2 2 1
3 2 2 1
1 1 1 1
1 1 2 2 1
1 3 2 3 2
3 1 3 4 1
```

#### 输出样例：

```
2 3 4 1
4 3 4 1
2 2 2 2
```



![](https://cdn.jsdelivr.net/gh/Jessicazzzzzz/github_mypic/202404201244428.png)


```java
import java.io.*;
class Main{
    static int N= 1010;
    static int M = 1010;
    public static void main(String[] args) throws IOException{
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String[] str = reader.readLine().split(" ");
        int row = Integer.parseInt(str[0]);
        int column = Integer.parseInt(str[1]);
        int query = Integer.parseInt(str[2]);
        int[][] arr = new int[N][M];
        int[][] b = new int[N][M];
        
        for(int i = 1;i<=row;i++){
             String[] s = reader.readLine().split(" ");
            for(int j = 1;j<= column;j++){
                 arr[i][j] = Integer.parseInt(s[j-1]);
                 insert(b,i,j,i,j,arr[i][j]);
            }
        }
        while(query-->0){
            String[] s1= reader.readLine().split(" ");
        
            int x1 = Integer.parseInt(s1[0]);
            int y1 = Integer.parseInt(s1[1]);
             int x2 = Integer.parseInt(s1[2]);
            int y2 = Integer.parseInt(s1[3]);
            int c = Integer.parseInt(s1[4]);
           
            insert(b,x1,y1,x2,y2,c);
          
        }
          // 求差分数组的前缀和
          for(int i = 1;i<=row;i++){
                for(int j = 1;j<=column;j++){
                  arr[i][j] = arr[i-1][j]+arr[i][j-1]-arr[i-1][j-1]+b[i][j];
                }
            }
            for(int i = 1;i<=row;i++){
                for(int j = 1;j<=column;j++){
                    System.out.print(arr[i][j]+" ");
                }
                System.out.println();
            }
        
    }
    // 构建差分数组
    static void insert(int[][] b,int x1,int y1,int x2 ,int y2,int c){
        b[x1][y1] +=c;
        b[x1][y2+1] -=c;
        b[x2+1][y1] -=c;
        b[x2+1][y2+1] +=c;        
    }
}
```