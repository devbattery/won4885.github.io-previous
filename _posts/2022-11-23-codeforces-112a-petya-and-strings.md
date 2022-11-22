---
layout: post
title: "[Java] Codeforces 112A - Petya and Strings"
tags: [algorithms, java, codeforces]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://codeforces.com/problemset/problem/112/A>

<br>

## Solution

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Solution {
    public static int solution(String input1, String input2) {
        return Integer.compare(input1.toLowerCase().compareTo(input2.toLowerCase()), 0);
    }

    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String input1 = br.readLine();
        String input2 = br.readLine();
        System.out.print(solution(input1, input2));
        br.close();
    }
}
```