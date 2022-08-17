---
layout: post
title: "[Java] LeetCode 1678. Goal Parser Interpretation"
tags: [algorithms, java, leetcode]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://leetcode.com/problems/goal-parser-interpretation/>

<br>

## Solution

```java
class Solution {
    static String interpret(String command) {
        return command.replaceAll("\\(\\)", "o").replaceAll("\\(al\\)", "al");
    }

    public static void main(String[] args) {
        System.out.println(interpret("G()(al)"));
        System.out.print(interpret("G()()()()(al)"));
    }
}
```