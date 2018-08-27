# HTML-Practice
## HTML이란?
웹페이지를 만들기 위한 언어로 웹브라우저 위에서 동작하는 언어이다.


**HT** - HyperText, 문서와 문서가 링크로 연결되어 있다.


**M** - Markup, 태그로 이루어져 있다.


**L** - Language

## 기본구성
```html
<!DOCTYPE html>  --문서형태 선언(문서의 형태에 따라 다르다.)
<html>
    <head>  --문서의 제목 또는 메타데이터, 문자코드값 등을 다룬다.

    </head>
    <body>   --문서의 내용을 담는다.

    </body>
</html>
```

## 태그란?(Tag)
정보를 정의하는 형식

- **<태그명 속성명 1="속성값" 속성명2="속성값2>컨텐트</태그명>**

- **`<br />` , `<input type="button" value="버튼" />`같이 닽히는 태그가 없는 태그도 존재한다.**

### 기본태그
**1. HEAD태그**
- <head>태그는 문서를 설명하는 태그들이 위치하는 태그다. <body>태그의 정보를 설명하는 메타 정보라고 할 수 있다.

**2. BODY태그**
- <body>태그는 웹페이지가 담아내려는 정보 그 자체라고 생각하면 된다.

**3. meta태그**
```html
    <meta name="" content="">
    <meta name="description" content="생활코딩은 일반인에게 프로그래밍을 알려주는 수업">
    <meta name="keywords" content="HTML,HEAD,META">
    <meta http-equiv="Content-Type" content="text/html;charset=utf-8">  --현 문서가 사용하는 문자에 대한 정보
```
- 문서에 대한 정보를 기술하는 태그이다.
- name : 메타데이터의 이름이다.
- content : 메타데이터의 값이다.
- http-equiv : meta요소에서 정의된 명령을 먼저 실행한 후에 페이지를 로딩한다. 이를 `프라그마 디렉티브`라고 한다.
    - **속성 값**
        - content-language : 전처리될 기본 언어를 지정할 수 있다. 선언하지 않는 경우 기본언어가 존재하지 않는 것으로 간주.
        ```html
        <meta http-equiv="content-language" content="ko" />
        ```
        - content-type : 문자 인코딩을 선언한다. `content`속성의 문자열 `text/html`와 아스키, 대문자 구별없이 일치해야만 한다. 그 뒤 리터럴 문자열 `charset`이 따라와야하며 문자인코딩에 해당하는 이름이 있어야 한다.
        XML에서는 사용할 수 없다.
        ```html
        <meta http-equiv="Content-Type" content="text/html; charset=euc-kr">
        ```
        - default-style : 대체 스타일시트 집합의 이름을 설정한다.
        ```html
         <meta http-equiv="content-style-type" content="text/css">
         ```
        - refresh : 리다이렉트처럼 페이지를 지정한 시간 이후에 새로고침을 할 수 있다. 값은 유효한 정수만 되며 초단위로 나타낸다.
        ```html
        <meta http-equiv="refresh" content="10, www.naver.com">
        ```
        - Content-Script-Type : 스크립트 형식을 지정한다. 형식에는 text/javascript 와 VBScript가 있다.
        ```html
        <meta http-equiv="Content-Script-Type" content="text/javascript">
        ```
        - Content-Style-Type : 스타일시트 형식을 지정해준다.
        ```html
            <meta http-equiv="Content-Style-Type" content="text/css">
        ```
        - Page-Enter/Exit : 속성값이 Page-Enter, Page-Exit는 웹문서를 들어오거나 나갈 때 한쪽 모서리 부터 서서히 드러나거나 사라지는 효과를 줍니다.
        ```html
        <meta http-equiv="Page-Enter" content="RevealTrans(Duration=10, Transition=50)">
        <meta http-equiv="Page-Exit" content="RevealTrans(Duration=10, Transition=50)">
        ```

**4. url연결 태그`<a>`**
```html
<a href="http://google.com" title="Google">Google</a>
```
- href : 링크이름과 연결되어 있는 리소스의 주소
- title : 연결되어 있는 리소스에 대한 설명, 롤오버 했을 때 툴팁으로 표시. 반드시 표기하여야 한다.
- target : 문서가 로드될 대상으로 아래의 속성값들이 있다.
    - _self : 현재의 문서가 로드된 프래임, 현재문서 사라짐
    - _blank : 새로운 창(탭)을 띄우고 거기에 문서를 로드
    - _parent : 현재 문서가 frame나 iframe에 로드된 경우 현재 문서를 로드한프래임에 문서로를 로드
    - 프래임의 이름

