# 오늘 한 일

## css 속성

### 투명도(opacity)

- 요소의 투명도를 뜻한다. 0~1사이의 소숫점 숫자로 표현한다. 
  - 0이면 완전 투명, 1이면 완전 불투명이다.


### 글꼴(font)

- 여러가지 속성
  - style : 글자의 기울기를 뜻한다. 기본값은 normal이며 italic(이텔릭체)가 대표적이다.

  - weight : 글자의 두께를 뜻한다. 기본값은 (normal, 400)이며 bold는 두껍게, 뒤에 숫자는 100단위로 사용한다.

  - size : 글자의 크기를 뜻한다. 기본값은 16px이고, 단위는 px,em,rem으로 지정한다.

  - line-height : 한 줄의 높이를 뜻한다. 행간과 유사하고, 숫자는 글꼴 크기의 배수로 지정하고(권장), 단위는 px,em,rem으로 지정한다.
    - 원래는 정렬의 의미로도 사용했는데 플렉스가 대체하고 있다.

  - family : font-family: 글꼴1, "글꼴2", 글꼴계열; 일 때, 글꼴2는 후보이다.
    - 글꼴을 인식하지 못하는 경우가 생길 수 있어 ""로 묶어주는 게 좋다.
    - 마지막에 글꼴계열을 **필수**로 지정해야 한다.
      - 글꼴계열은 거의 고딕(sans-serif)체 계열을 쓴다. 코딩에서는 고정너비 글꼴 계열(monospace)을 자주 쓴다. 
      - 또 다른 글꼴계열로는 바탕체(serif), 필기체(cursive), 장식 글꼴계열(fantasy)이 있다. 


### 문자(text)

- color : 글자의 색상이다. 기본값은 검정(black)이다.
  - 색상표현방식을 활용하면 된다.

- text-align : 문자의 정렬 방식이다. 기본값은 left이다.

- text-decoration: 문자의 장식이다. 기본값은 none이고, 밑줄(underline), 중앙선(line-through)가 있다.

- text-indent : 문자 첫 줄의 들여쓰기를 말한다. 음수를 사용하여 내어쓰기를 할 수 있다. 
  - 단위는 px,em,rem으로 지정한다.


### 배경(background)

- background-color :  요소의 배경 색상을 뜻한다.
  - 색상과 투명함(transpatrent)으로 표현할 수 있다.

- background-image : 요소의 배경 이미지 삽입을 뜻한다.
  - url("")로 이미지 경로를 지정할 수 있고, none은 이미지 없음이다.

- background-repeat : 요소의 배경 이미지를 반복한다는 뜻이다.
  - repeat : 이미지를 수직, 수평으로 반복하겠다는 뜻이다.
  - repeat-x : 이미지를 수평 반복하겠다는 뜻이다.
  - repeat-y : 이미지를 수직 반복하겠다는 뜻이다.
  - no-repeat : 반복하지 않겠다는 뜻이다.

- background-position :  요소의 배경 이미지 위치를 뜻한다.
  - 방향 : top,bottom, left, right, center 방향으로 설정하는 방식이다.(띄어쓰기로 두 방향도 설정 가능함)
  - 단위 : px,em,rem으로 지정하는 방식이다.

- background-size : 요소의 배경 이미지 크기를 뜻한다.
  - auto : 기본값, 이미지의 실제 크기를 반영한다.
  - cover : 더 긴 너비에 맞춘다. 
  - contain : 더 짧은 너비에 맞춘다. 

- background-attachment : 요소의 배경 이미지의 스크롤 특성을 뜻한다.
  - scroll : 기본값, 이미지가 요소를 따라서 같이 스크롤된다.
  - fixed : 이미지가 뷰포트에 고정되어 스크롤되지 않는다.


### 배치(position)

- position: 요소의 위치 지정 기준이다. 

  - static : 기본값, 기준이 없다는 뜻이다.

  - relative : 요소 자신을 기준으로 배치한다. 
    - 이동되어 보이는 것이지 실제로는 허상이라 사이 요소라면 공간이 떠 보일 수 있다.

  - absolute : 위치 상 부모 요소를 기준으로 배치한다.
    - 1,2,3번이 있다면 요소가 주변과 상호작용이 무너지고 요소가 겹칠 수 있다. 
    - 뷰포트가 기준이 되어 위치상의 부모요소를 자청할 수도 있다.
    - 부모요소(static)와 상위요소(relative)가 있을 때, 상위요소를 기준으로 배치한다.
    - 부모요소와 상위요소가 모두 (static)이면 뷰포트를 기준으로 배치한다.

  - fixed : 뷰포트(브라우저)를 기준으로 배치한다.
    - 부모요소와 상위요소가 모두 (relative)여도 뷰포트를 기준으로 배치한다.

  - 같이 사용하는 속성들
    - top,bottom, left, right : 각 방향별로 거리를 지정할 수 있다.
      - auto: 기본값, 브라우저가 계산한다. 
      - 단위는 px,em,rem으로 지정하고 음수도 사용 가능하다.
 

  - 요소 쌓임 순서 (Stack order) : 어떤 요소가 사용자와 더 가깝게 있는지 결정한다.
    - z-index: 음수 사용 가능하다. 기본값은 auto(0)이다.
  1. 요소에 position 속성의 값이 있는 경우 위에 쌓인다.
  2. 1번 조건이 같은 경우, z-index 속성의 숫자 값이 높을수록 위에 쌓인다.
  3. 1,2번 조건이 같은 경우, HTML의 다음 구조일수록 위에 쌓인다.

  - 요소의 display가 변경됨
    - position 속성의 값이 absolute나 fixed일 때, block 요소처럼 인식한다는 거 기억하자.


