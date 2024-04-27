---
title: 区间和
summary: 利用离散化的方式 ,实现区间和
date: 2024-04-20
tags:
  - acw基础
  - 离散化
  - 二分
  - 前缀和
---
假定有一个无限长的数轴，数轴上每个坐标上的数都是 00。

现在，我们首先进行 n次操作，每次操作将某一位置 x 上的数加 c。

接下来，进行 m 次询问，每个询问包含两个整数 l和 r，你需要求出在区间 [l,r] 之间的所有数的和。

#### 输入格式

第一行包含两个整数 n和 m。

接下来 n 行，每行包含两个整数 x 和 c。

再接下来 m行，每行包含两个整数 l 和 r。

#### 输出格式

共 m 行，每行输出一个询问中所求的区间内数字和。

#### 数据范围

−109≤x≤109,  
1≤n,m≤105,  
−109≤l≤r≤109,  
−10000≤c≤10000

#### 输入样例：

```
3 3
1 2
3 6
7 5
1 3
4 6
7 8
```

#### 输出样例：

```
8
0
5
```

![](https://cdn.jsdelivr.net/gh/Jessicazzzzzz/github_mypic/202404201729218.png)

![](https://cdn.jsdelivr.net/gh/Jessicazzzzzz/github_mypic/202404201741464.png)
```java
import java.util.*;
class Main{
    static final int N = 300010;
    public static void main(String[] args){
        
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int m = sc.nextInt();
        int[] a = new int[N];
        int[] s = new int[N];
        List<Integer> alls = new ArrayList<>();
        // add 是存放数组下标和数组值的
        List<Pair> add = new ArrayList<>();
        List<Pair> query = new ArrayList<>();
        for(int i = 0;i<n;i++){
            int x = sc.nextInt();
            int c = sc.nextInt();
            add.add(new Pair(x,c));
            alls.add(x);
        }
        
        for(int i =0;i<m;i++){
            int l = sc.nextInt();
            int r = sc.nextInt();
            query.add(new Pair(l,r));
            alls.add(l);
            alls.add(r);
        }
        
        Collections.sort(alls); // alls 排序
        int unique = unique(alls); // 去重,返回alls 的长度
        alls = alls.subList(0,unique); // 再重新赋值给alls
        // 将alls 中值对应到a数组中去
        // find 是返回alls 中下标+1 ,这个是为了方便做前缀和
        for(Pair item:add){
            int index = find(item.first,alls);
            a[index] += item.second;
        }
        // 获取a数组的前缀和
        for(int i = 1;i<=alls.size();i++) s[i]= s[i-1]+a[i];
        for(Pair item:query){
            int l = find(item.first,alls);
            int r = find(item.second,alls);
            System.out.println(s[r]-s[l-1]);
        }
    }
    
    public static int unique(List<Integer> list){
        int j= 0;
        for(int i= 0;i<list.size();i++){
            if(i==0 || list.get(i) !=list.get(i-1)){
                list.set(j,list.get(i));
                j++;
            }
        }
        return j;
    }
    
    public static int find(int x,List<Integer> list){
        int l = 0;
        int r = list.size()-1;
        while(l<r){
            int mid = l+r >>1;
            if(list.get(mid)>=x)r = mid;
            else l =mid+1;
        }
        return l+1;
    }
    
}

class Pair {
     int first ;
     int second ;
     public Pair(int x,int c ){
         this.first = x;
         this.second = c;
     }
}
```