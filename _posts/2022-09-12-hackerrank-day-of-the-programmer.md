---
layout: post
title: "[Java] HackerRank Day of the Programmer"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/day-of-the-programmer/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

class Result {
    static String dayOfProgrammer(int year) {
        String answer = "";
        if (year == 1918) {
            answer = "26.09.1918";
        } else if ((year <= 1917 && year % 4 == 0) || (year > 1918 & year % 400 == 0) || (year % 4 == 0 && year % 100 != 0)) {
            answer = "12.09." + year;
        } else {
            answer = "13.09." + year;
        }
        return answer;
    }
}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        System.out.print(Result.dayOfProgrammer(Integer.parseInt(br.readLine())));
        br.close();
    }
}
```