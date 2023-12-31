# bootcamp TIL

## HTML

### HTML 정의

**H**yper**T**ext : 하이퍼텍스트르 가장 중요한 특징이라고 하는

**M**arkup : 마크업 형식을 가진

**L**anguage :　컴퓨터 프로그래밍언어

사람과 웹브라우저에서 서로 이해할 수 있는 약속/언어

### Tag

```
html -> 확장자
웹브라우저로 열림
<strong>진하게 하고싶은 말</strong>
시작태그                  닫히는 태그
<h1>제목</h1>  큰글씨, 한줄 띄워줌
<h2>소제목</h2>  제목 보다 글씨 쫌더 작게해줌
```

### 속성

`(<a href=“https...”>링크</a>)` -> 현재 웹페이지에서 열림

`(<a href=“https...”target="-blank">링크</a>)` -> 다른 웹페이지에서 열림

`(<a href=“https...” title="전설적인 프로그래머">)`-> 커서

### 목록

list

`<li></li>하면 목록으로 나눠짐 `

#### 그루핑

`<ul></ul>` 같은 성격끼리 묶고 다른 성격끼리 나누는 (unordered list)

`<ol></ol>` 순서가 있는 list (ordered list)

### 탭이름

```
<title>HTML – 수업소개</title>

만약 글씨가 깨진다면??
<meta charset=“utf-8”>

h1~끝 : 본문
위에 title이나 utf같은 경우는 본문X, 문서를 꾸미는 역할 (부가적 정보)
다른 태그에 담도록 약속
<head> -> 본문이 아닌 태그
<body> -> 본문
이것들은 전부 <html> 태그 안에 있어야함
그러니까
<html>
<head>
</head>
<body>
</body>
</html>
이렇게

Doctype 그냥 앞에 무조건 넣어라
<!DOCTYPE html>
```

**열리는 태그 썼으면 바로 닫히는 태그 쓸 것**

### p태그 (paragraph)

단락 – 줄바꿈과 여백

`<p>`한 단락`</p>`

`<br>` 줄바꿈

`<p>`의 디자인 넓이 이런거 css를 통해 바꿀수 있음

`<br>` 여러번 써도 됨 그냥 줄바꿈 단락 x

### 이미지

img src=“이미지이름.jpg”

너비 정하고 싶으면 width=“”

높이 정하고 싶으면 height=“”

근데 둘다 정하면 원래사진이 구겨지니까 height만 해라

alt=“이미지설명” -> 이미지가 깨졌거나 사라졌을 때 이미지 깨진걸 보여주고 설명해줌 (대체제 alternative text) 쓰는게 좋다

title=“도움말”

### 표 삽입(table)

```
항목 하나하나를 td로 묶어야함
<td>이름</td> 이런식으로 다 묶어
이것들을 또 tr로 묶어야 함
이것들을 또 table로 묶어야 함
table테두리 만드려면 table border=“숫자” 해야함
따라서
<table border=“숫자”>
<tr>  -> 행
<td>항목</td><td>항목</td>  -> 칸
</tr>
여러개 하고
</table>
이렇게
이쁘게 하려면 css필요
디자인하는데 예전에는 많이 썼음
table에서는 thead tbody이런식으로.. 보기엔 차이없지만
각 항목의 제목부분을 td대신 th로 바꾸면 굵어짐
tfoot넣어도 됨 마지막
```

#### 표 병합

세로 병합하고자 하는 시작 칸에 `<td rowpan=“몇개”>`

가로 병합하고자 하는 시작 칸에 `<td colspan=“몇개”>`

**겹치는거 지우기**

### form

```
아이디 비밀번호 만드는 것

<form action="로그인 성공하면 갈 주소">
<p>아이디 : <input type="text"></p>
<p>비밀번호 : <input type="password"></p>
<input type="submit">
</form>

서버전송 url로 됨

글씨를 넣고 싶다면?
input타입의 text와, input타입의 password와, 여러줄을 입력받는 textarea
<p>text : <input type="text" name="id" value="default value"></p>
<p>password : <input type="password" name="pwd" value="default value"></p>
<p>textarea:
      <textarea cols="50" rows="2">default value</textarea>
</p>
```

### 선택

이제 form을 선택할 수 있어
head에 글씨 안깨지게 `<meta charset="utf-8">` 하고
body에 선택할수 있게 하는데 다중선택도 할수있음

