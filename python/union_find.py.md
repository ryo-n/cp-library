---
data:
  _extendedDependsOn: []
  _extendedRequiredBy: []
  _extendedVerifiedWith: []
  _pathExtension: py
  _verificationStatusIcon: ':warning:'
  attributes:
    links: []
  bundledCode: "Traceback (most recent call last):\n  File \"/opt/hostedtoolcache/Python/3.8.5/x64/lib/python3.8/site-packages/onlinejudge_verify/documentation/build.py\"\
    , line 70, in _render_source_code_stat\n    bundled_code = language.bundle(stat.path,\
    \ basedir=basedir).decode()\n  File \"/opt/hostedtoolcache/Python/3.8.5/x64/lib/python3.8/site-packages/onlinejudge_verify/languages/python.py\"\
    , line 84, in bundle\n    raise NotImplementedError\nNotImplementedError\n"
  code: "class UnionFind():\n    def __init__(self, n):\n        self.n = n\n    \
    \    self.parents = [-1] * n\n\n    def find(self, x):\n        if self.parents[x]\
    \ < 0:\n            return x\n        else:\n            self.parents[x] = self.find(self.parents[x])\n\
    \            return self.parents[x]\n\n    def union(self, x, y):\n        x =\
    \ self.find(x)\n        y = self.find(y)\n\n        if x == y:\n            return\n\
    \n        if self.parents[x] > self.parents[y]:\n            x, y = y, x\n\n \
    \       self.parents[x] += self.parents[y]\n        self.parents[y] = x\n\n  \
    \  def size(self, x):\n        return -self.parents[self.find(x)]\n\n    def same(self,\
    \ x, y):\n        return self.find(x) == self.find(y)\n    \n    def members(self,\
    \ x):\n        root = self.find(x)\n        return [i for i in range(self.n) if\
    \ self.find(i) == root]\n\n    def roots(self):\n        return [i for i, x in\
    \ enumerate(self.parents) if x < 0]\n\n    def group_count(self):\n        return\
    \ len(self.roots())\n\n    def all_group_members(self):\n        return {r: self.members(r)\
    \ for r in self.roots()}\n\n    def __str__(self):\n        return '\\n'.join('{}:\
    \ {}'.format(r, self.members(r)) for r in self.roots())\n\n"
  dependsOn: []
  isVerificationFile: false
  path: python/union_find.py
  requiredBy: []
  timestamp: '2020-09-17 16:42:12+09:00'
  verificationStatus: LIBRARY_NO_TESTS
  verifiedWith: []
documentation_of: python/union_find.py
layout: document
redirect_from:
- /library/python/union_find.py
- /library/python/union_find.py.html
title: python/union_find.py
---
