---
layout: post
title: "[Java] LeetCode 1221. Split a String in Balanced Strings"
tags: [algorithms, java, leetcode]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://leetcode.com/problems/split-a-string-in-balanced-strings/>

<br>

## Solution

```java
class Solution {
    static int balancedStringSplit(String s) {
        int answer = 0;
        int cntL = 0;
        int cntR = 0;
        for (int i = 0; i < s.length(); i++) {
            if (s.charAt(i) == 'R') {
                cntR++;
            } else { // s.charAt(i) == 'L'
                cntL++;
            }

            if (cntL != 0 || cntR != 0) {
                if (cntR == cntL) {
                    answer++;
                }
            }
        }

        return answer;
    }

    public static void main(String[] args) {
        System.out.println(balancedStringSplit("RLRRLLRLRL"));
        System.out.println(balancedStringSplit("RLRRRLLRLL"));
        System.out.print(balancedStringSplit("LLLLRRRR"));
    }
}
```