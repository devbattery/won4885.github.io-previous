---
layout: post
title: "[Java] Codeforces 236A - Boy or Girl"
tags: [algorithms, java, codeforces]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://codeforces.com/problemset/problem/236/A>

<br>

## Solution

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Solution {
    public static String isOddOrEven(String input) {
        // Odd: IGNORE HIM!
        // Even: CHAT WITH HER!
        String tmp = "";
        for (int i = 0; i < input.length(); i++) {
            if (input.indexOf(input.charAt(i)) == i) {
                tmp += input.charAt(i);
            } 
        } 
        return (tmp.length() % 2 == 0) ? "CHAT WITH HER!" : "IGNORE HIM!";
    }

    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String input = br.readLine();
        System.out.print(isOddOrEven(input));
        br.close();
    }
}
```