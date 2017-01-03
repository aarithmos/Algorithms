---
layout: post
title:  "Dynamic Programming"
author: "Dynamic Programming"
permalink: /Dynamic-Programming/
---


* #### [Longest Common Subsequence](#longest-common-subsequence-problem)



#### __Longest Common Subsequence Problem__

Given two sequences, find the length of longest subsequence present in both of them. A subsequence is a sequence that appears in the same relative order, but not necessarily contiguous. For example, “abc”, “abg”, “bdf”, “aeg”, ‘”acefg”, .. etc are subsequences of “abcdefg”. So a string of length n has 2^n different possible subsequences.

```
LCS-LENGTH(X,Y)
1 m = X.length
2 n = Y.length
3 let b[1...m,1...n] and c[0...m,0...n] be new tables
4 for i = 1 to m
5     c[i,0] = 0
6 for j = 0 to n
7     c[0,j] = 0
8 for i = 1 to m
9    for j = 1 to n
10      if x(i) == y(j)
11           c[i,j] = c[i-1,j-1] + 1
12           b[i][j] = "↖"
13      elseif c[i-1,j] >= c[i,j-1]
14           c[i,j] = c[i-1,j]
15           b[i][j] = "↑"
16      else c[i,j] = c[i,j-1]
17           b[i][j] = "←" 
18 return c and b
```
Time Complexity: __O(m*n)__ 

[BACK TO THE TOP](#top)

[![](/img/back.png)](/search)