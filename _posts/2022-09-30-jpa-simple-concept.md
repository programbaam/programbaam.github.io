---
layout: single
title:  "JPA 간단한 개념"
categories: spring-concept
tags: [spring, spring-concept, jpa]
toc: true
toc_sticky: true
toc_label: "목차"
author_profile: false
sidebar:
    nav: "docs"
---





JPA란?

출처:

<https://www.inflearn.com/course/%EC%8A%A4%ED%94%84%EB%A7%81%EB%B6%80%ED%8A%B8-%EA%B0%9C%EB%85%90%EC%A0%95%EB%A6%AC>



1. Java Persistence API 이다.

   - 영속성(Persistence)은 데이터를 생성한 프로그램의 실행이 종료되더라도 사라지지 않는 데이터의 특성
   - 램은 휘발성 데이터 저장. 컴퓨터 꺼지면 사라짐. 
     - 램에 있는 소중한 데이터는 하드디스크에 기록해야함. 하드디스크에 저장하면 영구적으로 저장됨
     - 영속성은 영구히 기록되도록 해주는 것
   - 자바에서는 데이터 저장을 파일시스템이 하드디스크에 하는 게 아님 하긴 하나 시스템이 dbms라 해서 하드디스크에 특정 영역을 잘라 관리를 함. 여기에 기록을 함
   - 자바에 있는 데이터를 영구히 기록할 수 있는 환경을 제공하는 API
   - API란?
     - Application Programming Interface
     - 프로그램(A) 만들기위한 과정(P)을 해주게 해는 인터페이스(I)
     - 프로그래밍을 하기 위해 제공해주는 인터페이스
       - 인터페이스도 약속을 의미
         - 상하관계가 존재하는 약속
       - 프로토콜은 권리가 동등하게 한 약속, 절차
   - 자바 프로그래밍을 할 때 데이터를 저장하기 위해 필요한 인터페이스가 JPA이다.

   출처:<https://youtu.be/ajZIPOv31yE>

2. ORM 기술

   - Object Relational Mapping
     - 오브젝트를 데이터베이스에 연결하는 방법론 같은 거
       - 자바와 데이터베이스가 가진 데이터 다름 클래스를 통해서 데이터베이스에 있는 타입으로 모델링 해야함.
     - 자바가 데이터베이스에 커넥션을 요청함
       - 데이터베이스가 세션을 오픈함. 
       - 자바가 연결하고 쿼리를 전송
       - 데이터베이스는 데이터를 돌려 줌
       - 자바는 데이터를 자바가 이해하게 변경해야함.
       - 단순한 반복적인 일 반복 
     - 이런 일을 JPA가 줄여줌. 함수 하나로 제공
       - 반복적인 일을 줄여줌
       - 단순하게 처리하게 도와줌

   출처: <https://youtu.be/4CRpndN3tP0>

3. 영속성 컨텍스트를 가지고 있다.

   - 자바에서는 데이터베이스에 영구적으로 저장 DB(ex) MySQL)
   - 컨텍스트는 대상의 모든 정보를 가지고 있는 것
   - 자바는 영속성 컨텍스트를 통해서 데이터베이스를 다룸 

4. DB와 OOP의 불일치성을 해결하기 위한 방법론 제공 (DB는 객체 저장 불가능)

   - ORM을 하면 자바가 주도권을 쥐는 모델을 만들 수 있음
   - JPA가 자동으로 매핑해줌. 자바는 객체 저장이 가능함.
   
   출처:<https://youtu.be/tXyDmqoMmKE>
   
5. OOP의 관점에서 모델링을 할 수 있게 해줌(상속, 콤포지션, 연관관계)

6. 방언 처리가 용이하며 Migration 하기 좋음. 유지보수에도 좋음.

   - 스프링->JPA->DB
     - JPA는 수많은 DB dialect를 지원 (오라클, MSSQL, MySQL)
     - 추상화 객체를 이용해서 가능. 데이터 베이스 방언처리 용이

7.  JPA는 쉽지만 어렵다.

출처: <https://youtu.be/vRoZAMX95Mc>

<https://getinthere.tistory.com/10?category=813090>