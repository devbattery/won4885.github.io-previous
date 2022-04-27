---
layout: post
title: Programmers 자릿수 더하기
tags: [algorithms, java, programmers]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://programmers.co.kr/learn/courses/30/lessons/12931>

<br>


## Solution

```java
import java.util.*;

public class Solution {
    public static int solution(int n) {
        int answer = 0;

        while (true) {
            answer += n % 10;
            n /= 10;

            if (n == 0) {
                break;
            }
        }
        return answer;
    }

    public static void main(String[] args) {
        System.out.println(solution(123));
    }
}
```
