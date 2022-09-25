---
layout: single
title:  "언리얼 따라하기 : Beginner Tutorial - RTS Game 01"
categories: followUE
tags: [followUE, UE, follow, beginner-tutorial-rts-game]
toc: true
toc_sticky: true
toc_label: "목차"
author_profile: false
sidebar:
    nav: "docs"
---



<https://www.youtube.com/watch?v=CCO0-64cfe4>



{% include video id="CCO0-64cfe4" provider="youtube" %}



이 과정은 블루프린트만 사용한다.



## Create the project and import the assets

프로젝트 생성과 에셋 임포트



### 샘플 다운

에픽 런쳐->샘플->UE 레거시 샘플->전략 게임

->프로젝트 생성->원하는 폴더에 가장 최신 버젼으로 생성한다.

![전략 게임 샘플 다운]({{"/images/follow-unreal-rts-download-rts-game.png" | relative_url}})

여기서 우리는 에셋만 쓸 것이다.



파일 탐색기에서 전략게임->Content로 이동하여 안에 파일들을 전부 복사

![전략 게임 에셋 복사]({{"/images/follow-unreal-rts-game-assets-copy.png" | relative_url}})



### 프로젝트 생성

언리얼 엔진에서 게임->기본->블루프린트->시작용 콘텐츠 체크 해제하고->프로젝트 이름은 자기마음대로 하고 생성 영상에선는 MyFirstRTS로 만듬

![프로젝트 생성]({{"/images/follow-unreal-rts-game-create-project.png" | relatvie_url}})



### 에셋 임포트

좌측 하단에 콘텐츠 드로어를 열고->콘텐츠 폴더를 우클릭->탐색기에서 표시를 클릭

![탐색기에서 표시]({{ "/images/follow-unreal-rts-game-content-folder-show-explorer.png" | relative_url}})

 

폴더 탐색기로 들어가지면 거기에 새 폴더를 만든 후 StategyGameAssets이라고 이름을 바꾼 후 아까 복사한 파일들을 붙여 넣는다.

![파일 붙여넣기]({{"/images/follow-unreal-rts-game-create-folder-and-paste-files.png" | relative_url}})



그러고 언리얼 엔진 에디터로 돌아오면 임포트 할것인지 떠있다. 임포트 버튼을 누르고 또 임포트 옵션이 뜬다. 모두 예를 누르면 된다.

![임포트 동의]({{"/images/follow-unreal-rts-import-agree.png" | relative_url}})



## Quick scene with the landscape tool



### 새 레벨 생성

파일->새 레벨->빈 오픈 월드로 생성

콘텐츠 브라우저 다시 열어 콘텐츠 폴더 하위 폴더로->MyFirstRTS(프로젝트 이름과 동일) 폴더 만들고->그 안에 Maps 폴더 만들기

![레벨 폴더 생성]({{"/images/follow-unreal-rts-create-project-folder-and-level-folder.png" | relative_url}})



파일->현재 레벨 저장->경로는 아까 만든 Maps 폴더 안으로 하고

이름은 RockyLevel로 저장



### 환경 라이트 생성

창->환경 라이트 믹서를 클릭하여 창을 띄우고

![환경 라이트 믹서]({{"/images/follow-unreal-rts-show-environment-light-mixer.png" | relative_url}})

그 후 스카이 라이트 생성, 애트머스페릭 라이트 0 생성, 불륨메트릭 클라우드 생성, 하이투 포그 생성, 스카이 에트머스피어 생성 버튼을 클릭



SkyLight 클릭->디테일 탭에서 리얼타임 캡쳐 체크

![스카이라이트 리얼타임 캡쳐 체크]({{"/images/follow-unreal-rts-skylight-realtime-capture-check.png" | relative_url}})



DirectionalLight, ExponentialHeightFog, SkyAtmosphere, SkyLight, VolumetricCloud 선택해서 검색 옆에 폴더 추가 버튼을 눌러 Lighting 폴더를 만들어 넣어준다.

![라이트닝 폴더 생성]({{"/images/follow-unreal-rts-create-lighting-folder.png" | relative_url}})



겹치지 않도록 각각 올려준다. Lighting 폴더에서 하나씩 액터를 선택하여 조금 만 더 위로 하나씩 올리자. 나중에 편하게 뷰포트에서 직관적으로 확인하고 누르기 위해서다.

