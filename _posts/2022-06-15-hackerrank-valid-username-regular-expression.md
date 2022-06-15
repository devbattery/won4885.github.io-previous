---
layout: post
title: "[Java] HackerRank Java Reflection - Attributes"
tags: [algorithms, java, hackerrank]
gh-repo: daattali/beautiful-jekyll
comments: true
---

<https://www.hackerrank.com/challenges/java-reflection-attributes/problem?isFullScreen=true>

<br>

## Solution

```java
import java.lang.reflect.Method;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

public class Solution {

    public static void main(String[] args) {
        Class<Student> studentClass = Student.class;
        Method[] methods = studentClass.getDeclaredMethods();

        List<String> methodList = new ArrayList<>();

        for (Method m : methods) {
            methodList.add(m.getName());
        }

        Collections.sort(methodList);

        for (String name : methodList) {
            System.out.println(name);
        }
    }
}

class Student {
    private String name;
    private String id;
    private String email;

    public String getName() {
        return name;
    }

    public void setId(String id) {
        this.id = id;
    }

    public void setEmail(String email) {
        this.email = email;
    }
}
```