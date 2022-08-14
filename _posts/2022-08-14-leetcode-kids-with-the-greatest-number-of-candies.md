---
layout: post
title: "[Java] LeetCode 1431. Kids With the Greatest Number of Candies"
tags: [algorithms, java, leetcode]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/>

<br>

## Solution

```java
import java.util.ArrayList;
import java.util.List;

class Solution {
    static List<Boolean> kidsWithCandies(int[] candies, int extraCandies) {
        List<Boolean> answer = new ArrayList<>();
        int max = 0;
        for (int candy : candies) {
            max = Math.max(candy, max);
        }
        for (int candy : candies) {
            answer.add(candy + extraCandies >= max);
        }
        return answer;
    }

    public static void main(String[] args) {
        System.out.println(kidsWithCandies(new int[]{2, 3, 5, 1, 3}, 3));
        System.out.println(kidsWithCandies(new int[]{4, 2, 1, 1, 2}, 1));
        System.out.print(kidsWithCandies(new int[]{12, 1, 12}, 10));
    }
}
```