![빛 올리기]({{"/images/follow-unreal-rts-up-light.png" | relative_url}})



### 랜드스케이프 모드

저장 아이콘 옆에 있는 선택모드에서 랜드스케이프 모드로 이동

변경 단축키 `Shift+2`

![랜드 스케이프 모드]({{"/images/follow-unreal-rts-landscape-mode.png"|relative_url}})



영상에서는 63*63으로 함 새 랜드스케이프 생성

![랜드스케이프 생성]({{"/images/follow-unreal-rts-create-landscape.png"|relative_url}})



스컬프팅으로 랜드스케이프를 다지라고 한다. 가운데는 평평하고 주위에는 산이 둘러싼 형태로

스컬프팅으로 강도, 브러시 크기를 올려 전체적으로 다양한 형태를 만들고 스무드로 부드럽게 만들어주고 기타 등등 도구로 가운데는 평평한 분지 형태를 만들어 줌

![랜드스케이프 스컬프팅]({{"/images/follow-unreal-rts-sculpting-landscape.png"|relative_url}})



## Add the assets to the map

콘텐츠 드로어->필터->스태틱 메시

StrategyGameAssets 폴더를 선택하여 스태틱 메시를 보자 

![콘텐츠 드러오 필터 기능]({{"/images/unreal-content-drawer-filter.png"|relative_url}})



선택 모드로 변경(`Shift+1`)

패널 전부 접고 싶다면 단축키 `F10`



Sm_TD_Brewery_01, SM_TD_Gold_Pile,  RTS_Env_Rocks_01B 각각 배치

머티리얼이 깨져있다.

![머티리얼이 깨진 에셋]({{"/images/follow-unreal-rts-broken-material-assets.png"|relative_url}})







## Fix the materials

### 스태틱 메시 에디터에서 머티리얼 삽입

수정하고 싶으면 콘텐츠 브라우저에서 에셋을 더블 클릭하거나, 

우클릭 편집... 이나 상단 파일->에셋 열기로 가능

혹은 뷰포트에서 액터 선택 후 `Ctrl+e`

스태틱 메시 에디터를 열 수 있다.



먼저 Sm_TD_Brewery_01 수정하겠다.

머티리얼 슬롯에 M_TD_Brawery가 들어가야 한다. 콘텐츠 드로어로 스태틱 메시 필터링을 끄고 찾아라. Brawery 검색 (오타인지 머티리얼은 Brawery다)

![Brawery 머티리얼 찾기]({{"/images/follow-unreal-rts-find-brawery-material.png"|relative_url}})



머티리얼을 선택 후 아래 사진 처럼 화살표를 누르면 그 머티리얼을 사용한다.

![스태틱 메시 에디터에서 머티리얼 사용]({{"/images/unreal-static-mesh-editor-use-material.png"|relative_url}})



### 머티리얼 에디터에서 텍스쳐 삽입

하지만  M_TD_Brawery도 깨져있다. 이것도

콘텐츠 드로어에서 더블 클릭하거나, 우클릭 편집...  혹은 에셋 열기로 오픈 가능

머티리얼 에디터로 들어간다.

![텍스쳐 누락]({{"/images/follow-unreal-rts-empty-texture.png"|relative_url}})



콘텐츠 브라우저에서 brewery를 검색하여

Texture Sample 노드, Mask 노드의 디테일 탭 머티리얼 표현식 텍스쳐 베이스에 정해진 에셋을 집어 넣자.

상단 Texture Sample 노드에는 T_TD_Brewery_D를

Mask 노드에는 T_TD_Brewery_E2를

하단 Texture Sample 노드에는 T_TD_Brewery_N을 넣으면

![텍스쳐 적용]({{"/images/follow-unreal-rts-texture-apply.png"|relative_url}})

![머티리얼 적용]({{"/images/follow-unreal-rts-material-apply.png"|relative_url}})

툴바에 적용 버튼을 누르고  Sm_TD_Brewery_01 스태틱 메시 에디터에서

확인이 가능하고 확실하게 사용할거면 각각 머티리얼 에디터, 스태틱 메시 에디터에서 저장을 누르자

### 나머지 에셋

 RTS_Env_Rocks_01B은

