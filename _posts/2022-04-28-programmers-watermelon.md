---
layout: post
title: "[Java] Programmers 수박수박수박수박수박수?"
tags: [algorithms, java, programmers]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://programmers.co.kr/learn/courses/30/lessons/12922>

<br>


## Solution

```java
class Solution {
    public static String solution(int n) {
        String answer = "";

        for (int i = 1; i <= n; i++) {
            if (i % 2 == 0) { // Even
                answer += "박";
            } else { // Odd
                answer += "수";
            }
        }

        return answer;
    }

    public static void main(String[] args) {
        System.out.println(solution(3));
        System.out.println(solution(7));
        System.out.println();
        System.out.println(solution(2));
        System.out.println(solution(4));
    }
}
```
