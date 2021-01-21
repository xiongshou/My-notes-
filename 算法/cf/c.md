# k-Amazing Numbers（思维）

## 思路

数组a[n] 中，k从1到n。求出序列：a[1 -- k], a[2 -- k+1] , a[3 -- k+2],都出现的数的最小值。

设x都出现在这些区间，那么这些x之间的位置差最大d[x] <k,第一个x的位置<=k,最后一个x的位置>=n+1-k.



d[x] = k：x需要的k值 ， 那么k，k+1，k+2-- n的值都是x，

定义f[] 记录k k+1 k+2。--  n 



```cpp
#include <bits/stdc++.h>
using namespace std;
const int N=1e6+100;
int n, a[N], d[N],k[N];
//只能覆盖比最大距离大的段 
int main()
{
	int t;
	cin >> t;
	while(t--)
	{
		cin >> n;
		memset(d, 0, sizeof(d));
		memset(last, 0, sizeof(last));
		memset(k, 0, sizeof(k));
		for(int i = 1; i <= n; i++) cin >> a[i];
		for(int i = 1; i <= n; i++)
		{
			d[a[i]] = max(d[a[i]], i - last[a[i]]);
			last[a[i]] = i;
		}
		for(int i = 1; i <= n; i++)
		{
			if(last[i]) d[i] = max(d[i], n + 1 - last[i]);
		}
		for(int i = 1; i <= n; i++)
		{
			if(!d[i]) continue;
			for(int j = d[i]; j <= n; j++)
			{
				if(k[j]) break;
				k[j] = i;
			}
		} 
		for(int i = 1; i <= n; i++) 
		{
			if(k[i]) cout << k[i] << ' ';
			else cout << - 1 << ' ';
		}
		cout << endl;
	}
	return 0;
}
```



