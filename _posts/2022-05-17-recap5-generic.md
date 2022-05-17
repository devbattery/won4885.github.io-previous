---
layout: post
title: "[자료구조] Generic 프로그래밍"
tags: [java, recap]
gh-repo: daattali/beautiful-jekyll
comments: true
---

**제너릭 프로그래밍**

 

제너릭 프로그래밍은 다양한 자료형의 객체에 대해 작성한 코드를 재사용한다는 객체 지향 기법입니다.

```java
// 정렬 알고리즘 예시
public class ss{
	public int[] superSort(int[] array){
		// ...sort...
		return array;
	}
}
```

위와 같은 정렬 알고리즘이 있다고 합시다. 이 정렬 함수를 int 외의 다른 자료형에 대해 사용하려면 어떻게 해야 할까요? 제너릭 프로그래밍이 없었다면 int를 String, Person 등 문자열, 원하는 객체로 바꿔야 했을 것입니다. 제너릭 프로그래밍의 목표는 1가지의 코드만 작성해서 이를 다른 자료형에 대해 재사용할 수 있게 만드는 겁니다.

<br>

**매개변수화 타입**

 

제너릭 프로그래밍을 구현하기 위한 방법으로 매개변수화 타입을 사용할 수 있습니다. 꺾쇠괄호<> 안에 Type Parameter를 넣어 컴파일 시 구체적인 타입이 결정되도록 하는 방법입니다.


이렇게 매개변수화 타입을 사용하려면 클래스, 함수를 정의할 때 아래와 같이 고쳐주어야 합니다. 다만, 생성자의 경우 예외적으로 E를 사용하지 않습니다. 

```java
// 클래스
public class LinkedList
public class LinkedLilst<E>

// 함수
public void addFirst(String S)
public void addFirst(E obj)

public String removeFirst()
public E removeFirst()
```
<br>

예시로, 매개변수화 타입을 사용하여 어떤 자료형이든 담을 수 있는 제너릭 노드를 만들면 다음과 같습니다. 아래 코드에서 E는 모두 같은 자료형을 의미합니다.

```java
// 제너릭 노드
class Node<E>{
	E data;
	Node<E> next;
	public Node(E obj){
		data=obj;
		next=null;
	}
}
```

<br>

배열의 경우, 다음과 같이 정의합니다.

```java
// 배열
E[] storage = (E[]) new Object[size];
```

<br>

아래 코드처럼 정의하면 컴파일이 되지 않습니다.

```java
// 배열 (컴파일 X)
E[] storage = new E[size];
```

<br>

[**Source**](https://www.boostcourse.org/cs204/joinLectures/145114)