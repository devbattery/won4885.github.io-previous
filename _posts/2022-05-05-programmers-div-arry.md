---
layout: post
title: "[Java] Programmers 나누어 떨어지는 숫자 배열"
tags: [algorithms, java, programmers]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://programmers.co.kr/learn/courses/30/lessons/12910>

<br>

## Solution

```java
import java.util.ArrayList;
import java.util.Collections;

class Solution {
    public static ArrayList<Integer> solution(int[] arr, int divisor) {
        ArrayList<Integer> answer = new ArrayList<>();

        for (int i = 0; i < arr.length; i++) {
             if (arr[i] % divisor == 0) {
                 answer.add(arr[i]);
             }
        }

        if (answer.isEmpty()) {
            answer.add(-1);
        }

        Collections.sort(answer); // ascending sort
        return answer;
    }

    public static void main(String[] args) {
        System.out.println(solution(new int[]{5, 9, 7, 10}, 5));
        System.out.println(solution(new int[]{2, 36, 1, 3}, 1));
        System.out.println(solution(new int[]{2, 3, 6}, 10));
    }
}
```
<br>

## Another Solution

```java
import java.util.Arrays;

class Solution {
  public int[] solution(int[] arr, int divisor) {
          int[] answer = Arrays.stream(arr).filter(factor -> factor % divisor == 0).toArray();
          if(answer.length == 0) answer = new int[] {-1};
          java.util.Arrays.sort(answer);
          return answer;
  }
}
```
