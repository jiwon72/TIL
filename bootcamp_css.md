# bootcamp TIL

## CSS

### CSS란

shtml은 웹디자인 x

font 태그를 쓰지 않는다

대신 css `<style></style>`을 사용

style사이에 명령을 함

```
<style>
li{
 color:red;
}
</style>
```

글자를 빨간색으로 만들어주세요 라는 뜻

`<li><font color=“red”><HTML</font><li>` 원래는 이랬는데

이걸 모든줄에 적용하려면 너무 힘들고 파랑으로 바꾸려면 하나하나 다 바꿔야됨

파일열기 : ctrl + o

`<h1 style="color:red">Hello world</h1>`

여기에서 style=“”는 html문법이고 color:red만 css임

이렇게 해도 되고

```
<head>
        <style>
            h2{color:blue}
        </style>
<h2>Hello word</h2>
    </body>
```

여기서도 `<style>`은 html이고 h2{color:blue}는 css임

이렇게 해도 되고

두가지 꾸미는 것을 같이 하고싶다면, 하나 하고 ; 해야됨 구분을 위해

색깔;
밑줄;
이런식으로

### css selector

h1{color:red;font-size:12px;}
선택자 속성 속성값 구분자 선언

#### 선택자 종류

- **태그 선택자**

  ex) li

- **아이디 선택자**

  li는 모두 선택하는 거고 한단어만 하고싶거나 하나만 선택해서 효과를주고싶다면

  `<li id="select">CSS</li>` 이렇게 하면 css만 선택인거고

  위에 `<style>`에서 #select{}해서 하고싶은거 하면 됨

- **클래스 선택자**

  `<li class=“하고싶은거” ></li>`

  여기있는 전체 class를 바꾸고 싶다면 .하고싶은거 {} 하기

  다른태그를 그루핑 할 수 있다.

- **부모 자식 선택자**

  선택자에서 띄어쓰기를 하면
  ul li
  라고한다면 ul 밑에있는 li를 말하는 것이다.

  border-두께 solid:단선

  ol>li 이렇게 하면 직계자손만 해당됨

  배경색 : background-color

  따로하면 불편하니까 ul,ol 하면 둘다에 적용됨

- **선택자 팁**

  flukeout.github.io 선택자 게임

  이미지 검색 css cheatsheet selector 해보기

### pseudo class selector 가상 클래스 셀렉터

id 도 아니고 tag도아니고 class처럼 동작하지만 class는 아니고 특수한 선택
엘리먼트의 상태에 따라서 ..

```
pseudo
a:active{
         color: green;
            }
```

누르고 있을 때 초록색 됨

```
a:hover{
         color: yellow;
            }
```

커서를 올리면 노란색 됨

동시에는 안됨 동급이면 아래쪽을 선택 그래서 커서를 올리고 누르면 초록색 안되지만 누르면서 커서를 누르는곳에서 멀리 가져가면 초록색으로 변함

```
a:focus{
               color:white
           }
```

이렇게 하면 tap키 누르면 하늘색 네모에 안에 하얀색으로 선택 되는데 enter키 누르면 들어갈수있음
되도록 맨 마지막에 할 것

### 여러 가지 선택자

