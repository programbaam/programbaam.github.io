---
layout: single
title: "블로그 03: 라이선스"
categories: github-pages
tags:
  - blog
  - github-pages
  - git
  - github
toc: true
toc_sticky: true
toc_label: 목차
author_profile: false
sidebar:
  nav: docs
---



## 블로그 03 : 라이선스



### mmistakes 테마 MIT 라이선스

mmistakes theme은 MIT 라이선스로 저작권은 Michael Rose 및 기여자들에게 있다. 

MIT 라이선스이기 때문에 제한 없이 사용이 가능하고 상업적 이용이 가능하다.

단, MIT 라이선스와 저작권자들에게 저작권이 있다고 고지 및 본 허가 고지를  소프트웨어 사본이나 실질적인 일부에 모든 문서에 포함되어야 한다.



그렇기에 가장 최상위 폴더에 LICENSE 파일에

```LICENSE
## MIT License

The MIT License (MIT)

Copyright (c) 2013-2020 Michael Rose and contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```



README.md 파일 최상단에는 배지와 함께 라이선스 페이지를 링크, 최하단에 별도에 라이선스 고지를 해주는 게 좋다.

![image-20250621201846615](../images/2025-06-21-make-blog-03-license/image-20250621201846615.png)

```markdown
최상단
[![LICENSE](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/mmistakes/minimal-mistakes/master/LICENSE)

최하단
### License
This project is licensed under the MIT License

#### MIT License
The MIT License (MIT)

Copyright (c) 2013-2020 Michael Rose and contributors

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Minimal Mistakes incorporates icons from The Noun Project creators Garrett Knoll, Arthur Shlain, and tracy tam. Icons are distributed under Creative Commons Attribution 3.0 United States (CC BY 3.0 US).

Minimal Mistakes incorporates Font Awesome, Copyright (c) 2017 Dave Gandy. Font Awesome is distributed under the terms of the SIL OFL 1.1 and MIT License.

Minimal Mistakes incorporates photographs from Unsplash.

Minimal Mistakes incorporates Susy, Copyright (c) 2017, Miriam Eric Suzanne. Susy is distributed under the terms of the BSD 3-clause "New" or "Revised" License.

Minimal Mistakes incorporates Breakpoint. Breakpoint is distributed under the terms of the MIT/GPL Licenses.

Minimal Mistakes incorporates FitVids.js, Copyright (c) 2013 Dave Rubert and Chris Coyier. FitVids is distributed under the terms of the WTFPL License.

Minimal Mistakes incorporates Magnific Popup, Copyright (c) 2014-2016 Dmitry Semenov, http://dimsemenov.com. Magnific Popup is distributed under the terms of the MIT License.

Minimal Mistakes incorporates Smooth Scroll, Copyright (c) 2019 Chris Ferdinandi. Smooth Scroll is distributed under the terms of the MIT License.

Minimal Mistakes incorporates Gumshoejs, Copyright (c) 2019 Chris Ferdinandi. Gumshoejs is distributed under the terms of the MIT License.

Minimal Mistakes incorporates jQuery throttle / debounce, Copyright (c) 2010 "Cowboy" Ben Alman. jQuery throttle / debounce is distributed under the terms of the MIT License.

Minimal Mistakes incorporates GreedyNav.js, Copyright (c) 2015 Luke Jackson. GreedyNav.js is distributed under the terms of the MIT License.

Minimal Mistakes incorporates Jekyll Group-By-Array, Copyright (c) 2015 Max White mushishi78@gmail.com. Jekyll Group-By-Array is distributed under the terms of the MIT License.

Minimal Mistakes incorporates @allejo's Pure Liquid Jekyll Table of Contents, Copyright (c) 2017 Vladimir Jimenez. Pure Liquid Jekyll Table of Contents is distributed under the terms of the MIT License.

Minimal Mistakes incorporates Lunr, Copyright (c) 2018 Oliver Nightingale. Lunr is distributed under the terms of the MIT License.
```



별도의 추가적인 저작권 물을 추가할 시 그 저작권자의 허락한 범위에 맞게 고지 사항을 지키며 라이선스 파일, README 파일, 별도의 사용하는 곳과 폴더에 문서 파일에 라이선스들을 고지하면 된다.

추가로 이 프로젝트에서 어떤 곳에 이 저작권자의 저작물을 사용했는 지도 라이선스와 같이 자세하게 적어주면 좋다.