#### 라디오 버튼

여러개의 선택지중에 하나 또는여러개를 선택할수 있음

`<input type="radio">`

name값이 같은 것들끼리 그루핑이 되는것이고 같은 그룹중에 하나가 선택되면 나머지는 해제됨

#### 체크박스

같은그룹에도 여러개 선택가능

데이터 전송 : form action =“주소”

### hidden field

ui가 없지만 서버로 어떤 값을 전송하고 싶을때는 hidden이라고 하는 type의 input태그를 쓰면 된다

### label

이름 말해줄 때 이름: 대신

`<label>`이름` </label>``
 `<label for=“id_txt”>`text :`</label>``

### method

get방식 :　아이디, 패스워드 url에 다보임. url로 데이터 전송

post방식으로 바꾸니까 안보임 url말고 다른방식으로 숨겨서 전송

form을 이용하면 거의 100프로 post

### 파일 upload

파일을 선택해서 저장하게 만드는

전송 : submit

form태그에 method를 post형식으로 저장

enctype = “multipart/form-data”

### 폰트태그

**쓰지마라 퇴출된 태그**

꾸며줌 3이 기본값인데 1~7까지의 값 글자가 커지고 작아지고, 글자 색 바꿀수 있고

하지만 font는 아무 의미를 가지고 있지않다?

의미있는 것들 사이에서 어지럽힘 반복적, 가독성x
css가 디자인 담당이 됨

html은 정보집중

### meta태그

데이터를 설명하는 데이터

tag들도 meta

제목(title), 요약, 키워드, .. 본문을 설명하는 정보들

utf-8 보이진 않지만..

**인코딩** : 정보들을 컴퓨터에 저장하는 것

**디코딩** : 저장되어있는 정보를 꺼내서 화면에 표시하는 과정

### 시멘틱(의미론적인)태그

| 태그 이름 | 설명                                                        |
| --------- | ----------------------------------------------------------- |
| article   | 본문                                                        |
| aside     | 광고와 같이 페이지의 내용과는 관계가 적은 내용들            |
| details   | 기본적으로 표시되지 화면에 표시되지 않는 정보들을 정의      |
| figure    | 삽화나 다이어그램과 같은 부가적인 요소를 정의               |
| footer    | 화면의 하단에 위치하는 사이트나 문서의 전체적인 정보를 정의 |
| header    | 화면의 상단에 위치하는 사이트나 문서의 전체적인 정보를 정의 |
| main      | 문서에서 가장 중심이 되는 컨텐츠를 정의                     |
| mark      | 참조나 하이라이트 표시를 필요로 하는 문자를 정의            |
| nav       | 문서의 네비게이션 항목을 정의                               |
| section   | 문서의 구획들을 정의 (참고)                                 |
| time      | 시간을 정의                                                 |

설명이 되거나 네비게이션의 역할이면 `<nav></nav>`

본문이면 `<article></article>`

article을 section으로 묶을수 있음

### 검색엔진 최적화(seo)

네이버나 구글 같은
사이트에있는 html을 해석해서 사용자들이 검색했을 때 적합한 컨텐츠를 제공

의미론적인 타당한 태그로 설명하기

적절한 수준의 검색엔진 최적화 필요

- **사이트 구조** - url구조 개선, 사이트 내 이동 쉽게

- **콘텐츠 최적화** – 이미지사용, 제목태그

- **검색로봇** – 원하는 부분만 나오게

- **모바일 최적화** – 모바일용 사이트..

- 사이트 홍보 분석

광고나 그런거 말고 기본 검색결과만 검색엔진 최적화에 영향을 미침

`<title>`먼저 `<li>`보다 그래서 적합한 태그를 사용해야함

잘 대표하는 title태그 작성하기

discription태그는 짧고 간단하게

url을 콘텐츠에 맞게 작성하는 것이 좋음 (일반적x, 반복x, 복잡x, 같은 컨텐츠 여러개x ..)

같은 컨텐츠인데 다른 url이 있다면 link rel=“canonical 링크 이렇게 넣기

**리다이렉션** – 사용자가 어떤 php로 갔을 때 다른 php로 튕기는거

홈페이지에 다른 곳으로 이동할수 있는 링크가 잘 되어 있어야한다.

