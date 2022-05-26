---
layout: post
title: "[Java] HackerRank Java End-of-file"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/java-end-of-file/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
import java.util.*;

public class Solution {
    public static void main(String[] args) {
        int count = 1;
        String str = "";
        Scanner scanner = new Scanner(System.in);

        while (scanner.hasNext()) {
            str = scanner.nextLine();
            System.out.println(count + " " + str);
            count++;
        }

        scanner.close();
    }

    // failed code
//    public static void main(String[] args) throws IOException {
//        int count = 1;
//        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
//        while (bufferedReader.readLine() != null) {
//            String string = bufferedReader.readLine();
//            System.out.println(count + " " + string);
//            count++;
//        }
//    }

}
```