| 상황                                    | 선택자                  |
| --------------------------------------- | ----------------------- |
| id값                                    | #id                     |
| 자손                                    | A B                     |
| 자손과 id조합                           | #id A                   |
| class값 전부                            | .classname              |
| 어떤 것 선택하고 그것의 전부class       | A.classname             |
| 두 개 다 선택할 때                      | A,B                     |
| 모든 element                            | \*                      |
| 뭐 밑에 있는 모든 tag                   | A\*                     |
| 인접한 sibling                          | A+B                     |
| 일반적인 sibling A에 인접한 모든 B      | A~B                     |
| 직계자식                                | A>B                     |
| 가장 첫 번째 있는거 선택                | :first-child            |
| 혼자 단독 자식일 때                     | :only-child             |
| 가장 뒤에있는 element 선택              | :last-child             |
| 몇 번째 자식                            | :nth-child(A)           |
| 뒤에서부터 몇 번째 자식                 | :nth-last-chile(A)      |
| span이 처음 등장하는 애                 | :first-of-type          |
| :nth-of-type(A)                         | even :　짝수, odd: 홀수 |
| 수열                                    | :nth-of-type(An+B)      |
| 자기자신과 같은 type의 sibling이 존재 x | :only-of-type           |
| type에서 가장 뒤                        | :last-of-type           |
| 아무것도 가지고 있지 않은 tag           | :not(X)                 |
| id가 fancy인거                          | :not(#fancy)            |

### 속성(중요도 순서)

### 타이포그라피:

#### font-size

단위(unit) - px, em, rem 상대적이냐 절대적이냐

px는 항상 정해져있고 나머지는 변경됨

요즘은 rem 사용

폰트크기를 조정할수 있는 사용자의 권리 지켜주기위해
px는 화면의 크기가 커져도 그대로

rem은 화면의 크기가 커지거나 사용자가 바꾸면 커지거나 작아질수있음

#### color지정

**color name** – 빨강 파랑 노랑처럼 색깔의 이름을 부르는 것 - {color:색이름}

**hex** – 16진수 - {color:#00FF00;}

**rgb** – 빨강 녹색 파랑을 합성한 숫자 - {color:rgb(0,0,0);}

### text-align 텍스트 정렬

```
<head>
<style>
p{
   text-align:center;  -> 가운데 정렬 left, right있음
   border:1px solid gray; -> 테두리는 회색 1px 두께
</style>
</head>
<body>
<p>
  텍스트
</p>
```

만약 텍스트가 길 때
text-align:justify; 하면 왼쪽 오른쪽 들쭉날쭉 하지않고 균일하게 된다
하지만 그게 더 못생겨 보일수도 있으니까 잘 보고 하기

### font

- font-family : 글꼴 지정

  font-family:폰트이름, 폰트이름, 폰트이름;
  첫 번째 폰트가 있으면 나오고 없으면 두 번째 폰트가 나옴.
  폰트 이름이 한 단어 이상일 때는 “”로 묶어주기
  뒤에 serif(장식이 있는 폰트), sans-serif(장식이 없는 폰트), cursive(흘림체), monospace(고정폭) 이것들중에 하나 붙여야 함.

- font-weight : 폰트의 두께 표현

- font-height : 글자의 행과 행 사이의 간격

  px사용하지말고 그냥 숫자, 상대적인 값 사용할 것

- font-property 이 모든 속성 축약

  순서 지켜주기 font: font-style font-variant font-weight font-size/line-height

  font-family|caption|icon|menu|message-box|small-caption|status-bar|initial|inherit;

  ```
    font-size: 5rem;
  font-family: arial, verdana, "Helvetica Neue", serif;
  font-weight: bold;
  line-height: 2;
  ```

  `font:bold 5rem/2 arial, verdana, "Helvetica Neue", serif;`

  위에 4줄이랑 밑에 1줄이랑 같은 말
  이렇게 위아래가 같을 때 **숏핸드(shorthand)** 라고 한다

### 웹폰트

사용자가 가지고 있지 않은 폰트는 깨질수 있는데 서버에서 웹 브라우저가 다운받아서 그 폰트를 사용할수 있게 하는 것

폰트의 용량 생각하기 한국어 폰트는 용량이 큼
구글 웹폰트 사이트

### 상속

#### 캐스케이딩

웹브라우저<사용자<저자

하나의 태그에 여러 css효과가 중첩되었을 때의 우선순위

style attribute>id selector>class selector>tag selector

!important - 어떤 것을 쓰든 가장 첫 번째 우선순위

#### inline vs block level

- **inline** - 자신과 자신을 둘러싸고있는 다른 텍스트나 다른 정보들과 하나의 같은 줄에 위치하는 형태의element

- **block** – 자기 혼자 한줄을 다 쓰는
  h1을 inline으로 바꾸는 법 - h1{display: inline}
  a를 block으로 바꾸는 법 – a{display: block}

### box model

글씨와 네모칸 사이에 거리 만들기 - **padding**:20px;

네모칸 끼리의 간격, 여백과 네모칸의 간격 – **margin**:60px;

보통 화면 전체를 사용하는데 그러고 싶지 않다면 width라는 것을 사용 높이는 거의 지정안함

그러나 inline값에서는 width랑 height값은 무시된다

### box-sizing

small인 값 하고싶으면 #small

border값이 다르고 안에 box의 값은 같을 때

border의 크기를 맞춰주기위해서 사용

### 마진겹침

마진 :다른 테두리들 사이의 간격

부모자식 둘다 마진 있는 경우에 마진겹침 생김

둘 중에 큰 쪽의 마진값 사용
