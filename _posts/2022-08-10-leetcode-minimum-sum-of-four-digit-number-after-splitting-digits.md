---
layout: post
title: "[Java] LeetCode 2160. Minimum Sum of Four Digit Number After Splitting Digits"
tags: [algorithms, java, leetcode]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://leetcode.com/problems/minimum-sum-of-four-digit-number-after-splitting-digits/>

<br>

## Solution

```java
import java.util.Arrays;

class Solution {
    static int minimumSum(int num) {
        char[] arrCharNum = String.valueOf(num).toCharArray();
        Arrays.sort(arrCharNum);
        return Integer.parseInt("" + arrCharNum[0] + arrCharNum[2]) + Integer.parseInt("" + arrCharNum[1] + arrCharNum[3]);
    }

    public static void main(String[] args) {
        System.out.println(minimumSum(2932)); // Ascending order -> 2239
        System.out.print(minimumSum(4009)); // Ascending order -> 0049
    }
}
```
