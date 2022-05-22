---
layout: post
title: "[Java] HackerRank Java Output Formatting"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/java-output-formatting/problem?isFullScreen=true>

<br>

## Solution

```java
import java.util.Scanner;

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("================================");
        for (int i = 0; i < 3; i++) {
            String s1 = sc.next();
            int x = sc.nextInt();
            System.out.printf("%-15s", s1);
            System.out.printf("%03d\n", x);
        }
        System.out.println("================================");

    }
}
```
