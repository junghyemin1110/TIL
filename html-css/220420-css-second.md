# 오늘 한 일

## CSS 속성

### 개요

이제부터 배울 것들

> 박스 모델, 글꼴과 문자, 배경, 배치, 플렉스(정렬),  
>전환, 변환, 띄움, 애니메이션, 그리드, 다단, 필터


### 너비(width,height)

> width : 요소의 가로 너비
> height : 요소의 세로 너비

- 기본값으로 이미 속성의 값이 들어 있다.
  - span은 인라인 요소라  
가로,세로 너비가 입력한 값만큼 줄어들려고 한다. 
  - div은 블럭 요소라  
가로 너비는 최대로 늘어나려고 하고, 세로는 입력한 값만큼 줄어들려고 한다.

> max-width, max-height : 요소가 커질 수 있는 **최대**의 가로, 세로 너비를 뜻한다. 
>기본값은 none(없음), 최대 너비의 제한이 없고, px나 em, vw등의 단위로 지정한다.

> min-width, min-height : 요소가 작아질 수 있는 **최소**의 가로, 세로 너비를 뜻한다.
>기본값은 0, 최소 너비의 제한이 없고, px나 em, vw등의 단위로 단위로 지정한다.


### CSS 단위

- px : 픽셀, 화면에 출력하는 점 단위이다. 가장 많이 사용한다. 절대 단위는 아니다.
- % : 상대적 백분율을 나타낸다.
- em : 요소의 글꼴 크기, 1em=10px
- rem : 루트 요소(html)의 글꼴 크기, html 요소만!
- vw : 뷰포트의 가로 너비의 백분율이다.
- vh : 뷰포트의 세로 너비의 백분율이다.


### 외부 여백(margin)

- margin : 요소의 **외부** 여백을 지정하는 단축속성이다. 음수를 사용할 수 있다.
  - 0: 외부 여백이 없음을 뜻한다.
  - auto: 브라우저가 여백을 계산한다.
  - 단위는 px,em,vw로 지정한다.
  - margin의 방향(top,right,bottom,left)을 설정(시계방향순)할 수 있다.
    - 1개일 땐 모든 방향, 2개일 땐 margin: 10px(top,bottom) 20px(left,right);처럼 띄어쓰기로 나눠서 설정 가능하다.
    - 3개일 땐, margin: 10px(top) 20px(left,right) 30px(bottom);처럼 띄어쓰기로 나눠서 설정 가능하다.
    - 4개일 땐, margin: 10px(top) 20px(right) 30px(bottom) 40px(left);처럼 띄어쓰기로 나눠서 설정 가능하다.
  - margin-방향을 적으면 개별 속성으로 지정할 수 있다.


### 내부 여백(padding)

- padding : 요소의 **내부** 여백을 지정하는 단축 속성이다.(여백으로 인해 요소가 커지는 특성이 있다.)
  - 0: 내부 여백이 없음을 뜻한다.
  - 단위는 px,em,vw로 지정한다.
  - %: 부모 요소의 **가로 너비**에 대한 비율로 지정한다.
  - padding의 방향(top,right,bottom,left)을 설정(시계방향순)할 수 있다.
    - 1개일 땐 모든 방향, 2개일 땐 padding: 10px(top,bottom) 20px(left,right);처럼 띄어쓰기로 나눠서 설정 가능하다.
    - 3개일 땐, padding: 10px(top) 20px(left,right) 30px(bottom);처럼 띄어쓰기로 나눠서 설정 가능하다.
    - 4개일 땐, padding: 10px(top) 20px(right) 30px(bottom) 40px(left);처럼 띄어쓰기로 나눠서 설정 가능하다.
  - padding-방향을 적으면 개별 속성으로 지정할 수 있다.


### 테두리 선과 색상 표현

- border : 요소의 테두리 선을 지정하는 단축 속성이다. (여백으로 인해 요소가 커지는 특성이 있다.)
  -적는 순서 : border: 선-두께(border-width) 선-종류(border-style) 선-색상(border-color);
    - border-width : 단위는 px, em, %로 지정하고, width나 padding처럼 방향을 설정 가능하다.
    - border-style : 선의 종류를 지정하고, none(선 없음), solid(실선), dashed(파선) 을 많이 사용한다. border-width처럼 방향을 설정 가능하다.
    - border-color : 선의 색상을 지정하고, 색상이나 투명(transparent)을 입력하면 된다. border-width처럼 방향을 설정 가능하다.
      - 색상 표현은 색상 이름(red), Hex색상코드(#000), RGB(빛의 삼원색), RGBA(빛의 삼원색+투명도)를 사용한다. 
    - 기타 속성으로는 border-방향, border-방향-속성 을 지정할 수 있다. 


### 모서리 둥글게

- border-radius : 요소의 모서리를 둥글게 깎는 속성이다.
  - 0 : 둥글게가 없음을 뜻한다.
  - 단위는 px,em,vw로 지정한다.
  - 4개일 땐, border-radius: 10px(top) 20px(right) 30px(bottom) 40px(left);처럼 띄어쓰기로 나눠서 설정 가능하다.


### 크기 계산

- box-sizing : 요소의 크기 계산 기준을 지정한다.
  - content-box : 요소의 내용으로 크기를 계산한다. 수동으로 조절해야 할 수도 있다. 기본값이다.
  - border-box : 요소의 내용+padding+border로 크기를 계산한다.


### 넘침 제어

- overflow : 요소의 크기 이상으로 내용이 넘쳤을 때, 보여짐을 제어하는 단축 속성이다. 
  - visible : 넘친 내용을 그대로 보여준다. 기본값이다.
  - hidden : 넘친 내용을 잘라낸다.
  - scroll : x축, y축에 스크롤바를 만든다.
  - auto : 브라우저에서 자동으로 스크롤바를 만든다.
  - overflow-x : x축으로 넘치는 것만 체크한다.
  - overflow-y : y축으로 넘치는 것만 체크한다.


### 출력 특성

- display : 요소의 화면 출력 특성이다.
  - 각 요소에 이미 지정되어 있는 값
    - block, inline, inline-block 요소
  - 따로 지정해서 사용하는 값
    - flex: 플렉스 박스, 1차원 레이아웃이다.
    - grid: 2차원 레이아웃이다.
    - none: 보여지는 특성이 없고 화면에서 사라진다. 
  - 기타 등등,,
