---
layout: post
title: Programmers 같은 숫자는 싫어
tags: [algorithms, java, programmers]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://programmers.co.kr/learn/courses/30/lessons/12906>

<br>

## Solution

```java
import java.util.*;

public class Solution {
    public static ArrayList<Integer> solution(int[] arr) {
        ArrayList<Integer> answer = new ArrayList<>();

        for (int i = 0; i < arr.length - 1; i++) {
            if (arr[i] == arr[i + 1]) {
                if (i == arr.length - 2) { // last
                    answer.add(arr[i + 1]);
                }
                continue; // key point
            } else {
                answer.add(arr[i]);
                if (i == arr.length - 2) { // last
                    answer.add(arr[i + 1]);
                }
            }

        }

        return answer;
    }

    public static void main(String[] args) {
        System.out.println(solution(new int[]{1, 1, 3, 3, 0, 1, 1}));
        System.out.println(solution(new int[]{4, 4, 4, 3, 3}));
        System.out.println(solution(new int[]{4, 4, 4, 3, 2, 1}));

    }
}
```
<br>

## Another Solution

```java
import java.util.*;

public class Solution {
    public int[] solution(int []arr) {
        ArrayList<Integer> tempList = new ArrayList<Integer>();
        int preNum = 10;
        for(int num : arr) {
            if(preNum != num)
                tempList.add(num);
            preNum = num;
        }       
        int[] answer = new int[tempList.size()];
        for(int i=0; i<answer.length; i++) {
            answer[i] = tempList.get(i).intValue();
        }
        return answer;
    }
}
```