머티리얼 M_RTS_Env_Rocks_01

상단 Texture Sample에 RTS_Env_Rocks_01_D

하단 Texture Sample에 RTS_Env_Rocks_01_N



SM_TD_Gold_Pile은

머티리얼 M_TD_Gold_Pile

상단 Texture Sample에 T_TD_Pile_D

중단 Texture Sample에 T_TD_Pile_N

하단 Texture Sample에 T_TD_Pile_E

각각 적용 후 저장

![머티리얼 텍스쳐 수정 고침]({{"/images/follow-unreal-rts-fix-material-and-apply.png"|relative_url}})



## Add a landscape material and paint the zones

### 폴더 컬러 설정

콘텐츠 드로어 다시 가서

이전에 만든 MyFirstRTS(프로젝트 명) 폴더를 오른쪽 클릭 후 컬러 설정으로

내가 원하는 색으로 표시 나중에 찾기 편하기 하기 위해서다

![폴더 컬러 설정]({{"/images/follow-unreal-rts-folder-color-setting.png"|relative_url}})



### 머티리얼 생성

폴더 안에 새로운 폴더 Environment 생성

안에 오른쪽 클릭->고급 에셋 생성->머티리얼->머티리얼 클릭해서 생성 

![머티리얼 생성]({{"/images/follow-unreal-rts-create-material.png"|relative_url}})



이름은 M_RockyLandscape 지음

더블 클릭으로 들어감

디테일 탭에서 fully rough 또는 완전 러프 검색해서 체크-체크하면 빛나지 않게 됨

![완전 러프 체크]({{"/images/follow-unreal-rts-fully-rough-material.png"|relative_url}})



#### LandscapeLayerBlend

그래프에서 오른쪽 클릭으로 LandscapeLayerBlend 클릭 추가(일부분만 검색해도 나옴)

![LandscapeLayerBlend]({{"/images/follow-unreal-rts-landscapelayerblend.png"|relative_url}})



M_RockyLandscape 베이스 컬러와 Layer Blend 우측 빈 원과 연결

Layer Blend 디테일 탭에서 Material Expression Landscape Layer Blend 열어 엘리먼트를 추가

![엘리먼트 추가]({{"/images/follow-unreal-rts-landscapelayerblend-add-element.png"|relative_url}})



레이어 아래 인덱스[0]를 열어 레이어 이름 Ground로 바꿔줌

레이어 옆 엘리먼트 옆 플러스 표시 눌러 엘리먼트 추가해

인덱스 [1]은 Rocks, 인덱스 [2]는 RockyGround로 명명

![3 엘리먼트 추가 후 이름 변경]({{"/images/follow-unreal-rts-landscapelayerblend-add-three-element.png"|relative_url}})



#### Constant3Vector

이제 색을 넣을 건데

`3+좌클릭` 아니면 오른쪽 클릭 Constant3Vector를 3개 추가

![Constant3Vector 추가]({{"/images/follow-unreal-rts-add-constant3vector.png"|relative_url}})



#### 색상 추출

그 노드를 더블클릭하면 색 지정 가능

머티리얼 에디터를 레벨 에디터 옆에 탭으로 붙여놧다면

색 선택 툴이 켜진 상태로 레벨에디터로 넘어갈 수 있다.

스포이드를 가지고

상단은 가장 배경이 되는 색

중단은 바위 같이 어두운 색

하단은 배경보다는 어두운 색으로 하자.

![색 지정]({{"/images/follow-unreal-rts-eyedropper-constant3vector.png"|relative_url}})



그리고 상단-Layer Ground, 중단-Layer Rocks, 하단-Layer RockyGround에 연결한다.

![M_RockyLandscape 레이어 블랜드]({{"/images/unreal-M_RockyLandscpae-Layer-Blend.png"|relative_url}})



### 머티리얼 적용

다시 레벨에디터로 돌아와 아웃라이너에서 랜드스케이프 머티리얼을 M_RockyLandscape로 설정한다.

![랜드스케이프 머티리얼 적용]({{"/images/follow-unreal-rts-apply-landscape-material.png"|relative_url}})



### 랜드스케이프 페인트

설정해도 변한 것은 없다.

랜드스케이프 모드로 바꾸고 페인트로 가서 타깃 레이어에 아래에 3개에 레이어를 볼 수 있다.

