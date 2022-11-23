---
layout: post
title: "[Java] Codeforces 339A - Helpful Maths"
tags: [algorithms, java, codeforces]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://codeforces.com/problemset/problem/339/A>

<br>

## Solution

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

public class Solution {
    public static String sortSum(String input) {
        StringBuilder answer = new StringBuilder();
        List<String> onlyNumList = new ArrayList<>();
        for (int i = 0; i < input.length(); i++) {
            if (input.charAt(i) != '+') {
                onlyNumList.add(String.valueOf(input.charAt(i)));
            }
        }
        Collections.sort(onlyNumList);
        for (int i = 0; i < onlyNumList.size(); i++) {
            answer.append(onlyNumList.get(i));
            if (i == onlyNumList.size() - 1) {
                break;
            }
            answer.append("+");
        }
        return answer.toString();
    }

    public static void main(String[] args) throws IOException { 
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String input = br.readLine();
        System.out.print(sortSum(input));
        br.close();
    }
}
```