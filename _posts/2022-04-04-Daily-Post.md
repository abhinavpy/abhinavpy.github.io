---
title: 'Daily Blog Post 4 April 2022'
date: 2022-04-04
permalink: /posts/2022/04/daily-post/
tags:
  - dynamic programming
  - interview problems
  - algorithms
  - data structures
---
## Reading Comprehension - GREEdge
- Finished Advanced Reading Comprehension Exercise 2. Scored 11/20. Need to do better. Questions were ambigious and confusing with similiar meaning options.
- Revised Essential RC Practice 1.
- Revised Essential RC Practice 2.

## CLRS - Dynamic Programming
- DP, Like Divide and Conquer solves problems by combining solutions to subproblems.
- Divide and Conquer Algorithms partition the problem into disjoint subproblems, solve the subproblems recursively, and then combine their solutions to solve the original problem.
- In contrast, DP applies when subproblems overlap-that is, when subproblems share subsubproblems. In this context a divide and conquer algorithm does more work than necessary, repeatedly solving the common subsubproblems.
- A dynamic programming algorithm solves each subsubproblem just once and then saves its answer in a table, thereby avoiding the work of recomputing the answer each time it solves each subsubproblem.
- We typically apply DP to optimization problems. Such problems can have many solutions. Each solution has a value, and we wish to find a solution with the optimal (minimum or maximum) value.
- We call such a solution an optimal solution to the problem as opposed to the optimal solution to the problem.
- When developing a dynamic-programming algorithm, we follow a sequence of four steps:
  1. Characterize the structure of an optimal solution.
  2. Recursively define the value of an optimal solution.
  3. Compute the value of an optimal solution, typically in a bottom-up fashion.
  4. Construct an optimal solution from computed information.
### Rod Cutting
The rod cutting problem is as follows given a rod of length n and a table of prices for lengths of rods. 
Determine the maximum revenue obtainable by cutting up the rod and selling the pieces.

We can cut a rod of length n in 2^(n-1) ways, since we have an independent option of cutting or not cutting, at distance i inches from the left end.
If an optimal solution cuts a rod into k pieces, for some 1<=k<=n, then an optimal decomposition n = i1 + i2 + i3 + i4 + ... + ik of the rod into pieces of lengths
i1, i2, i3, i4, i5, ..., ik provides maximum corresponding revenue rn = pi1 + pi2 + pi3 + ... + pik.

More generally, we can frame the values of rn from n >= 1 in terms of optimal revenues from shorter rods:
rn = max(pn, r1 + rn-1, r2 + rn-2, .... , rn-1 + r1).
- The first argument, pn, corresponds to making no cuts at all and selling the rod of length n as it is.
- The other n-1 arguments to max correspond to the maximum revenue obtained by making an initial cut of the rod into two pieces of size i and n - i, for each i.
- Since we don't know ahead of time which value of i optimizes revenue, we have to consider all possible values of i and pick the one that maximizes revenue.
- We also have the option of picking no i at all if we can obtain more revenue by selling the rod uncut.
- Note that to solve the original problem of size n, we solve smaller problems of the same type, but of smaller sizes. Once we make the first cut, we may consider the two pieces as independent instances of the rod-cutting problem. The overall optimal solution incorporates optimal solutions to the two related subproblems, maximizing revenue from each of those two pieces.
- We say that the rod cutting problem exhibits optimal substructure: optimal solutions to a problem incorporate optimal solutions to related subproblems, which we may solve independently.
- 

## GeeksForGeeks Practice - Arrays and Dynamic Programming
Solved about 8-10 problems.

## Quant - GREedge
- 
