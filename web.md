# web

### 웹 표준과 브라우저 전쟁

#### 1. HTML (Hyper Text Markup Language)

#### 2. HTML 기본 구조

```html
<!DOCTYPE html>
<html lang ="ko">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

- DOM 트리


- 요소(element)

- 속성(Attribute)

- Head

- 시맨틱태그

  - - header
    - nav
    - aside
    - section
    - article
    - footer
  



### HTML 문서 구조화

#### 1. 인라인 / 블록 요소

#### 2. 그룹 컨텐츠

- `<p>`
- `<hr>`
- 목록 `<ol>`, `<ul>`
- `<pre>`, `<blockquote>`
- `<figure>`, `<div>`

### 3. 텍스트 관련 요소

- `<a>`

- `<br>`, `<span>` , `<img>`

- `<p>`

- `<b>` , `<strong>` 

- `<em>`, `<i>`

#### 4. table

#### 5. Form



#### CSS selector

> 특정한 요소 선택하여 스타일링 하기 위해 반드시 필요한 개념
>

#### CSS 상속

- CSS는 상속을 통해 부모 요소의 속성을 ~~모두~~ 자식에게 상속
- MDN에서 확인 (구글에 MDN margin 검색)

### CSS 적용 우선 순위

- 중요도(importance) - 사용 시 주의
- 우선 순위
  - 인라인 / id 선택자 / class 선택자 / 요소 선택자
- 소스 순서



### 기초 CSS

- 크기 단위 (상대)
  - **`px` (**픽셀)
  - **`%`**
  - **`em`** : 배수 단위, **요소에 지정된 사이즈**에 상대적 사이즈 가짐
  - **`rem`** : 최상위 요소(html)의 사이즈 기준으로 배수 단위 가짐
  - viewpoint 기준 단위
    - `vw`, `vh`, `vmin`, `vmax`

- 브라우저의 폰트 기본 크기는 16px
  - 1.5 rem은  `16 * 1.5 = 24 px`
  - 1.5 em 은 상속 받아서 `24px * 1.5 = 36 px`

- 색상 단위
  - HEX
  - RGB
  - RGBA



### CSS

- 텍스트
- 컬러(color), 배경(background-image, background-color)
- 목록 꾸미기



### - Box model

- `margin : 10px` 은 상하좌우 모두 10px

- border도 shorthand가 있음

#### box-sizing

- 기본적으로 모든 요소의 box-sizing은 content-box
  - padding을 제외한 순수한 contents 영역만을 box로 지정
- 다만 우리가 일반적으로 영역을 볼 때는 border까지의 너비를 100px 보는 것을 원함
  - 그 경우 box-sizing을 border-box

#### 마진 상쇄 (Margin collapsing)

- top-bottom이 같이 주어지면 일어나는 현상
- 

### 레이아웃과 고급 CSS 기능

- 다단 레이아웃
- 네비게이션
- animation, transition - 요소 변형 / 클리핑



#### - CSS position

- static : 디폴트 값 (기준 위치)

- 좌표 프로퍼티(상 하 좌 우) 사용해서 이동 가능 (음수값 가능)


#### - CSS float

- 일반적인 흐름에서 벗어나도록(박스모델은 왼쪽 위로 붙는다는 배치) 하는 속성 중 하나



#### - CSS Layout

- 실습 - tag 선택자만 써서 구현. 

##### - [★] HTML/CSS 기본 특징

- 일반적으로 HTML 요소들은 문서의 **위 → 아래**로 순차적으로 나열
- 아래 방법 통해 변경
  - display 속성 통해 (표현되는) 방식 변경
    - block, inline, inline-block
  - position 속성 통해 위치 자체 변경
  - float 속성 통해 떠 있도록 만듦



#### - CSS 어렵게 만드는 요소

- float
- absolute positioning



### 자바스크립트

- CONSOLE 기준

- var 로 변수 선언

- 데이터 타입 분류 (typeof)

  - 원시 타입(primitive) - 변경 불가능한 값(immutable)
  - 객체타입(object)

- Number

  - NaN (넘버가 아니다) - 역시 넘버 타입..
  - 부동 소숫점 표현. -2^53 ~ 2^53 의 정수만 **안전하게 표현**

  - 이름 없이 하는 방법도 있고, 이름 선언해서 하는 방법도 있음

- 변수 유효 범위(scope)

  - 함수 레벨 스코프. 함수 내에서 선언된 변수는 지역 변수
  - 변수 선언 시 키워드(var)를 쓰지 않으면 암묵적 전역 설정

- 호이스팅과 let, const

  - 자바스크립트에서는 모든 선언을 호이스팅 한다.
  - 

### 배열 (Array)

##### - 배열 메소드

- sort() 

- 문자열 관련 - join / toString
- 배열 합치기 - concat

- 원소 삽입/삭제 - push, pop (뒤쪽) / unshift, shift (맨 앞)
- 인덱스 탐색 - indexOf
- 배열 조작 - splice

- 배열 자르기 - slice



###  문서 객체 모델 (DOM)

#### - DOM 조작

> 문서의 **구조화된 표현 제공**
>
> 구조화된 **노드와 오브젝트로 문서**를 표현

#### -  innerHTML, insertAdjacentHTML

- 보안적 취약점이 있으나 이 두가지 사용하면 됨



###  이벤트

#### - Event

- load, copy, mouseover, click, submit 등의 이벤트가 있다.

#### - Closure

> 함수와 함수가 선언된 어휘적 환경(Lexical scoping, environment)의 조합



### 레이아웃 배치

- flex를 쓰면 쉬움