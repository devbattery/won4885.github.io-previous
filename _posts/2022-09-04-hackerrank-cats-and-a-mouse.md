---
layout: post
title: "[Java] HackerRank Cats and a Mouse"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/cats-and-a-mouse/problem?isFullScreen=true>

<br>

## Solution

```java
class Solution {
    static String catAndMouse(int x, int y, int z) {
        String answer;
        int a = Math.abs(x - z); // Math.abs(): absolute value
        int b = Math.abs(y - z);
        if (a > b) {
            answer = "Cat B";
        } else {
            if (a < b) {
                answer = "Cat A";
            } else {
                answer = "Mouse C";
            }
        }
        return answer;
    }
}
```