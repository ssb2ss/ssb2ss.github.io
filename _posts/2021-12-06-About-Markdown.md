---
layout: post
title: "About Markdown"
date:   2021-12-06 18:00:00 +0900
categories: jekyll update
comments: true
---

Markdown은 일반 텍스트로 서식이 있는 문서를 작성하는 대표적인 방법이다.  
본 글 또한 Markdown으로 작성되었다.

# 목차

1. [글자 효과](#-글자-효과)  
  1.1. [제목](##-제목)  
  1.2. [굵게](##-굵게)  
  1.3. [기울임꼴](##-기울임꼴)  
  1.4. [취소선](##-취소선)  
2. [리스트](#-리스트)  
  2.1. [순서 없는 리스트](##-순서-없는-리스트)  
  2.2. [순서 있는 리스트](##-순서-있는-리스트)  
3. [코드](#-코드)  
  3.1. [한 줄 코드](##-한-줄-코드)  
  3.2. [코드 블럭](##-코드-블럭)  
4. [마무리](#-마무리)

# 글자 효과

Markdown으로는 다양한 글자 효과를 표현할 수 있다.  
그 중 일부는 다음과 같다.

## 제목

`제목(Header)` 표현 형식을 사용해 다음과 같은 큰 글씨를 작성할 수 있다.  
# Header 1
## Header 2
### Header 3
제목을 작성하는 방법은 다음과 같다.  
```markdown
# Header 1
## Header 2
### Header 3
```

## 굵게

`굵게(Bold)` 표현 방식을 사용해 다음과 같은 굵은 글씨를 작성할 수 있다.  
__Hello.__  
**Nice to meet you.**  
굵은 글씨를 작성하는 방법은 다음과 같다.
```markdown
__Hello.__
**Nice to meet you.**
```

## 기울임꼴

`기울임꼴(Italic)` 표현 방식을 사용해 다음과 같은 기울인 글씨를 작성할 수 있다.  
_Hello._
*Nice to meet you.*
기울임꼴을 작성하는 방법은 다음과 같다.  
```markdown
_Hello._
*Nice to meet you.*
```

## 취소선

`취소선(Strikethrough)` 표현 방식을 사용해 다음과 같은 취소선을 작성할 수 있다.  
~~Hello.~~  
취소선을 작성하는 방법은 다음과 같다.
```markdown
~~Hello.~~
```

# 리스트

Markdown으로는 리스트를 사용해 글의 내용을 깔끔하게 정리할 수 있다.

## 순서 없는 리스트

`순서 없는 리스트(Unordered List)`는 다음과 같이 표현된다.  
- Hello.  
- Nice to meet you.  
* I'm Sungmok Hong.  
* Thank you.  

순서 없는 리스트를 작성하는 방법은 다음과 같다.
```markdown
- Hello.
- Nice to meet you.
* I'm Sungmok Hong.
* Thank you.
```

## 순서 있는 리스트

`순서 있는 리스트(Ordered List)`는 다음과 같이 표현된다.
1. Hello.
2. Nice to meet you.
3. Thank you.

순서 있는 리스트를 작성하는 방법은 다음과 같다.
```markdown
1. Hello.
2. Nice to meet you.
3. Thank you.
```

# 코드

Markdown 문법은 코드 표현에 매우 특화되어있다.

## 한 줄 코드

`한 줄 코드(Inline Code)`는 다음과 같이 표현된다.  
`Hello.`  
한 줄 코드를 작성하는 방법은 다음과 같다.
```markdown
`Hello.`
```

## 코드 블럭

`코드 블럭(Code Block)`은 다음과 같이 표현된다.
```
Hello.
Nice to meet you.
```
코드 블럭을 작성하는 방법은 다음과 같다.
````markdown
```
Hello.
Nice to meet you.
```
````
코드 블럭은 또 다른 특이한 용법이 있는데, 여러가지 언어에 맞게 글자 색을 변환하는 기능이 있다.  
C 
```c
int main()
{
    printf("Hello.\nNice to meet you.\n");
}
```
C++
```cpp
int main()
{
    std::cout << "Hello.\nNice to meet you." << std::endl;
}
```
Java
```java
public static void main(String[] args)
{
    System.out.println("Hello.\nNice to meet you.");
}
```
Python
```python
if __name__ == "__main__":
    print("Hello.\nNice to meet you.")
```

이를 사용하는 방법은 다음과 같다.
````markdown
```c
int main()
{
    printf("Hello.\nNice to meet you.\n");
}
```

```java
public static void main(String[] args)
{
    System.out.println("Hello.\nNice to meet you.");
}
```
````
이처럼 코드 블럭을 시작하는 ` ``` ` 뒤에 본인이 원하는 언어의 이름을 입력하면 된다.

# 마무리

Markdown에는 이 외에도 매우 다양한 용법이 존재한다.  
더 많은 문법을 확인하고 싶다면 [Markdown Guide](https://www.markdownguide.org/basic-syntax)를 확인하자.