하위페이지에 사이트 이동경로 링크가 표시되어야 한다.
url일부를 제거해도 다른 웹페이지로 이동할 동선을 제공한다

주렁주렁 뭘 달아놓으면 안됨

`<a>`텍스트를 작성할 때 일반적인텍스트 안됨

url a텍스트 안됨

링크를 눈에 띄기 쉽게 표현 - css로 링크 디자인을 다 바꿀수 있으니까 이뻐보이긴하지만..

### 이미지 사용 최적화

이미지 깨질 때 alt텍스트 출력 스크린 리더 같은 기기를 사용할 때 그림의 내용을 말로 전달

일반적으로 많이 쓰는 디렉토리 명에 이미지를 저장하는 것이 좋다.

이미지의 이름에는 의미를 부여하는 이름이 더 좋음

이미지 `<a>`태그로 감싸면 링크를 걸수있기 때문에 다른 웹페이지로 이동할수 있음

### 로봇의 접근 robots.txt

웹사이트를 하면 수많은 로봇들이 접근함,
접근허용/접근 허용x

/ : 어떠한 로봇의 접속도 허락하지 않는다.
disallow는 못가져감. 다른 곳에서
보안도구로 사용 x

xml? 어떤 링크들이 그 페이지에 들어 있는지 어떤 페이지로 연결될수 있는지
sitemap제공

### 페이지랭크

c,d,e 가 a를 가리키고 b는 그냥 혼자라면
검색했을 때 a가 먼저 뜸  
페이지랭크가 높은 사이트가 페이지 랭크를 하면 더 먼저 뜸
스팸은 페이지 랭크를 높이고 많이 퍼질수록 많은 사람들에게 노출되고 더 유입되고 ..

ex) 야후 검색엔진 투자 중지 구글에게 검색엔진 넘김

### 웹 개발자도구

태그를 분석하고 싶으면 마우스 올리고 검사 하면 그 부분 영역에 html코드가 나옴

내가 만든 사이트가 아니어도 html볼수있음

페이지 소스보기 하면 전체 html코드 확인할수있음

태그를 선택하면 어떤 css코드가 적용이 됐는지도 보여줌 – styles

toggle 누르면 켜지고 다시누르면 사라지고
ipad, 스마트폰 기종, 뭐 선택하면 그기서 보이는 것처럼 보인다. - 디바이스모드

network
img 태그를 만나면 웹서버에서 다운로드 받고 저기에서 보여줌

파일을 열면서 어떻게 변화되는지 보여줌
웹페이지가 모바일에서도 잘 표현되는 방법
우클릭 검사 ctrl shift m누르면 됨

`<meta name="viewport" content="width=divice-width,initial-scale=1.0">`

화면에 크기를 디바이스크기에 맞게

### 새로운 제출양식들

form과 관련된 양식

input type의 변화- 다양해짐

type – 사용자의 입력을 규제하는 것과 관련

inputtype에 숫자를 넣으면 모바일에서는 숫자 치기가 편하게 숫자 키보드가 뜬다

사용자가 유효하지 않은 정보를 입력하면 브라우저가 막는다

**input types**

- color
- date
- datetime (현재x)
- datetime-local (현재 X)
- email
- month
- number
- range
- search
- tel
- time
- url
- week

### 새로운 속성

autocomplete="on" 전에 한거 기억하고있다가 해줌 모든 input tag 활성화

placeholder=”＂칸에 흐릿한 글씨로 적힘

autofocus 해놓으면 처음부터 커서가 거기로 가있음

### 입력값 체크

type email인데 email아니면 이메일로 바꾸라고 함

필수적 입력은 required
필수적이지 않으면 그냥 냅두고

**패턴 + 정규표현식**

pattern="[a-zA-Z]＂이렇게 하면 되는데 이렇게 하면 한 개만 칠 수 있고

pattern="[a-zA-Z][a-zA-Z]“ 이렇게 하면 두 개 입력할 수 있고
아무거나 해도 되면 . 하면됨

.+ 이면 어떤문자든 하나이상

**만약에 첫글자가 알파벳이고 뒷글자가 숫자인 것을 만들고 싶으면?**

pattern=“[a-zA-Z].+[0-9]”

**form validation은 편의 느낌 전적으로 신뢰하면 안됩니다**
