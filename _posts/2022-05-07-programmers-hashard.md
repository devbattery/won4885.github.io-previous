---
layout: post
title: Programmers 하샤드 수
tags: [algorithms, java, programmers]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://programmers.co.kr/learn/courses/30/lessons/12947>

<br>

## Solution

```java
class Solution {
    public static boolean solution(int x) {
        boolean answer = false;
        int sum = 0;
        int xReal = x;

        while (true) {
            sum += x % 10;
            x /= 10;

            if (x == 0) {
                break;
            }
        }

        if (xReal % sum == 0) {
            answer = true;
        }

        return answer;
    }

    public static void main(String[] args) {
        System.out.println(solution(18));
        System.out.println(solution(10));
        System.out.println(solution(11));
        System.out.println(solution(12));
        System.out.println(solution(13));
    }
}
```
