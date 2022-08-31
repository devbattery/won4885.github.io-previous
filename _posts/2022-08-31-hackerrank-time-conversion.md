---
layout: post
title: "[Java] HackerRank Time Conversion"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/time-conversion/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

class Result {
    static String timeConversion(String s) {
        String answer = "";
        int hour = Integer.parseInt(s.substring(0, 2)) % 12;
        if (s.contains("PM")) {
            hour += 12;
        }
        if (hour < 10) {
            answer = "0" + hour + s.substring(2, 8);
        } else {
            answer = hour + s.substring(2, 8);
        }
        return answer;
    }
}

class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String s = br.readLine();
        System.out.print(Result.timeConversion(s));
        br.close();
    }
}
```