**5. iframe태그 `<iframe>`**
```html
    <iframe id="sample" src="http://w3c.org" width="100%" height="400" sandbox></iframe>
```
- 외부문서를 자신의 문서에 삽입하는 태그이며 `src`속성에 해당 문서 주소를 넣는다.
- `width`와 `height`등으로 크기를 조절할 수 있으며 `sandbox`속성을 사용하면 비신뢰적인 문서에 대해서 보안성이 생긴다.
- scrolling : 아이프래임 안에서 스크롤링을 허용할것인지를 지정
    + auto : 스크롤이 필요한 경우만 스크롤 바 노출(기본 값)
    + yes : 스크롤링 허용. 필요없는 경우에도 노출
    + no : 스크롤링 비허용

**6. 문단,줄바꿈,띄어쓰기**
```html
    문단
    <p></P>

    줄바꿈
    <br />

    띄어쓰기
    &nbsp;
    spacebar  --한칸만 허용
```
- 줄바꿈은 엔드태그가 없으며 Enter키로는 불가능하다.
- 띄어쓰기는 한칸만 띄우는것은 spacebar가 가능하지만 그이상띄어쓰기는 불가능하다.

**7. 이미지 삽입<img>**
```html
    <img src="" alt="" width="" height="" longdesc=""/>
```
- src : 이미지가 위치하는 URL
- alt : 대체텍스트(altemative) 이미지를 로딩할 수 없는 경우 대체되어 텍스트로 나타난다.
        시각장애인을 위한 장치와 검색엔진에서도 사용된다.
- width, height : 이미지 크기를 정의한다.(width를 정해놓으면 height는 기재하지않아도 자동으로 비율에 맞게 조정된다.)
- longdesc : 이미지와 관련된 링크를 적는다.

**8. 목록(ul>li, ol>li)**
```html
<ol>
    <li></li>
</ol>

<ul>
    <li></li>
</ul>
```
- ol : 순서가 있는 리스트 (태그 속 <li>(list item)에 순서대로 번호가 생성된다.)
- ul : 순서가 없는 리스트 (태그 속 <li>(list item)에 순서대로 모형이 생성된다.)

**9. 이스케이핑**
HTML 코드 등 브라우저에 의해서 해석되는 약속된 문자들을 브라우저에 해석되지 않고 표기할 수 있게 하는 언어들

- &amp;amp; → & (ampersand, U+0026), &amp;nbsp;<br />
- &amp;lt; → < (less-than sign, U+003C)<br />
- &amp;gt; → > (greater-than sign, U+003E)<br />
- &amp;quot; → ” (quotation mark, U+0022)<br />
- &amp;apos; → ‘ (apostrophe, U+0027)<br />

**10. Form태그**
폼이란 사용자의 데이터를 서버에 전송하는 방법이다. 일반적으로 아래와 같은 작업을 하기 위해서는 폼을 이용한다.

- 로그인을 위해서 아이디/비밀번호를 입력할 때
- 회원가입을 하기 위해서 개인정보를 입력할 때
- 블로그나 게시판에 글을 작성하거나, 파일을 전송할 때

```html
<form action="" method="">
    텍스트 필드, 라디오 버튼, 체크 박스와 같은 컨트롤을 생성하는 태그
</form>
```
- action : 사용자가 입력한 데이터를 전송할 서버의 URL
- method : 사용자가 입력한 데이터를 전송하는 방법
    - get 
        - action에 입력한 URL에 파라미터의 형태로 전송
        - 전송할 수 있는 정보의 길이가 제한되어 있다.
        - 퍼머링크로 사용될 수 있다.
    - post 
        - header의 body에 포함해서 전송
        - URL 상에 전달한 정보가 표시되지 않는다.
        - GET에 비해서 보안상 약간의 우위에 있다.(사실상 동일하다.)
        - 전송할 수 있는 데이터의 길이 제한이 없다.
        - 퍼머링크로 사용될 수 없다.
        - 서버 쪽에 어떤 작업(데이터의 기록,삭제,수정 등)을 명령할 때 사용한다.

