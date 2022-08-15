---
layout: post
title: "[Java] LeetCode 1281. Subtract the Product and Sum of Digits of an Integer"
tags: [algorithms, java, leetcode]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://leetcode.com/problems/subtract-the-product-and-sum-of-digits-of-an-integer/>

<br>

## Solution

```java
class Solution {
    static int subtractProductAndSum(int n) {
        int answer = 0;

        String nStr = String.valueOf(n);
        int productDigits = 1;
        int sumDigits = 0;
        // 1. Product of digits
        for (int i = 0; i < nStr.length(); i++) {
            productDigits *= Character.getNumericValue(nStr.charAt(i));
        }

        // 2. Sum of digits
        for (int i = 0; i < nStr.length(); i++) {
            sumDigits += Character.getNumericValue(nStr.charAt(i));
        }

        answer = productDigits - sumDigits;
        return answer;
    }

    public static void main(String[] args) {
        System.out.println(subtractProductAndSum(234));
        System.out.print(subtractProductAndSum(4421));
    }
}
```