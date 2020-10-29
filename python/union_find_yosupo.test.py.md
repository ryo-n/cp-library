---
data:
  _extendedDependsOn:
  - icon: ':x:'
    path: python/library/union_find.py
    title: python/library/union_find.py
  _extendedRequiredBy: []
  _extendedVerifiedWith: []
  _pathExtension: py
  _verificationStatusIcon: ':x:'
  attributes:
    PROBLEM: https://judge.yosupo.jp/problem/unionfind
    links:
    - https://judge.yosupo.jp/problem/unionfind
  bundledCode: "Traceback (most recent call last):\n  File \"/opt/hostedtoolcache/Python/3.9.0/x64/lib/python3.9/site-packages/onlinejudge_verify/documentation/build.py\"\
    , line 71, in _render_source_code_stat\n    bundled_code = language.bundle(stat.path,\
    \ basedir=basedir).decode()\n  File \"/opt/hostedtoolcache/Python/3.9.0/x64/lib/python3.9/site-packages/onlinejudge_verify/languages/python.py\"\
    , line 85, in bundle\n    raise NotImplementedError\nNotImplementedError\n"
  code: "# verify-helper: PROBLEM https://judge.yosupo.jp/problem/unionfind\n\nfrom\
    \ python.library.union_find import DSU\n\ndef main():\n    N, Q = [int(x) for\
    \ x in input().split()]\n    uf = DSU(N)\n    for _ in range(Q):\n        t, u,\
    \ v = [int(x) for x in input().split()]\n        if t == 0:\n            uf.merge(u,\
    \ v)\n        else:\n            print(int(uf.same(u, v)))\n\n    \nif __name__\
    \ == \"__main__\":\n    main()\n"
  dependsOn:
  - python/library/union_find.py
  isVerificationFile: true
  path: python/union_find_yosupo.test.py
  requiredBy: []
  timestamp: '2020-10-29 11:20:37+09:00'
  verificationStatus: TEST_WRONG_ANSWER
  verifiedWith: []
documentation_of: python/union_find_yosupo.test.py
layout: document
redirect_from:
- /verify/python/union_find_yosupo.test.py
- /verify/python/union_find_yosupo.test.py.html
title: python/union_find_yosupo.test.py
---
