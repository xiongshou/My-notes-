# 树的中心

>
>
>dfs出树中每个节点往下走的最大距离d1[u] , 往上走的最大距离up[u],要想求出up[u]，需要求出往下走的次大距离d2[u]，求出这些值之后。
>
>取每个点的最长距离的最小值

## 代码





# 旅游规划

## 题意

![image-20201008190104615](https://tva1.sinaimg.cn/large/007S8ZIlly1gji4oly0idj30u01brgzg.jpg)



## 思路

> 求树中每个节点是不是经过树中的最长路径
>
> 需要求出每个节点往下走的最长路径、往下走的次长路径、往上走的最长路径。这三个属性值可以确定：经过这个点的树中最长路径。
>
> 然后比较一下，树的直径。最后输出

## 代码

```cpp
#pragma comment(linker, "/STACK:1024000000,1024000000")
#include<cstdio>
#include<cstring>
#include<algorithm>
#include<iostream>
#include<string>
#include<vector>
#include<stack>
#include<bitset>
#include<cstdlib>
#include<cmath>
#include<set>
#include<list>
#include<deque>
#include<map>
#include<queue>
using namespace std;
typedef long long ll;
typedef unsigned long long ull;
#define mst(s,_s) memset(s, _s, sizeof(s))
const double PI = acos(-1.0);
const double eps = 1e-6;
const int INF = 0x3f3f3f3f;
const int N = 1e6+100;
int T,n,m;

int h[N],ne[N],e[N],idx;
void add(int a,int b){
    e[idx]=b;
    ne[idx]=h[a];
    h[a]=idx++;
}
int d1[N],d2[N];
int p1[N],up[N];
int is_leaf[N],dist[N];
int maxd=0;

int  dfs_d(int u,int fa)
{
    
    d1[u]=d2[u]=-0x3f3f3f3f;
    for(int i=h[u];i!=-1;i=ne[i])
    {
        int j=e[i];
        if(j==fa) continue;
        int d=dfs_d(j,u)+1;
        
        if(d>d1[u])
        {
            p1[u]=j;
            d2[u]=d1[u];
            d1[u]=d;
        }
        else if(d>d2[u])
        {
            d2[u]=d;
        }
    }
    if(d1[u]==-0x3f3f3f3f) 
    {
        d1[u]=d2[u]=0;
        is_leaf[u]=1;
    }
    maxd=max(maxd,d1[u]+d2[u]);
    return d1[u];
}

void dfs_u(int u,int fa)
{
    for(int i=h[u];i!=-1;i=ne[i])
    {
        int j=e[i];
        if(j==fa) continue;
        if(p1[u]==j) up[j]=max(up[u],d2[u]) + 1;
        else{
            up[j]=max(up[u],d1[u])+1;
        }
        dfs_u(j,u);
    }
}
int main() {
    cin>>n;
    memset(h,-1,sizeof h);
    for(int i=0;i<n;i++)
    {
        int a,b;
        cin>>a>>b;
        add(a,b);
        add(b,a);
    }
    dfs_d(0,-1);
    dfs_u(0,-1);
    
    int res=0;
    for(int i=0;i<n;i++) 
        if(is_leaf[i])
            d1[i]=d2[i]=0;
    up[0]=0;
    for(int i=0;i<n;i++)
    {
        int _d3[3]={d1[i],d2[i],up[i]};
        sort(_d3,_d3+3);
        res=max(res,_d3[1]+_d3[2]);
    }
    for(int i=0;i<n;i++)
    {
        int _d3[3]={d1[i],d2[i],up[i]};
        sort(_d3,_d3+3);
        if(_d3[1] + _d3[2] ==maxd)
            cout<<i<<endl;
    }

    
    return 0;
}
```



# 杨老师的照相排列

## 题意

![image-20201009093705621](https://tva1.sinaimg.cn/large/007S8ZIlly1gjiu018m1vj30u01ao7hs.jpg)

## 思路

> 这些排列具有这些性质：越靠左上角越小，并且上面的数字个数比下面的多或者等于。
>
> 这样我们可以想象，每次小到大放数，每次放的位置，就那么几个情况：![image-20201009094008054](https://tva1.sinaimg.cn/large/007S8ZIlly1gjiu37vi6oj30h408q0tp.jpg)
>
> 然后DP[i] [j] [k] [l] [m] 表示这1行有i个数，第2行有j个数。。 。
>
> 每次转移，要保证，上一行比这一行>=.
>
> 另外，外面转移时候，“放这个位置”要保证这个行原本就有数。

## 代码

```cpp
#pragma comment(linker, "/STACK:1024000000,1024000000")
#include<cstdio>
#include<cstring>
#include<algorithm>
#include<iostream>
#include<string>
#include<vector>
#include<stack>
#include<bitset>
#include<cstdlib>
#include<cmath>
#include<set>
#include<list>
#include<deque>
#include<map>
#include<queue>
using namespace std;
typedef long long ll;
typedef unsigned long long ull;
#define mst(s,_s) memset(s, _s, sizeof(s))
const double PI = acos(-1.0);
const double eps = 1e-6;
const int INF = 0x3f3f3f3f;
const int N = 1e6+100;
int T,n,m;
int hight[N];
ll dp[33][33][33][33][33];



int main() {
    while(cin>>n)
    {
        if(!n) break;
        memset(dp,0,sizeof dp);
        memset(hight,0,sizeof hight);
        for(int i=1;i<=n;i++) cin>>hight[i];
        dp[0][0][0][0][0]=1;
        for(int i=0;i<=hight[1];i++)
            for(int j=0;j<=min(i,hight[2]);j++)
                for(int k=0;k<=min(j,hight[3]);k++)
                    for(int l=0;l<=min(hight[4],k);l++)
                        for(int m=0;m<=min(l,hight[5]);m++)
                        {
                            ll &x=dp[i][j][k][l][m];
                            if(i && i-1>=j) x+=dp[i-1][j][k][l][m];
                            if(j && j-1>=k) x+=dp[i][j-1][k][l][m];
                            if(k && k-1>=l) x+=dp[i][j][k-1][l][m];
                            if(l && l-1>=m) x+=dp[i][j][k][l-1][m];
                            if(m)      x+=dp[i][j][k][l][m-1];
                        }
    
        cout<<dp[hight[1]][hight[2]][hight[3]][hight[4]][hight[5]]<<endl;
        
    }
    
    return 0;
}
```



# 整数拼接

## 题意

给n个整数，从里面选俩个整数，一前一后拼接成一个新数，若这个新数是k的倍数，那么res++。问res多少?

## 思路

首先暴力代码

```cpp
for (int i = 0; i < n; i ++ )
    for (int j = 0; j < n; j ++ )
        if (check(a[i], a[j]))
            ans ++ ;
```

第一重循环，去不了的情况下，我们试图优化第二重循环。

第二重循环，求的是：拼接结果a[i] 在前a[j]在后是k的倍数的个数。

我们把这个数用DP处理出来。

我们先默认a[i]在前，a[j]在后,那结果为：

(a[i]*10^(len(a[j])) + a[j] ) %k ==0

化解一下：  a[i]*10^(len(a[j])) %k + a[j]  %k ==0

当我们枚举到第j个数a[j]时，得知道j之前符合上面的数的个数。

可以定义f[i] [j] ：为a[j] 之前的数，这些数^len(a[j]) 膜为j的个数。

把等式+左边的余数求出来，那我们就可以线性求出与等式+右边的余数之和为0的数。

## 代码

```cpp
#include<cstdio>
#include<cstring>
#include<algorithm>
#include<iostream>
#include<string>
#include<vector>
#include<stack>
#include<bitset>
#include<cstdlib>
#include<cmath>
#include<set>
#include<list>
#include<deque>
#include<map>
#include<queue>
using namespace std;
typedef long long ll;
typedef unsigned long long ull;
#define mst(s,_s) memset(s, _s, sizeof(s))
const double PI = acos(-1.0);
const double eps = 1e-6;
const int INF = 0x3f3f3f3f;
const int N = 1e6+100;
int a[N],T,n,m;
int f[13][N];

ll res=0;

int get(int x)
{
    int res=0;
    while(x){
        x/=10;
        res++;
    }
    return res;
}
void work()
{
    for(int i=1;i<=n;i++)
    {
        res+=f[get(a[i])][(m-(a[i]%m))%m] ;
        
        for(int j=1,t=10;j<11;j++)
        {
            
        
            f[j][1ll*a[i]*t%m] ++ ;
        
            t=t*10%m;
        }
    }
}
int main() {
    cin>>n>>m;
    for(int i=1;i<=n;i++) cin>>a[i];

    work();
    memset(f,0,sizeof f);
    reverse(a+1,a+n+1);
    work();
    cout<<res<<endl;



    return 0;
}

```