**11. input태그**
사용자로부터 텍스트를 입력받는다.
```html
<input type="text" name="값의 이름" value="값" disabled="disabled" readonly="readonly">
```
- type : text를 사용해야 텍스트 필드가 된다.(text, password, submit, hidden, radio 등이 있다.)
    - text : 일반적인 텍스트를 적을 때 사용한다. 긴문장을 사용할 때는 `<textarea>`를 사용한다.
    - password : 비밀번호를 입력하며 보여지지 않고 숨겨진다.
    - submit : 버튼형식으로 나오며 눌렀을 시 `<form>`에 지정된 url로 정보가 전송된다.
    - hidden : 사용자가 입력하지 못하며 화면에 표시도 되지않고 `submit`버튼을 눌렀을 때 지정된 정보가 전송된다.
    보통, 전 페이지의 입력 여부 등 다음페이지가 전페이지의 상황을 알아야 할 때 사용한다.
    - radio : 라디오 버튼이 생성된다.
    - checkbox : 체크박스목록을 생성한다.
    - file : 파일을 첨부하여 전송할 수 있다.
        ```html
            <form action="url" method="POST" enctype="multipart/form-data">
                <input type="file" name="imgfile">
                <input type="submit">
            </form>
        ```
- name : 입력한 데이터의 이름
- value : 데이터의 값, 입력한 데이터의 기본 값으로 이 값이 기본적으로 텍스트 필드에 표시된다.
- disabled : 텍스트 필드가 불능 상태가 되며 서버로 전송해도 이 속성이 설정된 컨트롤의 데이터는 서버로 전송되지 않는다.
- readonly : 텍스트 필드에 값이 입력되지 않는다. 서버로는 데이터가 전송된다.

### 서버와 클라이언트

> 폼을 이해하기 위해서는 우선 서버와 클라이언트라는 개념을 이해해야 한다. 서버는 정보를 제공하는 쪽이고, 클라이언트는 정보를 제공 받는 쪽을 의미한다. 웹브라우저의 주소창에 생활코딩의 홈페이지인 http://opentutorials.org를 입력하면 웹브라우저는 opentutorials.org에 해당하는 컴퓨터에게 생활코딩 컨텐츠를 요청한다. 이 맥락에서 웹브라우저는 정보를 요청하는 쪽 다시 말해서 제공 받는 쪽이기 때문에 클라이언트가 되고, opentutorials.org의 컨텐츠를 제공하는 컴퓨터는 정보를 제공하기 때문에 서버가 된다.

<img src="https://s3-ap-northeast-1.amazonaws.com/opentutorialsfile/module/2/1043.png" align="center" hspace="300" vspace="100">

### URL
URL(Uniform Resource Locator)이란 웹페이지, 이미지, 동영상과 같은 정보가 위치하는 유니크한 위치 정보

부분 | 명칭 | 설명
:---:|:---:|:---:
http:// | scheme | 통신에 사용되는 방식, 프로토콜
codingeverybody.com | hosts | 자원이 위치하고 있는 웹서버의 이름, 도메인이나 IP가 사용된다.
|/codingeverybody_html_tutorial/url_72/example2.html | url-path | 루트 디렉토리부터 자원이 위치한 장소까지의 디렉토리와 파일명|
?mode=view | query | 웹서버에 넘기는 추가적인 질문
#root | bookmark | 하이퍼링크를 클릭했을 때 특정 위치로 이동하기 위해서 사용

### 경로
- 상대경로 : 문서를 기준으로 한 다른 리소스들의 위치정보
- 절대경로 : 문서의 위치를 가르키는 도메인을 포함한 전체 위치정보

<table>
            <tr>
                <th>구분</th><th>기호</th><th>설명</th><th>코드 예시</th>
            </tr>
            <tr>
                <td rowspan="3">상대경로</td><td>../</td><td>부모 디렉토리</td><td>&lt;img src="../image/logo.png"/&gt;</td>
            </tr>
            <tr>
                <td>./</td><td>현재 디렉토리</td><td>&lt;img src="./image/logo.png"&gt;</td>
            </tr>
            <tr>
                <td>없음</td><td>현재 디렉토리 기호는 생략할 수 있다.</td><td>&lt;img src="image/logo.png"&gt;</td>
            </tr>
            <tr>
                <td rowspan="2">절대경로</td><td>/</td><td>루트(root)디렉토리</td><td>&lt;img src="/codingeverybody_html_tutorial/url_72/image/logo.png"&gt;</td>
            </tr>
            <tr>
                <td>URL</td><td>URL을 사용</td><td>&lt;img src="https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png"&gt;</td>
            </tr>
</table>

### 검색엔진 최적화(SEO)
검색엔진에 잘 노출될 수 있도록 하는 활동

[검색엔진 최적화 이유](https://support.google.com/webmasters/answer/35291?hl=ko)
