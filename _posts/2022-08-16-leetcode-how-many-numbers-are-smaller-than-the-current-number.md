---
layout: post
title: "[Java] LeetCode 1365. How Many Numbers Are Smaller Than the Current Number"
tags: [algorithms, java, leetcode]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://leetcode.com/problems/how-many-numbers-are-smaller-than-the-current-number/>

<br>

## Solution

```java
import java.util.Arrays;

class Solution {
    static int[] smallerNumbersThanCurrent(int[] nums) {
        int[] answer = new int[nums.length];
        int cnt = 0;
        for (int i = 0; i < nums.length; i++) {
            for (int j = 0; j < nums.length; j++) {
                if (i == j) {
                    continue;
                }

                if (nums[i] > nums[j]) {
                    cnt++;
                }
            }
            answer[i] = cnt;
            cnt = 0;
        }

        return answer;
    }

    public static void main(String[] args) {
        System.out.println(Arrays.toString(smallerNumbersThanCurrent(new int[]{6, 5, 4, 8})));
        System.out.print(Arrays.toString(smallerNumbersThanCurrent(new int[]{7, 7, 7, 7})));
    }
}
```