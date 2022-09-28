---
layout: single
title:  "안드로이드 간단한 프로젝트 만들기"
categories: android-concept
tags: [android, android-concept]
toc: true
toc_sticky: true
toc_label: "목차"
author_profile: false
sidebar:
    nav: "docs"
---



안드로이드 공부

출처:

<https://www.inflearn.com/course/%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-%EC%95%B1%EA%B0%9C%EB%B0%9C-%EA%B8%B0%EC%88%A0%EB%85%B8%ED%8A%B8/dashboard>

쉽게 따라할 수 있는 안드로이드 앱 개발-기술노트with알렉



## 앱 개발 처음하시는 분 간단한 앱 만들기

네이티브 앱

- 안드로이드

웹앱

- 인터넷 되야 함



<https://youtu.be/8tw2-K5Qz0s>



AMD CPU라 가상머신이 실행이 안된다면



Windows 기능 켜기/끄기 체크

- Hyper-V 체크
  - Hyper-V 관리 도구, Hyper-V 플랫 폼 체크

- Windows 하이퍼바이저 플랫폼 체크
- 가상 머신 플랫폼 체크

후 재부팅

<https://ourcodeworld.com/articles/read/1557/how-to-solve-android-emulator-hypervisor-error-driver-for-amd-processors-installation-failed>



만약 체크가 안된다면



AMD CPU에서 Hyper-v 안될 시

재부팅을 하고 부팅시 Delete 누르면 BIOS창이 뜨고 거기서 SVM Mode를 찾아 활성화 해준다.(가상머신 사용 유무)

설정 저장하고 재부팅

그 다음 다시 윈도우즈 기능 켜기/끄기 이동해서 체크 후 재부팅

<https://www.youtube.com/watch?v=H5vYI9reing>



## 누구나 5분이면 따라 하는 앱 만들기

### 프로젝트 생성

처음부터 File->New->New Project

Empty Activity 선택->언어는 자바



- 뷰를 하나 만들어서 헬로우 띄울 예정

### 클래스 생성

패키지 com.example.myapplication 에 클래스 하나 생성

SampleView로 SuperClass를 android.view.View 설정

조사한 바로는 이전 버젼으로 돌아갈 수 없다하니

SampleView 클래스를 만든 후

```java
package com.example.myapplication;

import android.view.View;

public class SampleView extends View {
}
```



만들면 에러가 뜸 생성자가 없다고

느낌 표 누르고 Create constructor matching super 클릭

첫번째 View(context:Context) 클릭

```java
package com.example.myapplication;
import android.content.Context;
import android.view.View;

public class SampleView extends View {
    public SampleView(Context context) {
        super(context);
    }
}
```



- 뷰를 하나 선언한 것

- 액티비티가 화면을 하나 지정한 것이고

- 그 안에 뷰를 통해서 글씨를 출력하려는 상황

### 페인트 지정

클래스 안에

public SampleView(Context context) { 위에

 Paint 생성자 추가

```java
private Paint paint = new Paint();
```

빨간색 줄의 Alt+Enter 치면 import class 골라 바로 import 가능

```java
import android.graphics.Paint;
```

글씨를 출력하려면 필요함

### 배경색 지정

super(context); 아랫 줄에

```java
setBackgroundColor(Color.WHITE);
```

선언. 흰색으로 백그라운드를 지정

### onDraw

SampleView 생성자 아래에

onDraw 친 후

protected void onDraw(Canvas canvas) 선택

```java
    @Override
    protected void onDraw(Canvas canvas) {
        super.onDraw(canvas);
    }
```

추가됨

#### canvas.drawText

super.onDraw(canvas);

아랫 줄에  

```java
canvas.drawText("Hello world!", 10, 100, paint);
```

캔버스라는 객체에서 drawText를 이용해서 문자열을 그릴거임

쓸문자열, 그릴 x, y좌표, 속성 선택

### 액티비티 뷰 변경

이제 이것을 실제적으로 액티비티에 뿌려줘야 함

MainActivity 로 가서

```java
setContentView(R.layout.activity_main);
```

를

```java
setContentView(new SampleView(this));
```

수정

방금 생성했던 뷰인 샘플 뷰로 여기서 보는 뷰로 세팅 됨.

### 글자 변경

하지만 글자가 너무 작음

SampleView로 돌아가

super.onDraw(canvas); 아래줄에

```java
paint.setTextSize(50);
```

추가

조금 더 커진 것을 확인 가능

### APK 생성

Build->Build Bundle(s)/APK(s)->Build APK(s)를 누르면

우측에 뜬 알림에 locate를 누르면

알림 다시볼라면 이벤트 로그에서 확인

파일 탐색기가 뜨면서 혹은 프로젝트명->app->build->outputs->apk->debug

 app-debug.apk를 핸드폰에 넣고 설치하면

우리가 프로젝트로 만든 앱이 핸드폰에서도 실행이 된다.



## 디지털 액자 완성 앱 만들기

### 기존 프로젝트 Hello world

기존 샘플 뷰를 추가 수정

기존 setContentView(R.layout.activity_main); 를 분석하면

res->layout->activity_main.xml를 가르킴

Code 탭으로 보면

```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

TextView로 보겠다는 내용

기존 MainActivity에서

```java
setContentView(R.layout.activity_main);
```

변경 후 출력

Hello world가 가운데에서 출력되는 걸 확인 가능

### 비트맵 그리기

비트맵 선언

```java
private Bitmap bmp;
```

SampleView 생성자 안에

```java
Resources res=context.getResources();
bmp= BitmapFactory.decodeResource(res, R.drawable.추가한 사진 이름);
```

추가

- 빨간 줄이 뜨면 Alt+Enter를 쳐 import 클래스 해주자

- 비트맵은 이미지를 불러올 수 있는 객체

- 이미지 하나 준비할 것

- res->drawable 폴더로 드래그 앤 드롭 할 것



onDraw 안에 추가

```java
canvas.drawBitmap(bmp, 0, 0, null);
```

그리고 

MainActivity에서

```java
setContentView(new SampleView(this));
```

다시 수정

### xml에 정의해서 이미지 불러오기

MainActivity에서

```java
setContentView(R.layout.activity_main);
```

수정

match_parent 전체화면 꽉채우는 것

```xml
    <ImageView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:src="@drawable/beomhoavatar"/>
```

텍스트 뷰 아래 추가

사진의 차이를 느낄 수 있음

자동으로 크기가 늘어나고 줄어들어서 출력됨

위치도 따로 지정 안함

이런 것들이 많이 모여 복잡해 지는 것임.



## 초보자도 10분이면 Mp3 플레이어 만들기





## 음성인식 노트앱 만들기





## 위치 기반 어플만들기



