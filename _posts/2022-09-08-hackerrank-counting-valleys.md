---
layout: post
title: "[Java] HackerRank Counting Valleys"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/counting-valleys/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
class Result {
    public static int countingValleys(int steps, String path) {
        int valleys = 0, count = 0;
        char[] pathChar = path.toCharArray();
        for (int i = 0; i < path.length(); i++) {
            if (pathChar[i] == 'U') {
                count++;
            } else if (pathChar[i] == 'D') {
                count--;
            }

            if (count == 0 && pathChar[i] =='U') {
                valleys++;
            }
        }
        return valleys;
    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int steps = Integer.parseInt(bufferedReader.readLine().trim());

        String path = bufferedReader.readLine();

        int result = Result.countingValleys(steps, path);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}
```