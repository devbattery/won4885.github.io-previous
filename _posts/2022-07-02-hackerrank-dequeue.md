---
layout: post
title: "[Java] HackerRank Java Dequeue"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/java-dequeue/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        try (Scanner sc = new Scanner(System.in)) {
            Deque<Integer> deque = new ArrayDeque<>();
            Set<Integer> set = new HashSet<>();

            int n = sc.nextInt();
            int m = sc.nextInt();
            int max = Integer.MIN_VALUE;

            for (int i = 0; i < n; i++) {
                int input = sc.nextInt();

                deque.add(input);
                set.add(input);

                if (deque.size() == m) {
                    if (set.size() > max) {
                        max = set.size();
                    }

                    int first = deque.remove();
                    if (!deque.contains(first)) {
                        set.remove(first);
                    }
                }
            }

            System.out.println(max);
        }
    }
}
```