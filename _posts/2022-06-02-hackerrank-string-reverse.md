---
layout: post
title: "[Java] HackerRank Java String Reverse"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/java-string-reverse/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        String str = bufferedReader.readLine();
        String answer = "Yes";
        char left; char right;

        for (int i = 0; i < str.length() / 2; i++) {
            left = str.charAt(i);
            right = str.charAt(str.length() - 1 - i);

            if (left != right) {
                answer = "No";
            }
        }

        System.out.println(answer);
        bufferedReader.close();
    }
}
```

<br>

## Another Solution

```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        String A = bufferedReader.readLine();
        System.out.println(A.equals(new StringBuilder(A).reverse().toString())
                ? "Yes" : "No");
        bufferedReader.close();
    }
}
```