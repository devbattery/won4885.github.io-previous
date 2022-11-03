---
layout: post
title: "[Java] HackerRank Strange Counter"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/strange-code/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;

class Result {
    static long strangeCounter(long t) {
        long t1 = 2, v1 = 3, answer = 0;
        while (t1 < t) {
            t1 += v1;
            v1 *= 2;
        }
        answer = (t1 - 1) % t;
        if (answer == 0) {
            answer = v1;
        }
        return answer;
    }
}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        long t = Long.parseLong(bufferedReader.readLine().trim());

        long result = Result.strangeCounter(t);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}
```