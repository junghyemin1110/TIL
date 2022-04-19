# 오늘 한 일

## CSS개요

### 기본 문법과 주석
```css
선택자{속성:값;}
```
- 해석하자면 선택자의 속성은 값이다.

- 속성이 많아지면 한눈에 보기 어려우므로 들여쓰기를 습관화해야한다.
- 'tab'은 들여쓰기, 'shift+ tab'은 내어쓰기이다.
- /*설명작성*/ 주석은 'ctrl+/'으로 바꿀 수 있다.

### 선언방식

```html
<style>
  div {
    color: red;
    margin: 20px;
  }
</style>
```
- 내장방식: 선택자를 지정하여 스타일을 작성하는 방식이다. 
~~ 권장하는 방식은 아니다 ~~

```html
<div style="color: red; margin: 20px;"></div>
```

- 인라인방식: 요소에 스타일 속성에 작성하는 방식이다. 
우선시되기 때문에 유지보수에 악영향을 미치기에 권장하지 않는다.

```html
<link rel="stylesheet" href="./css/main.css">
```

- 링크방식: 외부 CSS문서를 가져와서 연결하는 방식이다.

- import 방식
@import 규칙으로 CSS문서 안에서 
또 다른 CSS문서를 가져와 연결하는 방식이다.

### 선택자-기본

- * : 전체 선택자, 모든 요소를 선택한다.
- ABC : 태그 선택자, 태그 이름이 ABC인 요소를 선택한다. 
- .ABC : 클래스 선택자, class 속성의 값이 ABC인 요소를 선택한다.
- #ABC : 아이디 선택자, id 속성의 값이 ABC인 요소를 선택한다.

### 선택자-복합

- ABCXYZ : 일치 선택자, 동시에 만족하는 요소를 선택한다.
(태그 선택자를 앞에 두는 습관 들이기)
- ABC>XYZ : 자식 선택자, 선택자 ABC의 자식 요소인 XYZ를 선택한다.
- ABC XYZ : 후손(하위) 선택자, ABC의 하위 요소인 XYZ를 선택한다. 
띄어쓰기가 선택자의 기호!!! 편리하게 사용 가능하다.
- ABC+XYZ : 인접 형제 선택자, 선택자 ABC의 다음 형제 요소인 XYZ **하나**를 선택한다.
- ABC~XYZ : 일반 형제 선택자, 선택자 ABC의 다음 형제 요소인 XYZ **모두**를 선택한다.

### 선택자-가상 클래스

특별히 동작하는 것들

- ABC:hover : hover, 선택자 ABC 요소에 
마우스 커서가 올라가 있는 동안 선택한다.
- ABC:active : active, 선택자 ABC 요소에 
마우스 커서가 클릭하고 있는 동안 선택한다.
- ABC:focus : focus, 선택자 ABC 요소가 포커스되면 선택한다.

동작이 아닌 것들

- ABC:first-child : first-child, 선택자 ABC가 형제 요소 중 첫째라면 선택한다.
- ABC:last-child : last-child, 선택자 ABC가 형제 요소 중 막내라면 선택한다.
- ABC:nth-child(n) : nth-child(n), 선택자 ABC가 형제 요소 중 (n)째라면 선택한다.
(n을 2n처럼 활용 가능, 0부터 시작해서 2,4,6,8 이런 식으로 짝수 선택)
(홀수는 :nth-child (2n+1) 으로 활용 가능, n+2로도 가능)
- ABC:not(XYZ) : 부정선택자, 선택자 XYZ가 아닌 ABC요소를 선택한다.


### 선택자-가상요소

- ABC::before : before, 선택자 ABC요소의 내부 앞에 내용을 삽입한다.
- ABC::after : after, 선택자 ABC 요소의 내부 뒤에 내용을 삽입한다.

요소의 내용이 무엇인지 content로 입력해줘야 한다.

### 선택자-속성

- [ABC] : ATTR, 속성 ABC을 포함한 요소를 선택한다.
- [ABC="XYZ"] : 속성 ABC을 포함하고, 값이 XYZ인 요소를 선택한다.

### 스타일 상속

- 부모요소에 적용된 스타일이 자식이나 하위 요소까지 상속되어 적용된다.
(font-style, font-weight, font-size, line-height, font-family, color, text-align ...)

-강제 상속: inherit, 자녀요소는 inherit 이라고 적으면 부모 값이 강제 상속된다.

### 선택자 우선순위

> 우선순위란, 같은 요소가 여러 선언의 대상이 된 경우, 어떤 선언의 CSS속성을 우선 적용할지 결정하는 방법이다.
>>점수가 높은 선언이 우선된다.
>>점수가 같으면, 가장 마지막에 해석된 선언이 우선된다.

```html
<div
  id="color_yellow"
  class="color_green"
  style="color: orange;">
  Hello world!
</div>
```
```css
div               { color: red !important; }
#color_yellow { color: yellow; }
.color_green   { color: green; }
div               { color: blue; }
*                  { color: darkblue; }
body            { color: violet; }
```
>여기서 적용되는 컬러는 무엇일까?
>>적용되는 점수 순서대로 적어보자면(명시도)
>> red-orange-yellow-green-blue-darkblue-purple 이다.

##내일 할 일
- 남아있는 css강의 듣고 잘 따라해보기
- 특강 집중해서 듣고 정리해보기


