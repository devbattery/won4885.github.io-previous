---
layout: post
title: "[Java] HackerRank Java 1D Array"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/java-1d-array-introduction/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
import java.math.BigInteger;
import java.util.*;

public class Solution {

    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(bufferedReader.readLine());
        int[] nArr = new int[n];

        for (int i = 0; i < nArr.length; i++) {
            nArr[i] = Integer.parseInt(bufferedReader.readLine());
        }

        for (int v : nArr) {
            System.out.println(v);
        }
        bufferedReader.close();
    }
}
```