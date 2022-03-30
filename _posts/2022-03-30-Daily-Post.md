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

# Leetcode Unique Paths
See here for Problem Link: [Unique Paths](https://leetcode.com/problems/unique-paths/)

There is a robot on an mxn grid. The robot is initially located on the top-left corner. 
The robot tries to move to the bottom right corner. The robot can move down or right 
at any point of time.
Given two integers m and n return the possible number of unique paths that the robot
can take to reach the bottom right corner.

## Solution

We will be examining three solutions to this problem.

### Recursive (Time Limit exceeded for bigger values)

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


### Memoization Time Complexity: mxn Space Complexity: mxn

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

### Dynamic Programming Tabulation

```
int uniquePaths(int m, int n) {
  vector<vector<int> > grid[m][n];
  for(int i = 0; i < n; ++i) {
    for(int j = 0; j < m; ++j) {
      if(i == 0) grid[0][j] = 1;
      if(j == 0) grid[i][j] = 1;
      if(i != 0 && j != 0) {
        int up = grid[i-1][j];
        int left = grid[i][j-1];
        grid[i][j] = up + left;
      }
    }
  }
  return grid[n-1][m-1];
}
```
# Words of the day : Vocab for GRE
1. Supplication: The action of begging for something earnestly or humbly.
2. Abrogate: to officially end a law, an agreement, etc.
3. Corpulent: Excessively fat.
4. Automaton: a person who behaves like a machine, without thinking or feeling anything.
5. Eruption: an act, or instance of eruption.
6. Pedagogue: a teacher, who is strict and pedantic.
7. Annals: an official record of events or activities year by year; historical records
8. Megalomania: a mental illness in which the person has delusions of grandeur, power, wealth, etc.
9. Obloquy: Strong public condemnation.
10. Homogeneous: consisting of things or people that are all the same or all of the same type.
11. Subterfuge: a secret, usually dishonest, way of behaving.
12. Affable: Easily approachable; friendly
13. Badger: Nagging or annoying another with incessant questions or comments.
14. Benevolent: motivated by consideration of welfare of another or others
15. Reprimand: to tell somebody officially, that you don't approve of them or their action.
16. Factitious: not genuine but created deliberately and made to appear to be true.
17. Frail: Having less than a normal amount of strength or force : very weak.
18. Gullible: Too willing to believe or accept what other people tell you and therefore easily tricked.
19. Clique: a small group of people who spend their time together and do not allow others to join them.
20. Indifference: Lack of interest, concern, or sympathy.
21. Feint: a movement tha is intended to make your opponent think you are going to do one thing when you are really going to do something else.
22. Charlatan: A person who claims to have knowledge or skill that other people do not really have.
23. Strident: unpleasantly loud and harsh.
24. Besmirch: Cause damage or harm the reputation of someone or something.
