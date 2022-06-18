---
layout: post
title: "[Java] HackerRank Java List"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/java-list/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        try (Scanner scanner = new Scanner(System.in)) {
            int N = scanner.nextInt();
            List<Integer> list = new LinkedList<>();

            for (int i = 0; i < N; i++) {
                int value = scanner.nextInt();
                list.add(value);
            }

            int Q = scanner.nextInt();

            for (int i = 0; i < Q; i++) {
                String action = scanner.next();
                if (action.equals("Insert")) {
                    int index = scanner.nextInt();
                    int value = scanner.nextInt();
                    list.add(index, value);
                } else {
                    int index = scanner.nextInt();
                    list.remove(index);
                }
            }

            for (Integer num : list) {
                System.out.print(num + " ");
            }
        }
    }
}
```