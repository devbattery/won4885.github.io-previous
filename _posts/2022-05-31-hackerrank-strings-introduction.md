---
layout: post
title: "[Java] HackerRank Java Strings Introduction"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/java-strings-introduction/problem?isFullScreen=true>

<br>

## Solution

```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String A = sc.next();
        String B = sc.next();

        //Step one
        System.out.println(A.length() + B.length());

        // Step two
        if (A.compareTo(B) > 0) {
            System.out.println("Yes");
        } else {
            System.out.println("No");
        }

        // Step three
        String[] arrA = A.split("");
        arrA[0] = arrA[0].toUpperCase();

        String[] arrB = B.split("");
        arrB[0] = arrB[0].toUpperCase();

        A = String.join("", arrA);
        B = String.join("", arrB);

        System.out.println(A + " " + B);

        sc.close();
    }
}
```

<br>

## Another Solution

```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String A = sc.next();
        String B = sc.next();
        System.out.println(A.length() + B.length());
        System.out.println(A.compareTo(B) > 0 ? "Yes" : "No");
        System.out.println(A.substring(0, 1).toUpperCase() + A.substring(1, A.length()) + " " + B.substring(0, 1).toUpperCase() + B.substring(1, B.length()))
        sc.close();
    }
}
```