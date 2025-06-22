---
layout: single # 레이아웃 양식
title:  "Day 01 문자열 출력하기" # 제목
categories: programmers # _pages 폴더 안에 파일.md의 taxonomy 이름
tags: [PS, IO] # 태그
toc: true # 목차 뜨게 하기
toc_sticky: true # 목차 따라 다니게 하기
toc_label: "목차" # 목차 이름
author_profile: false # 저자 프로필 안뜨게 하기
sidebar:
    nav: "docs" # _data 폴더 안에 navigation.yml의 links 이름
---

## 문자열 출력하기

[https://school.programmers.co.kr/learn/courses/30/lessons/181952](https://school.programmers.co.kr/learn/courses/30/lessons/181952)

### 문자열 출력하기
#### Lv. 0
---

### 제한사항
---
- 1 ≤ `str`의 길이 ≤ 1,000,000
- - `str`에는 공백이 없으며, 첫째 줄에 한 줄로만 주어집니다.

#### 분류
---
- 입출력
#### 문제 설명
---
문자열 `str`이 주어질 때, `str`을 출력하는 코드를 작성해 보세요.

#### 입출력 예

입력 #1
---
```cmd
HelloWorld!
```
​

출력 #1
---
```cmd
HelloWorld!
```
​

#### 주어진 코드
---
solution.cpp
```c++
#include <iostream>
#include <string>

using namespace std;

int main(void) {
    string str;
    cin >> str;
    return 0;
}
```

#### 문제분석
---
출력 함수를 이용하여 문자열을 출력하라는 문제.
표준 출력 함수에 해당하는 cout을 이용하여 "Hello World!" 문자열 출력

#### 손 코딩
---
메인 함수
출력 함수("Hello World!")

#### 슈도코드
---
```pseudocode
main
	print "Hello World!";
```
​

#### 코드
---
```c++
#include <iostream>
#include <string>

using namespace std;

int main(void) {
    string str;
    cin >> str;
    return 0;
}
```

