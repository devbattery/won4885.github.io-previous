---
layout: post
title: "[Java] HackerRank Drawing Book"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/drawing-book/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

class Result {
    static int pageCount(int n, int p) {
        int answer = 0;
        int half = n / 2;
        if (p > half) {
            int reverse = n - p;
            if (reverse > 1) {
                answer = reverse / 2;
            } else if (n % 2 == 0 && reverse == 1) {
                answer = 1;
            }
        } else if (p > 1) {
            answer = p / 2;
        }
        return answer;
    }
}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        int p = Integer.parseInt(br.readLine());
        System.out.print(Result.pageCount(n, p));
        br.close();
    }
}
```