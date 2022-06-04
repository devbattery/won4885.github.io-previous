---
layout: post
title: "[Java] HackerRank Java String Tokens"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/java-string-tokens/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        String str = bufferedReader.readLine();

        if (str.trim().length() < 1 || str.trim().length() > 4 * Math.pow(10, 5)) {
            return;
        }

        String[] strArr = str.trim().split("[ !,?._'@]+");
        int count = strArr.length;
        System.out.println(count);
        for (String value : strArr) {
            System.out.println(value);
        }
    }
}
```