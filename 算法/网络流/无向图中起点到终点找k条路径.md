# 图中不重复K条路

## 题意

无向图中起点到终点找出不重复的K条路，求出这K条路中的最长路径的最小值。

## 思路

最大中的最小。看能不能二分。

二分最长路径，二分取值mid，若judge函数，可以定义为能不能找出K条路。

0-mid中的路径，mid值越大越可能找出K条路

现在的问题就是：能不能用最大流判断出0-mid长度走出K条路

## 处理

每次把一条边中权重小于mid的边，f[i] = 1,else f[i]=0。然后走网络流，因为容量为1，那么这些路肯定不重复。

## 代码

```cpp
#include<iostream>
#include<cstring>
using namespace std;
const int N = 210,M =80010,INF = 1e8;
int h[N],e[M],ne[M],w[M],f[M],idx;
int d[N],q[N],cur[N];
int n,m,S,T,K;
void add(int a,int b,int c){
    e[idx] = b,w[idx] = c,ne[idx] = h[a],h[a] = idx++;
    e[idx] = a,w[idx] = c,ne[idx] = h[b],h[b] = idx++;
}
bool bfs(){
    memset(d,-1,sizeof d);
    int hh = 0,tt = 0;
    d[S] = 0,q[0] = S,cur[S] = h[S];
    while(hh<=tt){
        int t = q[hh++];
        for(int i = h[t];i!=-1;i = ne[i]){
            int j = e[i];
            if(d[j] == -1&&f[i]){
                d[j] = d[t] + 1;
                cur[j] = h[j];
                if(j == T) return true;
                q[++tt] = j;
            }
        }
    }
    return false;
}
int find(int u,int limit){
    if(u == T) return limit;
    int flow = 0;
    for(int i = cur[u];i!=-1&&flow<limit;i = ne[i]){
        cur[u] = i;
        int j = e[i];
        if(d[j] == d[u] + 1&&f[i]){
            int t = find(j,min(f[i],limit - flow));
            if(!t) d[j] = -1;
            else flow +=t,f[i] -= t,f[i^1] += t;
        }
    }
    return flow;
}
int dinic(){
    int r = 0,flow;
    while(bfs()) while(flow = find(S,INF)) r += flow;
    return r;
}
bool check(int mid){
    for(int i = 0;i<idx;i++){
        if(w[i]>mid) f[i] = 0;
        else f[i] = 1;
    }
    int res = dinic();
    return res >= K;
}
int main(){
    memset(h,-1,sizeof h);
    scanf("%d%d%d",&n,&m,&K);
    S = 1,T = n;
    for(int i = 1;i<=m;i++){
        int a,b,c;
        scanf("%d%d%d",&a,&b,&c);
        add(a,b,c);
    }
    int l = 1,r = 1e6;
    while(l<r){
        int mid = (l + r)>>1;
        if(check(mid)) r = mid;
        else l = mid + 1;
    }
    cout<<r<<endl;
    return 0;
}
```

