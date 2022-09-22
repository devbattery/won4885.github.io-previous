---
layout: post
title: "[Java] HackerRank Beautiful Days at the Movies"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/beautiful-days-at-the-movies/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

class Result {
//    int i: the starting day number
//    int j: the ending day number
//    int k: the divisor
    static int beautifulDays(int i, int j, int k) {
        int answer = 0;
        for (int l = i; l <= j; l++) {
            StringBuilder sbTmp = new StringBuilder();
            sbTmp.append(l).reverse();
            int tmp = Integer.parseInt(String.valueOf(sbTmp));
            if (Math.abs(l - tmp) % k == 0) {
                answer++;
            }
        }
        return answer;
    }
}

class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine(), " ");
        int i = Integer.parseInt(st.nextToken());
        int j = Integer.parseInt(st.nextToken());
        int k = Integer.parseInt(st.nextToken());
        System.out.print(Result.beautifulDays(i, j, k));
        br.close();
    }
}
```