![랜드스케이프 페인트]({{"/images/follow-unreal-rts-apply-landscape-mode-paint.png"|relative_url}})



각 레이어들을 십자가 표시->웨이트 블렝딩된 레이어(노멀) 클릭 후->Environment 폴더에 저장하자

콘텐츠 드로어로 이동후 Environment 폴더 안에 RockyLevel 폴더를 생성하여 기존 파일 4개를 다 옮기고

RockyLevel 폴더 우클릭하여 폴더의 리디렉터 고치기를 클릭하자. 자동으로 해주지만 만일을 위해서

옮기고 자주 해주자.

![랜드스케이프 색칠]({{"/images/follow-unreal-rts-landscape-mode-paint.png"|relative_url}})



이제 원하는 레이어를 골라 마음대로 색칠하자

뷰포트 상단에 카메라를 클릭하면 카메라 속도 조절이 가능하다

## Import the needed assets frome Megascans

### 퀵 셀 콘텐츠 추가

콘텐츠 드로어->+추가->퀵 셀 콘텐츠 추가

![퀵셀 콘텐츠 추가]({{"/images/follow-unreal-rts-add-quixel-content.png"|relative_url}})



->Hartland Quay Shore 검색->들어가서 필터 설정 Surfaces->

마음에드는 에셋을 다운로드하고 Add 하자 3개 정도 추가

Megascans->Surfaces에서 확인 가능

![Hartland Quay Shore 추가]({{"/images/follow-unreal-rts-add-hartland-quay-shore-surface.png"|relative_url}})



### 머티리얼 텍스쳐 추가

M_RockyLandscape의 머티리얼 에디터로 들어간다 기존 Constant3Vector 3개의 색상을 뒤로 빼고

Layer Blend 연결을 다 끊는다. 단축키는 `Alt+좌클릭`

에디터 그래프 안에 각각에 D와 N을 끝나는 텍스쳐 드래그앤 드롭으로 추가

![텍스쳐들 드래그 앤 드롭]({{"/images/follow-unreal-rts-material-add-texture.png"|relative_url}})



D들은 각각 연결 그 다음 저장 후 레벨 확인 타일이 반복되서 붙여져 있음

툴바에서 라이브 업데이트에서 모든 노드 프리뷰 체크해서

텍스쳐 무슨일 일어나는 지 확인

![텍스쳐 타일 반복]({{"/images/follow-unreal-rts-material-add-texture-and-tiling.png"|relative_url}})



#### 텍스쳐 관련 노드 추가

그래프에 WorldPosition 노드 추가- 절대 월드 포지션이란 노드 생김

- 이 노드는 내부 단어 위치 정보를 얻을 수 있다고 한다.

- xyz 세가지 값까지는 필요없음. 

ComponentMask 노드 추가. 절대 월드 포지션 노드와 연결 후

ComponentMask 노드 디테일 탭에서 x와 y 값만 필요하니 R G만 체크

ComponentMask 노드 링크를 당겨 이걸 다시 Divide함

별도로 `1+좌클릭` Constant 노드 추가 값 512 입력하고 Divde의 B에 연결

![노드 추가 링크]({{"/images/follow-unreal-rts-material-add-node-and-link.png"|relative_url}})



Divide를 상단 Texture Sample의 UVs에 연결

저장하고 레벨을 확인한 후

![노드 추가 링크 텍스쳐 확인]({{"/images/follow-unreal-rts-material-add-node-and-link-texture.png"|relative_url}})



0이라 표시된 Constant 노드를 우클릭 파라미터로 변환 GroundTiling이라 지어줌

![파라미터 변환]({{"/images/follow-unreal-rts-material-change-parameter.png"|relative_url}})



절대월드 포지션, Mask, Divide, GroundTiling을 드래그하고 2번 복사

중단, 하단 Texture Sample의 UVs에 연결

GroundTiling을 RocksTiling, RockyGroundTiling으로 수정. 이름 수정은 `F2`

각각 타일링 값 디폴트 값은 512로 한다.

![타일링 머티리얼 그래프]({{"/images/unreal-M_RockyLandscpae-tilling.png"|relative_url}})



### 머티리얼 인스턴스

머티리얼 저장 후

