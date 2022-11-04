---
layout: post
title: "[Java] HackerRank Two Strings"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/two-strings/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
import java.util.HashSet; 
import java.util.Set;
import java.util.stream.*;

class Result {
    static String twoStrings(String s1, String s2) {
        Set<String> strings = new HashSet<>();
        for (int i = 0; i < s1.length(); i++) {
            strings.add(String.valueOf(s1.charAt(i)));
        }
        for (int i = 0; i < s2.length(); i++) {
            if (strings.contains(String.valueOf(s2.charAt(i)))) {
                return "YES";
            }
        }
        return "NO";
    }
}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int q = Integer.parseInt(bufferedReader.readLine().trim());

        IntStream.range(0, q).forEach(qItr -> {
            try {
                String s1 = bufferedReader.readLine();

                String s2 = bufferedReader.readLine();

                String result = Result.twoStrings(s1, s2);

                bufferedWriter.write(result);
                bufferedWriter.newLine();
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        });

        bufferedReader.close();
        bufferedWriter.close();
    }
}
```