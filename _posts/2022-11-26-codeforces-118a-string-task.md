---
layout: post
title: "[Java] Codeforces 118A - String Task"
tags: [algorithms, java, codeforces]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://codeforces.com/problemset/problem/118/A>

<br>

## Solution

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Solution {
    public static String returnDeleteVowels(String input) {
        StringBuilder answer = new StringBuilder();
        char[] inputArray = input.toLowerCase().toCharArray();
        for (char c : inputArray) {
            if (c == 'a' || c == 'o' || c == 'y' || c == 'e' || c == 'u' || c == 'i') {
                continue;
            }
            answer.append(".");
            answer.append(c);
        }
        return answer.toString();
    }

    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String input = br.readLine();
        System.out.print(returnDeleteVowels(input));
        br.close();
    }
}
```