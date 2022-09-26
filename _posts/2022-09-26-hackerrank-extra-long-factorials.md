---
layout: post
title: "[Java] HackerRank Extra Long Factorials"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/extra-long-factorials/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
import java.math.BigInteger;

class Result {
    public static void extraLongFactorials(int n) {
        BigInteger answer = BigInteger.valueOf(1);
        BigInteger tmp = BigInteger.valueOf(n);
        for (int i = n; i > 0; i--) {
            answer = answer.multiply(BigInteger.valueOf(i));
        }
        System.out.print(answer);
    }
}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(bufferedReader.readLine());
        Result.extraLongFactorials(n);
        bufferedReader.close();
    }
}
```