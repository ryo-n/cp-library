---
data:
  _extendedDependsOn: []
  _extendedRequiredBy: []
  _extendedVerifiedWith:
  - icon: ':x:'
    path: python/union_find_yosupo.test.py
    title: python/union_find_yosupo.test.py
  _pathExtension: py
  _verificationStatusIcon: ':x:'
  attributes:
    links: []
  bundledCode: "Traceback (most recent call last):\n  File \"/opt/hostedtoolcache/Python/3.9.0/x64/lib/python3.9/site-packages/onlinejudge_verify/documentation/build.py\"\
    , line 71, in _render_source_code_stat\n    bundled_code = language.bundle(stat.path,\
    \ basedir=basedir).decode()\n  File \"/opt/hostedtoolcache/Python/3.9.0/x64/lib/python3.9/site-packages/onlinejudge_verify/languages/python.py\"\
    , line 85, in bundle\n    raise NotImplementedError\nNotImplementedError\n"
  code: "class DSU:\n    '''\n    Implement (union by size) + (path compression)\n\
    \    Reference:\n    Zvi Galil and Giuseppe F. Italiano,\n    Data structures\
    \ and algorithms for disjoint set union problems\n    '''\n\n    def __init__(self,\
    \ n: int = 0):\n        self._n = n\n        self.parent_or_size = [-1] * n\n\n\
    \    def merge(self, a: int, b: int) -> int:\n        assert 0 <= a < self._n\n\
    \        assert 0 <= b < self._n\n\n        x = self.leader(a)\n        y = self.leader(b)\n\
    \n        if x == y:\n            return x\n\n        if -self.parent_or_size[x]\
    \ < -self.parent_or_size[y]:\n            x, y = y, x\n\n        self.parent_or_size[x]\
    \ += self.parent_or_size[y]\n        self.parent_or_size[y] = x\n\n        return\
    \ x\n\n    def same(self, a: int, b: int) -> bool:\n        assert 0 <= a < self._n\n\
    \        assert 0 <= b < self._n\n\n        return self.leader(a) == self.leader(b)\n\
    \n    def leader(self, a: int) -> int:\n        assert 0 <= a < self._n\n\n  \
    \      if self.parent_or_size[a] < 0:\n            return a\n\n        self.parent_or_size[a]\
    \ = self.leader(self.parent_or_size[a])\n        return self.parent_or_size[a]\n\
    \n    def size(self, a: int) -> int:\n        assert 0 <= a < self._n\n\n    \
    \    return -self.parent_or_size[self.leader(a)]\n\n    def groups(self) -> typing.List[typing.List[int]]:\n\
    \        leader_buf = [self.leader(i) for i in range(self._n)]\n\n        result:\
    \ typing.List[typing.List[int]] = [[] for _ in range(self._n)]\n        for i\
    \ in range(self._n):\n            result[leader_buf[i]].append(i)\n\n        return\
    \ list(filter(lambda r: r, result))\n"
  dependsOn: []
  isVerificationFile: false
  path: python/library/union_find.py
  requiredBy: []
  timestamp: '2020-10-29 11:20:37+09:00'
  verificationStatus: LIBRARY_ALL_WA
  verifiedWith:
  - python/union_find_yosupo.test.py
documentation_of: python/library/union_find.py
layout: document
redirect_from:
- /library/python/library/union_find.py
- /library/python/library/union_find.py.html
title: python/library/union_find.py
---
