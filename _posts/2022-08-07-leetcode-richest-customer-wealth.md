---
layout: post
title: "[Java] LeetCode 1672. Richest Customer Wealth"
tags: [algorithms, java, leetcode]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://leetcode.com/problems/richest-customer-wealth/>

<br>

## Solution

```java
class Solution {
    static int maximumWealth(int[][] accounts) {
        int max = Integer.MIN_VALUE;
        for (int i = 0; i < accounts.length; i++) {
            int tmp = 0;
            for (int j = 0; j < accounts[i].length; j++) {
                tmp += accounts[i][j];
            }

            if (tmp > max) {
                max = tmp;
            }
        }

        return max;
    }
}
```
