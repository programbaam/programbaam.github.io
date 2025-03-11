---
layout: single
title:  "블로그 01: GitHub Pages로 블로그 만들기"
categories: make-blog
tags: [blog, github-pages, git, github]
toc: true
toc_sticky: true
toc_label: "목차"
author_profile: false
sidebar:
    nav: "docs"
---



## 블로그 01 : GitHub Pages로 블로그 만들기



GitHub Pages는 GitHub를 통해 호스트되고 게시되는 퍼블릭 웹페이지

- 무료 호스팅 제공

GitHub Pages를 시작하는 가장 빠른 방법은 jekyll 테마 선택기 사용하여 미리 만들어진 테마를 로드하는 것.

jekyll은 Ruby 기반에 설치형 블로그 중 정적 사이트 생성기이다.

- 마크다운 사용하여 포스트 작성하면 HTML으로 변환하여 정적 사이트 만듬.

굳이 로컬에 Ruby와 jekyll을 설치하지 않아도 GitHub Pages는 가능하나 로컬에서 미리 보기 위하여  Ruby와 jekyll을 설치하겠다.



### Ruby WITH DEVKIT 설치

Ruby는 스크립트 언어의 일종으로 오픈 소스 프로그래밍 언어이다. 웹 개발에서 백엔드에 많이 쓰인다.

https://rubyinstaller.org/downloads/ 접속하여 자기 운영체제 맞는 걸 다운로드

![image-20250310181609479]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310181609479.png" | relative_url}})

![image-20250310181624584]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310181624584.png" | relative_url}})

![image-20250310181644959]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310181644959.png" | relative_url}})

MSYS2 체크하고 설치할 것

- 윈도우용 소프트웨어 빌드 플랫폼으로 유닉스와 유사한 환경, 명령줄 인터페이스 등을 제공한다.
- Ruby를 사용하기 쉽게 도와주는 툴킷이다.



![image-20250310181930243]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310181930243.png" | relative_url}})



![image-20250310181942095]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310181942095.png" | relative_url}})

1 입력 - MSYS2 base 설치

![image-20250310182059897]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310182059897.png" | relative_url}})



Start Command Prompt with Ruby 실행

![image-20250310182208649]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310182208649.png" | relative_url}})

```cmd
gem install bundler jekyll
```

gem이란 루비의 라이브러리, 루비에서 지원하는 패키지 시스템이다.

- gem을 이용해서 간단하게 원하는 프로그램 설치 가능
- jekyll과 bundler 젬을 설치한다.
- https://jekyllrb-ko.github.io/
- https://jekyllrb-ko.github.io/docs/

![image-20250310182410808]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310182410808.png" | relative_url}})

![image-20250310182446533]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310182446533.png" | relative_url}})

```cmd
jekyll -v
```

jekyll 버전 확인

![image-20250310182525555]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310182525555.png" | relative_url}})



### Jekyll 테마 선택

내가 사용할 테마는 minimal-mistakes를 선택하였다.

https://mmistakes.github.io/minimal-mistakes/ - 테마 모습

https://github.com/mmistakes/minimal-mistakes - 테마 다운받는 곳

![image-20250310185808376]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310185808376.png" | relative_url}})

우선 Download ZIP으로 로컬에 다운 받은 후

압축을 푼 후 폴더 명을 blog으로 변경 후 난 C 드라이브에 두었다.



```cmd
cd 블로그위치
```

![image-20250310183649451]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310183649451.png" | relative_url}})

블로그 디렉터리로 이동 후





```cmd
jekyll new
```

![image-20250310184624536]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310184624536.png" | relative_url}})



블로그 디렉터리에 jekyll 사이트를 생성한다.

```cmd
bundle exec jekyll serve
```

사이트를 빌드하고 로컬 서버에 적용

![image-20250310184659152]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310184659152.png" | relative_url}})

![image-20250310184735821]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310184735821.png" | relative_url}})

브라우저를 통해 http://localhost:4000이나 http://127.0.0.1:4000로 접속 가능하다.

![image-20250310184816186]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310184816186.png" | relative_url}})

![image-20250310184831034]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310184831034.png" | relative_url}})



접속을 끝내고 싶다면

![image-20250310210253212]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310210253212.png" | relative_url}})

`Ctrl+c`를 누른 후 y를 2번 쳐서 서버를 종료시킨다.

![image-20250310184901817]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310184901817.png" | relative_url}})

![image-20250310184912740]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310184912740.png" | relative_url}})

![image-20250310184937386]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310184937386.png" | relative_url}})



사이트를 빌드를 하면 2개의 폴더가 생긴 걸 볼 수 있다.

![image-20250310190345363]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310190345363.png" | relative_url}})



### GitHub Pages 만들기

GitHub Pages 만드는 법은 https://docs.github.com/ko/pages/quickstart - 참고



#### 원격저장소 생성

![image-20250310180436557]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310180436557.png" | relative_url}})

New 버튼을 누른 후

![image-20250310180757525]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310180757525.png" | relative_url}})



깃허브에서 신규 리포지토리를 만든 후 리포지토리 이름을 깃허브사용자이름.github.io로 만들면 된다.



### Git 설치

https://git-scm.com/downloads/win - windows 기준

![image-20250310181448891]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310181448891.png" | relative_url}})

![image-20250310181407315]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310181407315.png" | relative_url}})

운영체제에 맞는 Git 설치



## GitHub 연동

설치 후 Git bash를 열어



git에 사용자 등록

```bash
git config --global user.name 유저이름
git config --global user.email 유저이메일
```



![image-20250310192328969]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310192328969.png" | relative_url}})

![image-20250310192503697]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310192503697.png" | relative_url}})



```bash
git config -l
```

git log를 통해 사용자 등록 확인 가능

![image-20250310192725068]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310192725068.png" | relative_url}})



블로그 디렉터리로 이동 후

```bash
git init
```

![image-20250310201823777]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310201823777.png" | relative_url}})



기존 블로그 폴더에서 docs와 test는 파일을 삭제해도 상관없다. minimal-mistakes의 테마 블로그의 예시 들이다. 다른 곳에 옮겨놓고 참고해서 봐도 상관없다.

![image-20250310201941635]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310201941635.png" | relative_url}})

```bash
git add .
```

.은 모든 파일을 뜻한다.

모든 파일을 추가한다는 것이다.

![image-20250310202137120]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310202137120.png" | relative_url}})

```bash
git commit -m 'initial commit'
```

추가한 파일들에 대한 메시지를 입력한다. 

![image-20250310202258606]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310202258606.png" | relative_url}})

```bash
git remote add origin https://github.com/유저이름/유저이름.github.io.git
```

![image-20250310202502887]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310202502887.png" | relative_url}})

원격 저장소를 연결한다.



```bash
git push -u origin master
```

![image-20250310202607047]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310202607047.png" | relative_url}})

`-u` 옵션은 로컬 저장소 origin 브랜치를 원격 저장소 master 브랜치에 연결하기 위한 것으로 한 번만 사용하면 된다.



```bash
git log
```

![image-20250310203112008]({{"/images/2025-03-10-make-blog-01-make-blog/image-20250310203112008.png" | relative_url}})

git log를 통해 기록 확인 가능



다음부터 변경된 내용 있을 시 새로운 커밋을 아래 명령어로 업로드 가능하다.

```bash
git add .

git commit -m '커밋메시지'

git push
```


