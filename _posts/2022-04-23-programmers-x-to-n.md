---
layout: post
title: "[Java] Programmers x만큼 간격이 있는 n개의 숫자"
tags: [algorithms, java, programmers]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://programmers.co.kr/learn/courses/30/lessons/12954>

<br>

잘 풀리지 않다가 "X만큼 간격이 있는 n개의 숫자"의 제목에서 ⚽식이 떠오름


## Solution

```java
import java.util.Arrays;

public class Solution {
    public static long[] solution(int x, int n) {
        long[] answer = new long[n];

        answer[0] = x;
        for (int i = 0; i < n - 1; i++) {
            answer[i + 1] = answer[i] + x; // ⚽
        }

        return answer;
    }

    public static void main(String[] args) {
        System.out.println(Arrays.toString(solution(2, 5)));
        System.out.println(Arrays.toString(solution(4, 3)));
        System.out.println(Arrays.toString(solution(-4, 2)));

    }
}

```
