---
layout: post
title: "[Java] HackerRank Smart Number"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/smart-number/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.BufferedReader;
import java.io.IOException; 
import java.io.InputStreamReader;
import java.util.*;

public class Solution {
    public static boolean isSmartNumber(int num) {
        return (int) Math.sqrt(num) * (int) Math.sqrt(num) == num;
    }

    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        List<String> list = new ArrayList<>();
        for (int i = 0; i < n; i++) {
            if (isSmartNumber(Integer.parseInt(br.readLine()))) { // TRUE
                list.add("YES");
            } else { // FALSE
                list.add("NO");
            }
        }
        for (String s : list) {
            System.out.println(s);
        }
        br.close();
    }
}
```