콘텐츠 브라우저에서 M_RockyLandscape를 우 클릭해 머티리얼 인스턴스를 생성 후 이름을 (M 머티리얼)  MI_RockyLandscape 변경해준다. 테스트하고 싶은 랜드스케이프에 머티리얼을 인스턴스로 한 후

(MI 머티리얼 인스턴스)

![머티리얼 인스턴스]({{"/images/follow-unreal-rts-create-material-instance.png"|relative_url}})



아웃라이너에서 Landscape와 그 하위 모든 Landscape들을 전부 선택 후 (`Shift+좌클릭`으로 추가 가능) MI_RockyLandscape로 랜드스케이프 머티리얼로 에셋을 사용하자.

![머티리얼 인스턴스 에셋 사용]({{"/images/follow-unreal-rts-chose-material-instance.png"|relative_url}})



그리고 MI_RockyLandscape에 머티리얼 에디터를 탭에서 분리해 작게 별도로 열어 Global Scalar Parameter Values 각 타일링이 숫자를 변화시켜 테스트 가능하다. 변하지 않는 다면 머티리얼이 설정이 안되있는 것이다. 숫자 뒤에 연산을 넣는 것도 가능하다. 타일을 가지고 놀 수 있다.

값이 커야지 자연스러운걸 알 수 있다.  

![머티리얼 인스턴스 증가]({{"/images/follow-unreal-rts-increase-material-instance.png"|relative_url}})



## Add the normal textures to the landscape material

### 관련 텍스쳐 추가

 M_RockyLandscape 머터리얼 에디터로 돌아와서

N으로 끝나는 텍스쳐도 아까처럼 추가 랜드스케이프가 더 명확해질 것이다.

Layer Blend 노드를 복사하여 링크하고 Normal에 연결하여 아래처럼 만든다.

![타일링 N 추가]({{"/images/unreal-M_RockyLandscpae-tilling-add-n.png"|relative_url}})



### 경유 선언 노드 추가

하지만 N 텍스쳐들에게도 절대월드포지션과 타일링 변수 값을 연결해주어야 한다. 좀 더 깔끔하게 추가하기 위하여

D 텍스쳐와 연결된 Divde 노드들의 연결을 다 끊고 우클릭 name이라 쳐서 명명된 경유 선언 노드 추가...(reroute declaration node) 을 클릭 기존 Tiling 노드들 뒤에 Value를 추가하고 

![명명된 경유 선언 노드]({{"/images/follow-unreal-rts-reroute-declaration-node.png"|relative_url}})



경우 선언 노드에 이름을 Tiling으로 짓는다. 그리고 기존 파라미터 이름을 뒤에 Value를 추가 안해도 상관은 없다.

경우 선언 노드는 노드를 정리하기 편해서 좋다

기존 연결했던 UVs 뒤에 맞는 이름을 가진 경유 노드를 붙이자

![경우 선언 노드]({{"/images/unreal-M_RockyLandscpae-reroute-declaration-node.png"|relative_url}})



노드 그룹에서 `q`를 누르면 연결 정렬 해준다. 더 많은 정렬과 단축키는 우클릭 정렬에서 확인 가능

콘테츠 드로어에가서 틈틈히 모두 저장하자

저장하고 모두 저장도 해주자



### 언로드시

만약 저장하고 다시 켰는 데 내 맵이 보이지 않는다.

파일->레벨 열기->MyFirstRTS(초반에 프로젝트 명으로 지은 폴더)->Maps->RockyLevel을 열자

![레벨 언로드]({{"/images/follow-unreal-rts-rockylevel-unload.png"|relative_url}})



창->월드 파티션->월드 파티션 에디터를 추가하고

월드 파티션 탭에서 맵 전체를 드래그 한후 선택된 셀 로드하자

![월드 파티션 셀 로드]({{"/images/follow-unreal-rts-world-partion-editor-drag.png"|relative_url}})

여기까지 내가 아는 해결법이다.

편집->프로젝트 세팅->맵&모드->Default Maps->에디터 시작 맵을 RockyLevel로 설정하면 이런 현상이 덜 일어나는 것 같다.



여기까지가 44:43초까지 내용이다.

<https://github.com/programbaam/unreal-study/tree/e759a6d4d3da2066e00e1df8c670933554ded8d7/MyFirstRTS>

여기까지 한 프로젝트