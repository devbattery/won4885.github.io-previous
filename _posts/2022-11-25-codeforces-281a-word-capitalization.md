---
layout: post
title: "[Java] Codeforces 281A - Word Capitalization"
tags: [algorithms, java, codeforces]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://codeforces.com/problemset/problem/281/A>

<br>

## Solution

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Solution {
    public static String returnFirstLetterUpper(String input) {
        StringBuilder answer = new StringBuilder();
        answer.append(String.valueOf(input.charAt(0)).toUpperCase());
        for (int i = 1; i < input.length(); i++) {
            answer.append(input.charAt(i));
        }
        return answer.toString();
    }

    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String input = br.readLine();
        System.out.print(returnFirstLetterUpper(input));
        br.close();
    }
}
```