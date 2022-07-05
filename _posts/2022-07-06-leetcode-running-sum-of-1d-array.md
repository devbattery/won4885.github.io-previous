---
layout: post
title: "[Java] LeetCode 1480. Running Sum of 1d Array"
tags: [algorithms, java, leetcode]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://leetcode.com/problems/running-sum-of-1d-array/>

<br>

## Solution

```java
import java.util.Arrays;

class Solution {
    public static int[] runningSum(int[] nums) {
        for (int i = 1; i < nums.length; i++) {
            nums[i] += nums[i - 1];
        }

        return nums;
    }

    public static void main(String[] args) {
        System.out.println(Arrays.toString(runningSum(new int[]{1, 2, 3, 4})));
    }
}
```
