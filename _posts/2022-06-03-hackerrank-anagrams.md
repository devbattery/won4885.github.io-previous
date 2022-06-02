---
layout: post
title: "[Java] HackerRank Java Anagrams"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/java-anagrams/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.Arrays;

public class Solution {

    static boolean isAnagram(String a, String b) {
        String A = a.toUpperCase();
        String B = b.toUpperCase();

        char[] arrA = A.toCharArray();
        char[] arrB = B.toCharArray();

        Arrays.sort(arrA);
        Arrays.sort(arrB);

        return Arrays.equals(arrA, arrB);
    }

    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        String a = bufferedReader.readLine();
        String b = bufferedReader.readLine();

        System.out.println(isAnagram(a, b) ? "Anagrams" : "Not Anagrams");

        bufferedReader.close();
    }
}
```