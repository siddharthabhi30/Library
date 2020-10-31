#include <bits/stdc++.h>
using namespace std;
#define ll int64_t
#include <cstdlib> 
#include <math.h>
#include<cstdio>
#include<cstring>
#include <math.h>
#define vi v(n) vector<ll> v(n);
#define FOR(I, A, B) for (ll I = (A); I <= (B); I++)
#define fo(i,n) for(ll i=0;i<n;i++)
#define sz(a) ll((a).size())
#define pb push_back
#define all(c) (c).begin(),(c).end()
#define dbg(x) cout << #x << " = " << x << endl
#define dbg2(x,y) cout << #x << " = " << x << ", " << #y << " = " << y << endl
#define dbg3(x,y,z) cout << #x << " = " << x << ", " << #y << " = " << y << ", " << #z << " = " << z << endl
#define dbg4(x,y,z,q) cout << #x << " = " << x << ", " << #y << " = " << y << ", " << #z << " = " << z << ", " << #q << " = " << q << endl
#define scan(char_array) scanf("%[^\n]s",&char_array)
#define IOS ios::sync_with_stdio(false); cin.tie(0); cout.tie(0);

const ll N=2000005;
g++ -o h  a.cpp && ./h < in
ll Power(ll base , ll e)
{
    if(e == 0) return 1;
    ll ans = base; e--;
    while(e)
  {
        if(e & 1) ans = (((ans%MOD) * (base%MOD)) %MOD+MOD)%MOD;
        base = (((base%MOD) * (base%MOD)) %MOD+MOD)%MOD;
        e >>= 1;
  }
  return (ans+MOD) %MOD;
}
ll primes[N];
void sieve()
{
  
  
  for(ll i=2;i<=N;i++)
  {
    if(primes[i]==-1)
    {
        for(ll j=i;j<=N;j+=i) primes[j]=i;
        
     }
   }

}

ll gcd(ll a, ll b) 
{ 
    if (b == 0) 
        return a; 
    return gcd(b, a % b);  
      
}
ll lcm(ll a,ll b){
    ll t=(a*b)/(gcd(a,b));
    return t;
}

 


factorial and inverse 
ll fact[N];
ll invfact[N];


ll Power(ll base , ll e)
{
    if(e == 0) return 1;
    ll ans = base; e--;
    while(e)
  {
        if(e & 1) ans = (((ans%MOD) * (base%MOD)) %MOD+MOD)%MOD;
        base = (((base%MOD) * (base%MOD)) %MOD+MOD)%MOD;
        e >>= 1;
  }
  return (ans+MOD) %MOD;
}

ll modinv(ll k)
    {
        return Power(k, MOD-2);
    }

void precompute()
    {
        fact[0]=fact[1]=1;
        for(ll i=2;i<N;i++)
        {
            fact[i]=fact[i-1]*i;
            fact[i]%=MOD;
        }
        invfact[N-1]=modinv(fact[N-1]);
        for(ll i=N-2;i>=0;i--)
        {
            invfact[i]=invfact[i+1]*(i+1);
            invfact[i]%=MOD;
        }
    }

    ll nCr(ll x, ll y)
    {
        if(y>x)
            return 0;
        ll num=fact[x];
        num*=invfact[y];
        num%=MOD;
        num*=invfact[x-y];
        num%=MOD;
        return num;
    }


stl 
// queue
.push
.pop
.front
.back
.emplace
.size


// deque
  .push back
  .push front
  .front
  .back
  .emplace_back



struct cmp
{
    bool operator()(ll a, ll b)
    {
        return a<b;
    }
};


//for vectors
auto compare=[](const ll a, const ll b) {return a > b;};


another compare for priority_queue
struct CustomCompare
{
    bool operator()(const int& lhs, const int& rhs)
    {
        return lhs < rhs;
    }
};



auto compare = [](int lhs, int rhs)
                {
                    return lhs < rhs;
                };

    std::priority_queue<int, std::vector<int>, decltype(compare)> q(compare);

    


compare for set

struct cmp {
    bool operator() (const pair<int, int> &a, const pair<int, int> &b) const {
        int lena = a.second - a.first + 1;
        int lenb = b.second - b.first + 1;
        if (lena == lenb) return a.first < b.first;
        return lena > lenb;
    }
};

set<pair<int, int>, cmp> segs;



//union find
ll height[N];
ll father[N];
void init() {
    for (ll i = 0;k i < N; ++i) {
        father[i] = i;
        height[i] = 0;
    }
}

ll find(ll node) {
    if (father[node] != node) {
        father[node] = find(father[node]);
    }
    return father[node];
}

