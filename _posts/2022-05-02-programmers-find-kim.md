---
layout: post
title: Programmers 서울에서 김서방 찾기
tags: [algorithms, java, programmers]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://programmers.co.kr/learn/courses/30/lessons/12919>

<br>


## Solution

```java
import java.util.Objects;

class Solution {
    public static String solution(String[] seoul) {
        String answer = "";

        int num = 0;
        for (int i = 0; i < seoul.length; i++) {
            if (Objects.equals(seoul[i], "Kim")) {
                num = i;
            }
        }

        answer = "김서방은 " + num + "에 있다";

        return answer;
    }

    public static void main(String[] args) {
        System.out.println(solution(new String[]{"Kim", "Jane"}));
        System.out.println(solution(new String[]{"Jane", "Kim"}));
        System.out.println(solution(new String[]{"Jeong", "Jang", "Kim", "Jane"}));
    }
}
```
<br>

## Another Solution

```java
import java.util.Arrays;

public class FindKim {
    public String findKim(String[] seoul){
        //x에 김서방의 위치를 저장하세요.
        int x = Arrays.asList(seoul).indexOf("Kim");

        return "김서방은 "+ x + "에 있다";
    }

    // 실행을 위한 테스트코드입니다.
    public static void main(String[] args) {
        FindKim kim = new FindKim();
        String[] names = {"Queen", "Tod","Kim"};
        System.out.println(kim.findKim(names));
    }
}
```
