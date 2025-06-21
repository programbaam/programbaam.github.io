---
layout: single
title:  "스프링 간단한 개념"
categories: spring-concept
tags: [spring, spring-concept]
toc: true
toc_sticky: true
toc_label: "목차"
author_profile: false
sidebar:
    nav: "docs"
---



스프링부트 개념 정리 1~3강

출처: <https://www.inflearn.com/course/%EC%8A%A4%ED%94%84%EB%A7%81%EB%B6%80%ED%8A%B8-%EA%B0%9C%EB%85%90%EC%A0%95%EB%A6%AC>



1. 프레임워크
   
   - 틀안에서 동작
2. 오픈 소스
   
   - 내부를 뜯어 고치는 게 가능
3. IoC 컨테이너 가진다. (Inversion of Controll) 제어의 역전
   - 스프링의 핵심
   - 주도권을 스프링에게 빼앗겼다.
     - 클래스-> 설계도
     - 오브젝트->실체화가 가능한 것
     - 인스턴스->실체화가 된 것
   - 스프링이 수많은 오브젝트들을 스캔을 해서 자기가 이 객체들을 띄움 heap 메모리에 올려줌. IoC 
4. DI Depndency Injection 의존성 주입
   - 이제는 스프링이 스캔해서 메모리 띄워서 내가 객체를 관리 안함.
   - 내가 원하는 모든 곳에서 가져와서 사용가능

   출처:<https://youtu.be/XBG6CUtVCIg>
   
5. 엄청나게 많을 필터 가짐
   - 스프링 자체 필터 사용
   - 톰캣 필터 web.xml->스프링 컨테이너 필터 인터셉터(AOP)
6. 엄청나게 많은 어노테이션 가짐
   - 컴파일 체킹
     - 어노테이션 (주석)은 컴파일러가 체킹할 수 있게 힌트를 주는 주석
       - 컴파일러가 무시하지 않음
     - @override 컴파일 할 때 
       - 확인해야 겠네 판단

   출처:<https://youtu.be/mAFLNA9MYg8>

   - 스프링에서는 어노테이션을 통해 객체 생성
     - @Component
       - 클래스 메모리에 로딩
       - 스프링이 스캔 읽어서 힙 메모리에 올림
     - @Autowired
       - 로딩된 객체 해당 변수에 집어 넣어
       - 읽은 객체를 선언하고 위에 어노테이션을 넣으면
         - 분석(리플렉션) 메서드, 필드, 어노테이션 체킹함
         - 있다면 무엇인가를 해라 설정가능
         - 떠있지 않다면 그냥 Null 들어가고
         - 같은 타입의 데이터 있으면 메모리에 있는 데이터 넣음
           - DI임 의존성 주입 
     - 어노테이션 (주석 힌트), 리플렉션(분석하는 기법->런타임시 분석)
7. MessageConverter를 가지고 기본값은 현재 Json이다.
   - 중간언어 : Json
   - 자바 오브젝트를 JSON을 변경해주는 MessageConverter : Jackson 라이브러리
8. 버퍼드리더, 버퍼드라이터 쉽게 사용
   - 8비트->1바이트 일반적인 프로그래밍 통신의 최소 단위
     - 논리적으로 부르는 말
     - 1 바이트 = 하나의 문자
     - 유니코드 UTF-8 3바이트 통신
   - 바이트 스트림 : 1바이트 8비트 
     - InputStream 스트림 
       - 바이트를 읽음
       - 받은 데이터를 char로 받아야함
       - 복잡하니 InputStreamReader 문자하나
         - 배열로 여러개의 문자 받을 수 있긴 하나 배열은 크기가 정해져 있음
         - 배열이 작으면 나머지 문자가 버려짐
         - 보내진 데이터 적으면 낭비됨
       - 버퍼드 리더로 감싸야함
         - 가변 길이의 문자를 받을 수 있다.
   - request.getReader()
   - 버퍼드라이터, PrintWriter rint(), println()
     - 전송단위가 가변길이의 데이터를 쓰게 해줌
   - @ResponseBody->버퍼드 라이터 존재
   - @RequestBody->버퍼드 리더 존재
9. 스프링은 계속 발전 중

출처: <https://youtu.be/-5r52dt2HcU>

<https://getinthere.tistory.com/9?category=813090>