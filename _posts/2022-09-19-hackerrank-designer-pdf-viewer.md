---
layout: post
title: "[Java] HackerRank Designer PDF Viewer"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/designer-pdf-viewer/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
import java.util.*;
import java.util.stream.*;
import static java.util.stream.Collectors.toList;

class Result {
    static int designerPdfViewer(List<Integer> h, String word) {
        int answer = 0;
        char[] charWord = word.toCharArray();
        for (char c : charWord) {
            if (h.get(c - 97) > answer) {
                answer = h.get(c - 97);
            }
        }
        answer *= charWord.length;
        return answer;
    }
}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        List<Integer> h = Stream.of(bufferedReader.readLine().replaceAll("\\s+$", "").split(" "))
                .map(Integer::parseInt)
                .collect(toList());

        String word = bufferedReader.readLine();

        int result = Result.designerPdfViewer(h, word);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}
```