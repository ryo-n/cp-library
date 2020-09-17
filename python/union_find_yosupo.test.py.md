---
data:
  _extendedDependsOn:
  - icon: ':heavy_check_mark:'
    path: python/library/union_find.py
    title: python/library/union_find.py
  _extendedRequiredBy: []
  _extendedVerifiedWith: []
  _pathExtension: py
  _verificationStatusIcon: ':heavy_check_mark:'
  attributes:
    PROBLEM: https://judge.yosupo.jp/problem/unionfind
    links:
    - https://judge.yosupo.jp/problem/unionfind
  bundledCode: "Traceback (most recent call last):\n  File \"/opt/hostedtoolcache/Python/3.8.5/x64/lib/python3.8/site-packages/onlinejudge_verify/documentation/build.py\"\
    , line 70, in _render_source_code_stat\n    bundled_code = language.bundle(stat.path,\
    \ basedir=basedir).decode()\n  File \"/opt/hostedtoolcache/Python/3.8.5/x64/lib/python3.8/site-packages/onlinejudge_verify/languages/python.py\"\
    , line 84, in bundle\n    raise NotImplementedError\nNotImplementedError\n"
  code: "# verify-helper: PROBLEM https://judge.yosupo.jp/problem/unionfind\n\nfrom\
    \ python.library.union_find import UnionFind\n\ndef main():\n    N, Q = [int(x)\
    \ for x in input().split()]\n    uf = UnionFind(N)\n    for _ in range(Q):\n \
    \       t, u, v = [int(x) for x in input().split()]\n        if t == 0:\n    \
    \        uf.union(u, v)\n        else:\n            print(int(uf.same(u, v)))\n\
    \n    \nif __name__ == \"__main__\":\n    main()\n"
  dependsOn:
  - python/library/union_find.py
  isVerificationFile: true
  path: python/union_find_yosupo.test.py
  requiredBy: []
  timestamp: '2020-09-17 16:46:42+09:00'
  verificationStatus: TEST_ACCEPTED
  verifiedWith: []
documentation_of: python/union_find_yosupo.test.py
layout: document
redirect_from:
- /verify/python/union_find_yosupo.test.py
- /verify/python/union_find_yosupo.test.py.html
title: python/union_find_yosupo.test.py
---
