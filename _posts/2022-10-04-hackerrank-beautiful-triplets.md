---
layout: post
title: "[Java] HackerRank Beautiful Triplets"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/beautiful-triplets/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
import java.util.*;

class Result {
    static int beautifulTriplets(int d, List<Integer> arr) {
        int answer = 0;
        for (Integer integer : arr) {
            if (arr.contains(integer + d) && arr.contains(integer + 2 * d)) {
                answer++;
            }
        }
        return answer;
    }
}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        StringTokenizer st = new StringTokenizer(br.readLine(), " ");
        int n = Integer.parseInt(st.nextToken());
        int d = Integer.parseInt(st.nextToken());
        st = new StringTokenizer(br.readLine(), " ");
        List<Integer> arr = new ArrayList<>();
        for (int i = 0; i < n; i++) {
            arr.add(Integer.parseInt(st.nextToken()));
        }
        System.out.print(Result.beautifulTriplets(d, arr));
        br.close();
    }
}
```