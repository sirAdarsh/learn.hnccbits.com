---
title: "D-BS-01 (Beginner)"
linkTitle: "D-BS-01 (Beginner)"
weight: 1
description: >
  D-BS-01 (Beginner)
---

{{% pageinfo %}}
Upper Bound/ Lower bound 
{{% /pageinfo %}}

**READ BEFORE YOU TRY:**

http://www.cplusplus.com/reference/algorithm/lower_bound/
http://www.cplusplus.com/reference/algorithm/upper_bound/

**CRUNCH:**

*Upper bound* returns pointer to the first element which is just greater than the searched element.
*Lowe bound* returns pointer to the first element which is equal to or greater than the searched element.

If *it* is the pointer to that is returned by the upper or lower bound, then its index can be derived by : *it*-*vec.begin()*, assuming the vector<int> vec as the search space.

If *it==vec.end()*, this means the upper/lower bound could not be found.


**PROBLEM**

https://codeforces.com/gym/295323/problem/E


**SOLUTION**

*Link to accepted code* : https://codeforces.com/gym/295323/submission/93077349


**EXPLAINATION**

*We* simply maintained a vector of prefix sums in the *vector<int> pre*, so whatever volume of water we are given, we can just *Binary Search* for the volume in the array *pre*  when it gets filled. Now vector *pre* will be a increasingly sorted array, hence *pre[i]* will contain the voulume of water which can be stored upto the pool *i*. 
*Therefore*, we will just have to search for the first pool which could not store a given volume of water, hence *upper_bound* will work swiftly in this case.