void unite(ll A, ll B) {
    ll rootA = find(A);
    ll rootB = find(B);
    if (height[rootA] > height[rootB]) {
        father[rootB] = rootA;
        height[rootA] = max(height[rootA], height[rootB] + 1);
    } else {
        father[rootA] = rootB;
        height[rootB] = max(height[rootB], height[rootA] + 1);
    }
  
// 

//__builtin_popcountll()

z algo
vector<ll> z(string s) {
       ll n = s.size();
       vector<ll> z(n);
       ll x = 0, y = 0;
       for (ll i = 1; i < n; i++) {
     z[i] = max(0,min(z[i-x],y-i+1));
       while (i+z[i] < n && s[z[i]] == s[i+z[i]]) {
       x = i; y = i+z[i]; z[i]++;
       }
      }        
return z;
}



//compare function




fenwick tree
const ll N=1000005
;ll tree[N];
ll a[N];
ll n;
ll sum(ll k) {
ll s = 0;
while (k >= 1) {
s += tree[k];
k -= k&-k;
}
return s;
}
void add(ll k, ll x) {
while (k <= N) {
tree[k] += x;
k += k&-k;
}
}


//inverse and gcd

void extgcd(ll a, ll b, ll *x, ll *y) {
    ll xx, yy;
    if (b == 0) {
        *x = 1;
        *y = 0;
    } else {
        ll q = a / b;
        ll r = a % b;
        extgcd(b, r, &xx, &yy);
        *x = yy;
        *y = xx - q * yy;
    }
}
 
ll inv(ll a) {
    ll x, y;
    extgcd(a, MOD, &x, &y);
    return (x + MOD) % MOD;
}



//kosaraju and topological


const ll N=1e5+10;
stack<ll> st;
ll n,m;
vector<ll> ad[N];
vector<ll> gra[N];
bool is_loop;
ll visited[N];
void dfs(ll n){
     if(visited[n]) return;
      visited[n]=1;
     for(auto j:adj[n]){
        if(!visited[j]) dfs(j);
     }
    //cout<<"  this  "<<n<<endl;
     st.push(n);
 
 
 
}
void bfs(ll n){
    
 
    queue<ll> q;
    q.push(n);
    ll a;
    ll cnt=1;
    while(!q.empty()){
        a=q.front();
        
        visited[a]=1;
        
        q.pop();
        for(auto j:gra[a]){
             if(!visited[j]) {q.push(j); cnt++;}
        }
 
    }
    if(cnt>1) is_loop=true;
 }

 ll main(){
 
 is_loop=false;
 cin>>n>>m;
 ll tmp,tmp1;
 fo(i,m){
    cin>>tmp>>tmp1;
    adj[tmp].pb(tmp1);
    gra[tmp1].pb(tmp);


 }
 fo(i,n+1) visited[i]=0;

 FOR(i,1,n) {
    if(!visited[i]) dfs(i);
 }
fo(i,n+1) visited[i]=0;
stack<ll> st1=st;
 while(!st.empty()){
        ll tmp=st.top();
        st.pop();
        if(!visited[tmp]) bfs(tmp); 
     }
if(is_loop) {cout<<"IMPOSSIBLE"<<endl; return 0;}





trie 
// poller node can directly to reference to a node without using & ,with new node

struct trie
{ 
    trie* children[26];
    bool child[26];
  
    // isEndOfWord is true if the node represents 
    // end of a word 
    bool is;
}; 
  trie
// Returns new trie node (initialized to NULLs) 
trie* getNode(void) 
{ 
    trie* pNode =  new trie; 
  
    
  
    for (ll i = 0; i < 26; i++) {
        pNode->child[i] = false;
        pNode->children[i]=NULL; 
    }
    pNode->is=false;
  
    return pNode; 
} 



segment tree max

std::vector<ll> seg(N*4);
 
void sege(ll x,ll y,ll pos)
{
if(x==y){
    
    seg[pos]=maax[x]; 
    return;
        
}
ll mid=(x+y)/2;
sege(x,mid,2*pos +1);
sege(mid+1,y,2*pos+2);
seg[pos]=max(seg[2*pos+1],seg[2*pos+2]);

}
 
ll qr(ll x,ll y,ll lo,ll hi,ll pos)
{
 
    if(lo>=x&&hi<=y) return seg[pos];
 
    if(hi<x||lo>y) return 0;
 
    ll mid=(lo+hi)/2;
 
    return max(qr(x,y,lo,mid,2*pos+1),qr(x,y,mid+1,hi,2*pos+2));
 
}