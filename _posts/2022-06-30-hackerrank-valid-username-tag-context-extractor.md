---
layout: post
title: "[Java] HackerRank Tag Content Extractor"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/tag-content-extractor/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
import java.util.*;
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Solution {

    public static void main(String[] args) {
       try (Scanner sc = new Scanner(System.in)) {
           int testCases = Integer.parseInt(sc.nextLine());

           while (testCases-- > 0) {
               String line = sc.nextLine();
               boolean matchFound = false;
               Pattern r = Pattern.compile("<(.+)>([^<]+)</\\1>");
               Matcher m = r.matcher(line);

               while (m.find()) {
                   System.out.println(m.group(2));
                   matchFound = true;
               }

               if (!matchFound) {
                   System.out.println("None");
               }
           }
       }
    }
}
```