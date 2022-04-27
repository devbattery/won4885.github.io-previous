---
layout: post
title: Programmers 짝수와 홀수
tags: [algorithms, java, programmers]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://programmers.co.kr/learn/courses/30/lessons/12937>

<br>

## Solution

```java
class Solution {
    public static String solution(int num) {
        String answer = "";

        if (num % 2 == 0) { // Even
            answer = "Even";
        } else { // Odd
            answer = "Odd";
        }

        return answer;
    }

    public static void main(String[] args) {
        System.out.println(solution(3));
        System.out.println(solution(4));
    }
}
```

<br>

## Another Solution

```java
public class EvenOrOdd {
    String evenOrOdd(int num) {
        return num % 2 == 0 ? "Even": "Odd";
    }

    public static void main(String[] args) {
        //String str = "1 2 3 4";
        EvenOrOdd evenOrOdd = new EvenOrOdd();
        System.out.println("결과 : " + evenOrOdd.evenOrOdd(3));
        System.out.println("결과 : " + evenOrOdd.evenOrOdd(2));
    }
}
```
