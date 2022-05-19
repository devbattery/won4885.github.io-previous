---
layout: post
title: "[Java] LeetCode 1929. Concatenation of Array"
tags: [algorithms, java, leetcode]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://leetcode.com/problems/concatenation-of-array/>

<br>

## Solution

```java
import java.util.Arrays;

class Solution {
    public static int[] getConcatenation(int[] nums) {
        int[] answer = new int[nums.length * 2];

        for (int i = 0; i < nums.length; i++) {
            answer[i] = nums[i];
        }

        for (int i = nums.length; i < ans.length; i++) {
            answer[i] = nums[i - nums.length];
        }

        return answer;
    }

    public static void main(String[] args) {
        System.out.println(Arrays.toString(getConcatenation(new int[]{1, 2, 1})));
    }
}
```

<br>

## Another Solution

```java
import java.util.Arrays;

class Solution {
    public int[] getConcatenation(int[] nums) {
        int[] answer = new int[nums.length * 2];
        for (int i = 0; i < nums.length; i++) {
            // result[i + nums.length] = result[i] = nums[i];
            answer[i] = nums[i];
            answer[i + nums.length] = answer[i]; // or nums[i]; (both are equal)
        }
        return result;
    }
}
```
