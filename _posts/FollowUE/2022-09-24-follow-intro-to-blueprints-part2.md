---
layout: single
title:  "언리얼 따라하기 : Intro to Blueprints 03"
categories: followUE
tags: [followUE, UE, follow, intro-to-blueprints]
toc: true
toc_sticky: true
toc_label: "목차"
author_profile: false
sidebar:
    nav: "docs"
---



## Toggling a Light with the Level BP

레벨 블루프린트로 점등/소등 기능 만들기

<https://www.youtube.com/watch?v=gHdwOiR0D0A&list=PLjP7GdaJBM7GIJSjelGybVbm-S1VErg5y&index=3>



{% include video id="gHdwOiR0D0A" provider="youtube" %}



플레이어가 방에 들어가면 불이 들어오고

방에 나가면 불이 꺼는 것을 만들어보겠다.



방에 들어갔다는 행동의 기준 정확하게 정의해야함.

'볼륨'으로 정의 가능



볼륨은 3차원 공간을 말함



언리얼 엔진의 볼륨은 뭔가가 진입, 나가는 판정 가능 레이어 존재

