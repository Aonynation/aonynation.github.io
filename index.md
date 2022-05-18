# Welcome to Aonynation.github.io

## 校内资源
[**初等数论.pptx**](https://raw.githubusercontent.com/Aonynation/aonynation.github.io/main/%E5%88%9D%E7%AD%89%E6%95%B0%E8%AE%BA.pptx)

教练课件，包括原根，exgcd，线性同余方程，BSGS，CRT，不定方程ax+by=c，素数判定，大整数的因子分解。

[**分治基础.pdf**](https://raw.githubusercontent.com/Aonynation/aonynation.github.io/main/%E5%88%86%E6%B2%BB%E5%9F%BA%E7%A1%80.pdf)

学长课件，题目为主，包括 根号分治，树分治，cdq 分治，整体二分，线段树分治。

[**字符串及其相关.pdf**](https://raw.githubusercontent.com/Aonynation/aonynation.github.io/main/%E5%AD%97%E7%AC%A6%E4%B8%B2.pdf)

学长课件，题目为主，字符串算法全家桶。

[**可持久化数据结构.ppt**](https://raw.githubusercontent.com/Aonynation/aonynation.github.io/main/Persistent%20Data%20Structures%201.ppt)

学长课件，可持久化线段树以及练习题。

[**计算几何.pptx**](https://raw.githubusercontent.com/Aonynation/aonynation.github.io/main/%E8%AE%A1%E7%AE%97%E5%87%A0%E4%BD%95%E5%88%9D%E6%AD%A5.pptx)

教练课件，计算几何全家桶。

[**网络流练习题.pdf**](https://raw.githubusercontent.com/Aonynation/Classppt/main/%E7%BD%91%E7%BB%9C%E6%B5%81.pdf)

学长课件，全是题目资源，没有题解。。。

[**高等数学全家桶.zip**](https://raw.githubusercontent.com/Aonynation/aonynation.github.io/main/Higher%20Mathematics.zip)

学长课件，以讲解为主，包括极限，三分，积分等。

## 校外资源

[**边三联通分量论文.pdf**](https://raw.githubusercontent.com/Aonynation/aonynation.github.io/main/%E8%BE%B9%E4%B8%89%E8%81%94%E9%80%9A%E5%88%86%E9%87%8F.pdf)

就是英文论文，休闲娱乐佳品。 /tuu

[**算法学习笔记 知乎**](https://zhuanlan.zhihu.com/p/105467597)

[**各校老师 金牌，钻石 课件**](https://github.com/hzwer/shareOI)


## Code

### 本人常用缺省源：
```cpp
#include <bits/stdc++.h>

#define file(a) freopen(a".in", "r", stdin), freopen(a".out", "w", stdout)

#define Enter putchar('\n')
#define quad putchar(' ')

signed main(void) {
  file("1");
  return 0;
}
```

### FastIO 模板：
```cpp
namespace IO {
template <class T> inline void read(T &a);
template <class T, class ...rest> inline void read(T &a, rest &...x);
template <class T> inline void write(T x);
template <class T, class ...rest> inline void write(T x, rest ...a);
}

namespace IO {
template <class T> inline void read(T &a) {
  T s = 0, t = 1;
  char c = getchar();
  while ((c < '0' || c > '9') && c != '-')
    c = getchar();
  if (c == '-')
    c = getchar(), t = -1;
  while (c >= '0' && c <= '9')
    s = (s << 1) + (s << 3) + (c ^ 48), c = getchar();
  a = s * t;
}
template <class T, class ...rest> inline void read(T &a, rest &...x) {
  read(a); read(x...);
}

template <class T> inline void write(T x) {
  if (x == 0) putchar('0');
  if (x < 0) putchar('-'), x = -x;
  int top = 0, sta[50] = {0};
  while (x)
    sta[++top] = x % 10, x /= 10;
  while (top)
   putchar(sta[top] + '0'), top --;
  return ;
}
template <class T, class ...rest> inline void write(T x, rest ...a) {
  write(x); quad; write(a...);
}
}
```
