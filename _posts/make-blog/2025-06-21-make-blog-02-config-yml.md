---
layout: single
title:  "블로그 02: _config.yml 세팅"
categories: make-blog
tags: [blog, github-pages, git, github]
toc: true
toc_sticky: true
toc_label: "목차"
author_profile: false
sidebar:
    nav: "docs"
---



## 블로그 02 : _config.yml 세팅

https://mmistakes.github.io/minimal-mistakes/docs/configuration/

참조



### Theme Settings

```yml
# Theme Settings
```



#### 스킨 skin

폴더에 _config.yml 파일을 연다.

```yml
minimal_mistakes_skin    : "default" # "air", "aqua", "contrast", "dark", "dirt", "neon", "mint", "plum", "sunrise"
```

블로그의 전체 색을 수정



필자는

```yml
minimal_mistakes_skin    : "aqua" 
```

아쿠아로 수정

![image-20250621191355526]({{"/images/2025-06-21-make-blog-02-config-yml/image-20250621191355526.png" | relative_url}})

색은 여기서 확인 가능

https://mmistakes.github.io/minimal-mistakes/docs/configuration/#skin



### Site Settings

```yml
# Site Settings
```



#### 사이트 기본 언어 locale

```yml
locale                   : "en-US"
```

를

```yml
locale                   : "ko-KR"
```

로 수정



#### 블로그 제목 title

```yml
title                    : "Site Title"
```

를

```yml
title                    : "baam의 블로그"
```

로 수정

![image-20250621191326316]({{"/images/2025-06-21-make-blog-02-config-yml/image-20250621191326316.png" | relative_url}})

![image-20250621191336279]({{"/images/2025-06-21-make-blog-02-config-yml/image-20250621191336279.png" | relative_url}})



#### 사이트에 대한 짧은 태그라인 subtitle

```yml
subtitle                 : # site tagline that appears below site title in masthead
```

를

```yml
subtitle                 : "프로그래밍 블로그" # site tagline that appears below site title in masthead
```

수정

![image-20250621192714493]({{"/images/2025-06-21-make-blog-02-config-yml/image-20250621192714493.png" | relative_url}})

#### 이름 name

```yml
name                     : "Your Name"
```

를

```yml
name                     : "Beomho Lee"
```

수정

#### 사이트 설명 description

```yml
description              : "An amazing website."
```

를

```yml
description              : "이범호의 프로그래밍 공부 기록"
```

수정

#### url

```yml
url                      : "https://programbaam.github.io"
```

수정

#### 원격 저장소 repository

```yml
repository               : # GitHub username/repo-name e.g. "mmistakes/minimal-mistakes"
```

를

```yml
repository               : "programbaam/programbaam.github.io" # GitHub username/repo-name e.g. "mmistakes/minimal-mistakes"
```

수정

### Site Author

```yml
# Site Author
```

#### 사이트 저자 author

```yml
# Site AuthorMore actions
author:
  name             : "Your Name"
  avatar           : # path of avatar image, e.g. "/assets/images/bio-photo.jpg"
  bio              : "I am an **amazing** person."
  location         : "Somewhere"
  email            :
```

를

```yml
name             : "Beomho Lee"More actions
  avatar           : "./images/beomho-avatar.png" # path of avatar image, e.g. 
  bio              : "프로그래밍을 열심히 **공부** 중"
  location         : "대한민국"
  email            :  "programbaam@naver.com"
```

수정

![image-20250621193538071]({{"/images/2025-06-21-make-blog-02-config-yml/image-20250621193538071.png" | relative_url}})

#### 링크 links

본인이 링크 하고 싶은 메신저를 추가

```yml
  links:
    - label: "Email"
      icon: "fas fa-fw fa-envelope-square"
      # url: "mailto:your.name@email.com"
    - label: "Website"
      icon: "fas fa-fw fa-link"
      # url: "https://your-website.com"
    - label: "Twitter"
      icon: "fab fa-fw fa-twitter-square"
      # url: "https://twitter.com/"
    - label: "Facebook"
      icon: "fab fa-fw fa-facebook-square"
      # url: "https://facebook.com/"
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      # url: "https://github.com/"
    - label: "Instagram"
      icon: "fab fa-fw fa-instagram"
      # url: "https://instagram.com/"
```

를

```yml
  links:
    - label: "Email"
      icon: "fas fa-fw fa-envelope-square"
      url: "mailto:programbaam@naver.com"
    - label: "Website"
      icon: "fas fa-fw fa-link"
      # url: "https://your-website.com"
    - label: "Twitter"
      icon: "fab fa-fw fa-twitter-square"
      # url: "https://twitter.com/"
    - label: "Facebook"
      icon: "fab fa-fw fa-facebook-square"
      # url: "https://facebook.com/"
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/programbaam"
    - label: "Instagram"
      icon: "fab fa-fw fa-instagram"
      # url: "https://instagram.com/"
```

수정

![image-20250621193548839]({{"/images/2025-06-21-make-blog-02-config-yml/image-20250621193548839.png" | relative_url}})

### Site Footer

```yml
# Site Footer
```

#### 사이트 하단 footer

```yml
# Site Footer
footer:
  links:
    - label: "Twitter"
      icon: "fab fa-fw fa-twitter-square"
      # url:
    - label: "Facebook"
      icon: "fab fa-fw fa-facebook-square"
      # url:
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      # url:
    - label: "GitLab"
      icon: "fab fa-fw fa-gitlab"
      # url:
    - label: "Bitbucket"
      icon: "fab fa-fw fa-bitbucket"
      # url:
    - label: "Instagram"
      icon: "fab fa-fw fa-instagram"
      # url:
```

를

```yml
# Site Footer
footer:
  links:
    - label: "Twitter"
      icon: "fab fa-fw fa-twitter-square"
      # url:
    - label: "Facebook"
      icon: "fab fa-fw fa-facebook-square"
      # url:
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/programbaam"
    - label: "GitLab"
      icon: "fab fa-fw fa-gitlab"
      # url:
    - label: "Bitbucket"
      icon: "fab fa-fw fa-bitbucket"
      # url:
    - label: "Instagram"
      icon: "fab fa-fw fa-instagram"
      # url:
```

수정

![image-20250621193559915]({{"/images/2025-06-21-make-blog-02-config-yml/image-20250621193559915.png" | relative_url}})




