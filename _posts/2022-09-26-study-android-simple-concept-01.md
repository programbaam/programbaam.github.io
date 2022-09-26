---
layout: single
title:  "안드로이드 필요한 간단한 개념"
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



## 안드로이드 앱 간단하게 3가지

Layout-> 안드로이드는 xml으로 표현

- 구성요소 버튼, 박스, 지도 등
- xml로 레이아웃을 결정, 설계도, 배치도 같은 것
- 배치도 같은거 화면을 정의
- 안드로이드 스튜디오에서 미리보기로 그려준다.
- 크기, 위치 정의

Activity-> 화면 자체를 말함. 액티비티가 레이아웃을 품고 있다,

- 레이아웃은 배치만 하고 거기 안에 기능은 액티비티가 담당
- 레이아웃 하나씩 매핑됨. 대부분의 액티비티는 모양을 가지고 있다.
- 배치는 레이아웃에 의해 결정
- 안드로이드 앱은 액티비티들의 모임, 합집합

이벤트->버튼을 누르면 동작하는 것을 나타냄

- 어떤 행동을 하면 함수를 실행하라.



<https://youtu.be/LkBMmOdjm3E>



## 화면개발

- 어떤 식으로 배치
  - 리니어 레이아웃
    - 순차적으로 배치, 밑으로 쭉, 방향을 정해 줘야 함
    - 개념을 정확하게 알 것
  - relative 레이아웃
    - 상대적 배치, 상대적 기준 명시
    - 상대적인 좌표의 의해서 배치



<https://youtu.be/fOFBza-KuYk>



## 앱 개발을 위한 자바

최소한의 Java 중요한 개념, 언어

 자바

- 객체 지향
  - c++, 자바는 객체가 중심
  - c 언어 변수가 함수를 포함안함
  - 객체는 변수도 있지만 행위도 담고 있음
- 클래스, 메소드
  - 메소드 클래스 안의 함수
    - 받는 값 인자, 인수
    - 생성자
      - 오버로드
        - 동일한 이름 메소드를 선언하고 매개변수 타입, 수나 반환 타입이 다름 
        - 직관성이 더 생김
      - 오버라이드
        - 상속받은 부모가 가지고 있던 함수를 재정의



<https://www.youtube.com/watch?v=-ItD1gOdPag>



## 앱 개발자에게 필요한 네트워크 지식

TCP/IP 쉽게, 더 쉽게 책 추천

클라 브라우저 요청->서버 web서버 응답

프로토콜 약속

- HTTP
  - 하이퍼텍스트 (html)
  - GET / / 서버에 요구 

- 이메일
  - SMTP, pop3

- FTP->파일

AJAS

- 동기
-  비동기

쿠키

- 클라이언트에 저장됨. 로컬에 저장됨. 변수 저장

세션

- 서버에 저장되있는 데 DB랑 다름. 웹서버나 was서버 수준에 저장
- 접속한 클라이언트를 위해 만들어진 변수
- 비슷한 예 로그인 유지
- 보안 상으로 쿠키에 저장하지 않으려 함

VOIP->voice over IP

- 음성을 데이터 화->IP->데이터->음성
- 인터넷 망만 되면 전화 가능
- IP 네트워크, 서버 인프라, 연결 서버

- UDP 개념
  - TCP 정확한 메시지 전달
  - UDP는 손실에 대해서 허용
    - 압축 
      - 무손실은 손실되면 풀리지 않음. 알집
      - 손실 약간 깨져도 됨. 영상, 소리 파일
        - 클라이언트 단위에서 보정 기술이 있음

포트 port

- IP가 한국이라면 port는 인천, 부산 항구
- 포트에 해당하는 어플리케이션에서 받음

서버, 컴퓨터 포트->'netstat -n'

- 도메인->DNS서버->IP 
- 라우팅해서 감
- IPv6 많은 디바이스 소화하도록 확장됨

NAT(network address translation)

- 모든 서버가 퍼블릭 IP를 가지진 않음
- 이런 서버들은 private IP를 사용함(외부적으로 접근 못함)
  - 접속 방법 필요함. 이 IP로 다른 서버들과 소통 못함
  - NAT는 private IP를 퍼블릭 IP로 만들어줌

ipconfig

- 할당받은 IP 주소 확인

ping 주소IP

- 상대 컴퓨터에서 응답해줌
- 컴퓨터에서 막으면 못받음. 공격용으로 쓰는 경우 있어서

tracert url

- 해당 url을 가는 라우팅 정보를 줌
- 어디서 막혔는 지 파악에 좋음

nslookup 도메인

- 해당 도메인 ip 응답
- DNS 서버 조회
- ip를 통해 도메인을 알고 반대도 가능

이더넷

- 통신 규격 규약

허브

- 일종의 스위치

HTTPS

- 암호화 통신
- 암호화를 통해 전달

전자서명->데이터 원본

전자 인증->사용자 증명, 기관



<https://www.youtube.com/watch?v=65h9uxHKGPk>



## 앱 서버 연동을 위한 서버 클라우드 지식

클라우드 서비스, AWS, 서버

- 

아마존

- www.pyrasis.com
- 아마존 웹 서비스를 다루는 기술
