# django

## Grid System 개념

### HTML / CSS의 배치 핵심

> 왼쪽 위에 쌓인다.
>

- float
- position : absolute / fixed



## flex

- `flex` 이전에는 배치를 위해서 `float` , `position` 지정을 해야 했다.

### flex 주요 개념

- `container` , `item`

- `main axis` (주축) , `cross axis` (크로스축)



## flex 속성

### 1. flex-grow

> flex-grow는 남은 영역을 나누어 가진다.
>

### 2. justify-content

> main 축을 기준으로 정렬한다.

### 3. align-items

> cross 축을 기준으로 정렬한다.

(+) `align-items` : 전체 요소를 설정 / `align-content` : 요소 사이의 간격

### 4. order

> 아이템의 순서를 정의할 수 있다.

### 5. align-self

> 아이템에 직접 align 지정할 수 있음



## Bootstrap

- CDN  (Content Delivery (distribution) Network)

  > 컨텐츠(CSS, JS, image, Text 등)을 효율적으로 전달하기 위해 여러 노드에 가진 네트워크에 데이터를 제공하는 시스템

### 1. Utilities

#### 1.1 Spacing

- `.m-0` : `margin: 0;`
- `.mr-0` : `margin-right: 0;`
- `.mx-0` : left와 right이 x축이므로 `margin-left: 0;` & `margin-right: 0;`
- `.py-0` : `padding-top: 0;` & `padding-bottom: 0;`
- `.mt-1` : `margin-top: 0.25rem` (0.25rem은 16px * 1/4 = 4px)
- 뒤의 숫자는 0부터 5까지. 음수는 `n1`로 사용

#### 1.2 Color

- `.bg-primary` : `background-color: primary;`
- `.text-success` : `color: succese;`
- `.alert-warning`

#### 1.3 border

> 기본값 : `border : 1px solid

#### 1.4 display

- `.d-block` : `display: block;`
- `.d-sm-none` : 반응형 맛보기. 특정한 너비가 넘어가게 된다면 none으로 하겠다.

#### 1.5 position

- `.position-static` : `position: static;`
- `.fixed-top` : 사실상 nav 고정과 같음

#### 1.6 Text

- `.text-center`

#### 1.7 justify-content

- `.justify-content-center`



### *Responsive web*

#### alert

> 새로고침을 하면 사라지는 형태의 정보

#### badge

> 쇼핑몰 new와 같은 것. span 처리되어 있음.

#### breadcrumb

> 페이지 위치 경로

#### Card view

> 텀블벅 같은 ui

#### carousel

> 이미지가 넘어가도록(여러개의 이미지 사용)하는 것
>

#### modal

> 새로운 창을 띄우는 것



### Layout

#### - Grid

> 전체 큰 틀을 Grid로 짜는 경우가 많음
>
> flex로 구현된 것
>
> `Container - row - col` 의 3단 구조임을 꼭 기억할 것

- Mix and Match
  - `.col-  ` `.col-sm-`  `.col-md-`  `.col-lg-`  `.col-xl-` 
  - 반응형을 쉽게 할 수 있음
  - 한 행을 row로 묶어서 하는 것이 point. row 위에는 항상 container가 존재.

- `.col`, `.col-sm`, `.col-md`, `.col-lg`,`.col-xl`
- ![breakpoint](https://k.kakaocdn.net/dn/pxzQq/btqCX9UcWZd/u4flAMckyJJGEAWMbD0hTK/img.png)

### Django

> python 기반의 web framework

#### 1.`urls.py` 에서 경로 연결

#### 2.`views.py` 에서 함수 정의

#### 3. `template` 파일 생성

- DTL (Django Templates Language)



### 사용자 정보 처리(Form) 로직


### Model

#### 스키마 (Schema)

> 각 열(column)들이 어떤 데이터 타입을 가지게 되는 지 정의함



> 체계화해서 통합, 관리하는 데이터의 집합

### migration

> 모델의 변경사항들을 데이터베이스 스키마에 반영하는 방법

- Model (필드)생성 / 수정 / 삭제 등
- migration 파일 생성
  - migration 파일은 DB 스키마를 위한 버전관리 시스템(git)이라 생각
- migrate 통해 데이터베이스에 적용



### 파일 업로드 HW/WS 해설

기본구조

- 요청(request)을 보낸다

  > url로 보낸다.

- 응답(response)을 받는다.

  > html로 받는다.

  

#### - HTTP 요청 메서드

- GET : 특정 리소스의 표시를 요청. 데이터를 받기만 함
- POST : 특정 리소스에 엔티티(form 양식을 넣어서)를 제출할 때. 서버 상태의 변화



### STATIC (정적)

> CSS, JS, image를 스태틱파일이라고 함
>
> app 폴더 안에 `static` 폴더 - `app명 폴더`  - 안에 파일 생성



#### accounts의 signup(가입) 구현

> articles와 같이 기존의 방식대로 구현하면 안됨
>
> - user DB에서 가장 중요한 것은 password



### 쿠키 개념도

- HTTP 프로토콜은 상태x 연결x 이므로 쿠키에 정보를 담아 요청

- 쿠키는 외부 노출, 사용자의 정보이므로 100% 확신할 수 없음

  ∴ 세션을 사용 - 만료기간, 논리, 값 등을 기록



### 캐시

> 사용자가 한 번 방문한 페이지에 대해서 리소스를 캐시 데이터를 통해서 좀 더 빨리 로딩할 수 있도록 해줌
>
> 또 다른 저장소라고 생각하면 됨





### SQL (Structured Query Language)

> 데이터베이스 관리하기 위해 설계된 특수 목적의 프로그래밍 언어
>
> RDBMS에서 자료 검색·관리, DB 스키마 생성·수정, DB 접근관리 등을 위해 고안



### 데이터베이스 관계 (1:N)

​    `reporter = models.ForeignKey(Reporter, on_delete=models.CASCADE)`

#### 일대다 관계

- 개념 이해

  1명의 기자가 여러 개(0 ~ N)의 글을 쓸 수 있음

  (+) 어떤 값이 저장될 지를 그려보는 게 좋다.



### 코드 작성 흐름 ( U → V → T )

>  하나의 요청을 처리하기 위해서

#### Url

> 1. 패턴 (url → view)
> 2. 이름

- 기본 : `(path) url` → `view의 함수`
  - urlpatterns = [`path('create/', views.create)`]
    - 다양한 url 패턴들을 들고 있는 공간
  - `app_name=____` → `path('', viesw.index, name='index')`
    - url의 변수화: template / view 변경 X
    - `app_name`: app별 namespace

#### View

> 함수 (인자 → 반환 return)

#### Templates

> HTML 파일을 만들어 주는 것 ← DTL
>
> - context(dict) 에 넘어온 값을 넘겨줌
>
> - context-porcessors →  `request.user`
>
>   →  확장(상속) : `base.html` - 받아오는 것 `{% extends %}`



#### Auth

> 모델 (User)
>
> - 가져다 씀: ModelForm / Form (UserCreationForm, ... )
> - Costom: 가져다가 상속

| 기능     | Model | 가져옴             | form      |
| -------- | ----- | ------------------ | --------- |
| 회원가입 | User  | UserCreationForm   | ModelForm |
| 로그인   | X     | AuthenticationForm | Form      |



### HTTP 상태 코드 (http response)

- 4xx

  - 401(권한 없음) : 인증 안됨(is_authenticated)
  - 403(금지됨) : 필요한 권한을 가지고 있지 않음
  - 404(찾을 수 없음)
  - 405(허용되지 않음)



