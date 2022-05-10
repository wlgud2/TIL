## HTML5
>[참조](https://webclub.tistory.com/491)

---

### HTML이란?

Hypertext Markup Language. **웹페이지**가 어떻게 **구조화**되어있는지 브라우저가 알 수 있도록 하는 마크업 언어

### HTML5?

HTML의 새로운 버전으로, 클라이언트와 서버간의 통신이 가능하며 **외부 플러그인(plug-ins)을 사용하지 않고도** 웹 서비스를 제공할 수 있도록 부가 기능이 추가된 것



### HTML5의 주요기능

`Device AccessDEVICE ACCESS` : 카메라, 동작센서 등의 H/W 기능을 웹에서 직접적으로 제어

`CONNECTIVITY(Web Socket)` : 웹 (클라이언트)에서 서버 측과 직접적인 양방향 통신 가능

`3D, GRAPHICS & EFFECTS` : 다양한 2차원 및 3차원 그래픽 기능을 지원

`Styling Effects(CSS3)` : 글씨체, 색상, 배경 등 다양한 스타일 및 이펙트 기능 제공

`MULTIMEDIA` : 비디오 및 오디오 기능을 자체적으로 지원

`OFFLINE & STORAGE` : 네트워크 미지원 환경에서도 웹 이용을 가능하게 함

`Geo-Location`: GPS없이도 단말기의 지리적인 위치 정보를 제공

`SEMANTICS` : 웹 자료에 의미를 부여하여 사용자 의도에 맞는 맞춤형 검색 제공



### Syntax(구문)

```html
<!doctype html>
<html lang="ko">
    <head>
        <meta charset="UTF-8">
        <title>HTML5 Document type</title>
    </head>
    <body>
        <!-- 콘텐츠 영역 -->
    </body>
</html>
```

1. DOCTYPE

   최상단에 `DOCTYPE`을 작성해야하며 개행문자(enter)도 들어가서는 안됨

   `DOCTYPE`은 *HTML*과 *XHTML* 두가지가 있다

2. ENCODING

   ###### 기존의 문서 타입에서 사용하던 Charset. 즉, encoding

  ```html
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
  ```

###### 		 HTML5의 Charset

```html
<meta charset="UTF-8">
```

3. 그래픽 언어의 사용

   수식기술언어 `MathML`, 그래픽언어 `SVG` 등을 사용할 수 있다

 ```html
 <!doctype html> 
 <html lang="ko">
     <head>
         <meta charset="UTF-8">
         <title>Document</title> 
     </head>
     <body>
         <div> 
             <svg> <circle r="50" cx="50" cy="50" fill="green"/> </svg>
         </div> 
     </body>
 </html>
 ```



### Language(언어)

###### 새로 추가된  Semantic Element

Header - 문서의 Header 를 나타낼 때 사용

Footer - 문서의 Footer 를 나타낼 때 사용

Nav - 문서내에 Navigation 요소가 있을 때 사용

Section - 문서의 영역을 구성하며, 문서 구조를 구성하는 H1~H6 와 함께 사용

Article - 뉴스기사나 블로그 article 과 같은 독립된 Contents 를 표시할 때 사용

Aside - 주요 컨텐츠 이외의 참고가 될 수 있는 컨텐츠를 구성할때 사용

Figure - 그림, 비디오와 같은 포함된 컨텐츠의 Caption 을 표시할때 사용

Figcaption - 캡션에 사용

<img src="JAVA%EC%99%80%20C%20%EC%96%B8%EC%96%B4%EC%9D%98%20%EC%B0%A8%EC%9D%B4.assets/22560D4A57CE635B0E.gif" alt="img" style="zoom:67%;float:left;" />

###### 기타 추가된 Element

Audio, Video - 멀티미디어 컨텐츠를 표시하는 데 사용

Embed - Plugin 컨텐츠를 표시할 때 사용

Mark - 별도로 표시한 문자를 표시하는데 사용

Progress - 작업 진행상황을 나타낼 때 사용

Meter - 측정값을 표시할 때 사용

Time - 날짜, 시간을 표시할 때 사용

Ruby, rt, rp - Ruby 언어를 나타낼 때 사용

Canvas - Bitmap Graphic을 표시할 때 사용

Command - 사용자가 호출할 수 있는 명령어를 표시하는데 사용

details - 사용자 요청에 따라 얻은 콘트롤이나 추가적인 정보를 표시하는데 사용

Datalist - List Attribute 와 함께 사용하여 ComboBox 를 만들때 사용

Keygen - 키쌍(Key pair)을 생성할 때 사용

Output - 스크립트 계산 결과 같은 실행결과를 표시하는데 사용



###### 새롭게 추가된 Attribute

data-* : 접두사 "data-" 를 가진 속성으로 추후 HTML 버전 충돌없이 사용자 태그로 이용하거나 추후 브라우져가 지원하게 되었을때 사용할 수 있다.

role, aria-* : 보조기능에 가리키는데 사용할 수 있다.

contenteditable : 편집가능한 Area 임을 나타낸다.

contextmenu : 작성자가 제작한 Context Menu 지정하는데 사용할 수 있다.

draggable : 새로운 Drag & Drop API 에서 사용할 수 있다.

hidden : element 가 아직 없거나 없을 때 사용

spellcheck : 맞춤법 검사기능을 제공할지 여부를 지정



######  변경된 Attribute

> 이 속성은 사용하지 않기를 권장하며 꼭 필요한 곳에서만 사용하도록 한다.

img 의 border : border 값은 0 일때만 사용하고 CSS 를 사용할 수 있다.

a 의 name : name 속성을 **id 속성으로 바꾸어** 쓸 수있다.

table 의 summary : 다른 대안을 정의하고 있다.

script 의 language : language 값은 JavaScript 에만 사용하고 type 속성과 함께 쓰지 않고 생략할 수있다.



###### 사라진 Element

- 다음 Element는 보여지는 것에만 사용되는 것이고 CSS로 처리 가능하기에 사라짐

  `basefont`, `big`, `center`, `font`, `strike`, `u` 등...

- 다음 Element는 Frame과 관련되고, 사용성과 접근성에 부정적이므로 제거

  `frame`, `frameset`, `noframes`

- 다음 Element는 자주 사용되지 않고 다른 Element로 대체할 수 있기에 제거

  `acronym`, `applet`, `isindex`, `dir`