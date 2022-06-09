---
layout: post
title: "[Java] HackerRank Java 2D Array"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/java-2d-array/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        int[][] n = new int[6][6];
        int sum = 0;
        int maxSum = Integer.MIN_VALUE;

        try (Scanner scanner = new Scanner(System.in)) {
            for (int i = 0; i < 6; i++) {
                for (int j = 0; j < 6; j++) {
                    n[i][j] = scanner.nextInt();
                    if (i > 1 && j > 1) {
                        sum = n[i][j] + n[i][j - 1] + n[i][j - 2] + n[i - 1][j - 1]
                                + n[i - 2][j] + n[i - 2][j - 1] + n[i - 2][j - 2];

                        if (sum > maxSum) {
                            maxSum = sum;
                        }
                    }
                }
            }
        }

        System.out.println(maxSum);
    }
}
```