# The Maximum Unreachable Node Set

## 题意

有向无环图中，求最多能选出多少个点集合：任意俩点，都互不联通。

求一个：最少路径重复点覆盖问题。每一条路径是一个点集合。其最少路径数=点数-最大匹配数

## 代码

```cpp
#include<bits/stdc++.h>
using namespace std;
const int N=500;
int match[N];
int st[N];
int g[N][N];
int n,m;
void floyd()
{
    for (int k = 1; k <= n; k ++ )
        for (int i = 1; i <= n; i ++ )
            for (int j = 1; j <= n; j ++ )
                g[i][j] |= g[i][k] & g[k][j];
    

    
}

bool find(int x)
{
    for(int i=1;i<=n;i++)
    {
        if(st[i]) continue;
        
        if(g[x][i]==0) continue;
        st[i]=1;
        if(!match[i] || find(match[i]))
        {
            match[i]=x;
            return true;
        }
    }
    return false;
}
int main()
{
    cin>>n>>m;
    for(int i=0;i<m;i++)
    {
        int a,b;
        cin>>a>>b;
        g[a][b]=1;
        //g[b][a]=1;
    }
    floyd();
    int res=0;
    for(int i=1;i<=n;i++)
    {
        memset(st,0,sizeof st);
        if(find(i))
            res++;
    }
    cout<<n-res<<endl;
    return 0;
}
```

