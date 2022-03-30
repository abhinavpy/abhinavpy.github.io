---
title: 'Daily Blog Post 30 March 2022'
date: 2022-03-30
permalink: /posts/2022/03/daily-post/
tags:
  - dynamic programming
  - interview problems
  - algorithms
  - data structures
---

Leetcode , Unique Paths , https://leetcode.com/problems/unique-paths/
There is a robot on an mxn grid The robot is initially located on the top-left corner. 
The robot tries to move to the bottom right corner. The robot can move down or right 
at any point of time.
Given two integers m and n return the possible number of unique paths that the robot
can take to reach the bottom right corner.

Solution
======
We will be examining three solutions to this problem.

Recursive (Time Limit exceeded for bigger values)
======
```
int uniquePaths(int m, int n) {
  return uniquePathsHelper(m-1, n-1);
}

int uniquePathsHelper(int m, int n) {
  if(m < 0 || n < 0) {
    return 0;
  } else if (m == 0 || n == 0) {
    return 1;
  } else {
    return uniquePathHelpers(m-1, n) + uniquePathHelpers(m, n-1);
  }
}
```


Memoization Time Complexity: mxn Space Complexity: mxn
======
```
int uniquePaths(int m, int n) {
  vector <vector<int> > dp[m][n];
  return uniquePathsHelper(m-1, n-1, dp);
}
int uniquePathsHelper(int m, int n, vector<vector<int> > &dp) {
  if(m < 0 || n < 0) return 0;
  else if(m == 0 || n == 0) return 1;
  else if(dp[n][m] > 0) return dp[n][m];
  else {
    dp[n][m] = uniquePathsHelper(m - 1, n, dp) + uniquePathsHelper(m, n - 1, dp);
    return dp[n][m];
  }
}
```

You can have many headings
======

Aren't headings cool?
------