### 플렉스(정렬) container

- flex : 1차원 레이아웃으로 x축, y축
  - display : flex container의 화면 출력 특성을 뜻한다. 
    - flex : 블록요소와 같이 flex container을 정의한다.
    - inline-flex : 인라인요소와 같이 flex container을 정의한다.

  - direction : flex container의 주 축을 설정한다. 수평인지 수직인지!
    - row : 기본값, 행 축을 뜻한다. 좌에서 우로 이어진다.
    - row-reverse : 행축이 우에서 좌로 이어진다. 
    - x가 주 축이 되고 y가 교차축이 된다. 시작점과 끝점이 존재한다.

- flex-wrap : Flex Items 묶음(줄 바꿈)의 여부를 뜻한다.
  - nowrap : 묶음 없음을 뜻한다.
  - wrap : 여러 줄로 묶는다는 뜻이다. 칸이 모자라면 줄바꿈해서 다음 줄로 출력한다.

- justify-content : 주 축의 정렬 방법(수평정렬)을 뜻한다.
  - flex-start : Flex Items를 시작점으로 정렬한다는 뜻이다. 
  - flex-end : Flex Items를 끝점으로 정렬한다는 뜻이다. 
  - center : Flex Items를 가운데 정렬한다는 뜻이다.

- align-content : 교차 축의 **여러** 줄 정렬 방법을 뜻한다. 
  - **항목이 2줄 이상이고 여백이 존재해야 한다.**
  - stretch: 기본값, Flex Items를 시작점으로 정렬한다. 
    - 높이가 설정되지 않으면 최대한으로 늘어나려고 한다.
  - flex-start : Flex Items를 시작점으로 정렬한다는 뜻이다. 
  - flex-end : Flex Items를 끝점으로 정렬한다는 뜻이다. 
  - center : Flex Items를 가운데 정렬한다는 뜻이다.

- align-items : 교차 축의 **한** 줄 정렬 방법을 뜻한다.
  - stretch: 기본값, Flex Items를 시작점으로 정렬한다.
    - 높이가 설정되지 않으면 최대한으로 늘어나려고 한다.
  - flex-start : Flex Items를 시작점으로 정렬한다는 뜻이다. 
  - flex-end : Flex Items를 끝점으로 정렬한다는 뜻이다. 
  - center : Flex Items를 가운데 정렬한다는 뜻이다.

### 플렉스(정렬) items (flex- 뒤에 붙는 요소들)

- order : Flex Item의 순서를 뜻한다. 
  - 숫자가 작을수록 먼저이고, 0은 순서가 없는 것이다.

- grow : Flex Item의 증가 너비의 비율을 뜻한다.
  - 숫자는 증가 비율을 뜻하고, 기본값인 0은 증가 비율이 없는 것이다.

- shrink : Flex Item의 감소 너비의 비율을 뜻한다.
  - 숫자는 감소 비율을 뜻한다.
  - 기본값은 1은 Flex Container 너비에 따라 감소 비율을 적용한다.

- basis : Flex Item의 공간 배분 전의 기본 너비를 뜻한다.
  - auto : 기본값, 요소의 content 너비를 뜻한다. 
  - 단위는 px,em,rem으로 지정하는 방식이다.


### 전환(transition)

- transition : 요소의 전환(시작과 끝)효과를 지정하는 단축속성을 뜻한다.

- transition: 속성명 지속시간(필수 포함 속성) 타이밍함수 대기시간 순으로 작성한다.
  - property : 전환 효과를 사용할 속성 이름을 지정한다. 
    - all은 모든 속성을 지정한다.
    - ,로 다른 속성도 함께 지정할 수 있다.

  - duration : 전환 효과의 지속시간을 지정한다. 기본값인 0s는 전환효과가 없다.

  - timing-function : 전환 효과의 타이밍(easing) 함수를 지정한다.
    - ease : 기본값, 느리게-빠르게-느리게  
    - linear : 일정하게
    - ease-in : 느렸다가 빨라지게 
    - ease-out : 빨랐다가 느려지게
    - ease-in-out : 느렸다가 빨라졌다가 다시 느려지게


### 변환(transform)

- 2D 변환 함수
  - translate(x,y) : x축, y축으로 이동한다. px로 입력한다. 
  - translateX(x) : x축으로 이동한다. px로 입력한다. 
  - translateY(y) : y축으로 이동한다. px로 입력한다. 
  - scale(x,y) : x축, y축으로 이동한다. 찌그러질 수 있어 둘 다 입력한다.
  - rotate(degree) : 회전하는 각도를 입력한다. deg라는 각도 단위로 입력한다.
  - skewX(x) : x축으로 기울인다.
  - skewY(y) : y축으로 기울인다.

- 3D 변환 함수
  - rotateX(x) : x축으로 회전한다. deg라는 단위로 입력한다.
  - rotateY(y): y축으로 회전한다. deg라는 단위로 입력한다.
  - **perspective(n)** : 원근법 함수로 제일 앞에 작성해야 한다. 
    - 원근거리를 만든다. px로 입력한다. 관찰대상에 적용한다.

- perspective : 원근 거리를 만드는 속성이다. 관찰 대상의 부모에 적용한다. 함수 아니다.

- backface-visibility : 3D 변환으로 회전된 요소의 뒷면 숨김 여부를 뜻한다.
  - visible은 기본값으로 뒷면 보임, hidden은 뒷면 숨김이다. 


## 내일 할 일

실시간 특강 듣고 SCSS강의 들으며 예제 실습해보기
