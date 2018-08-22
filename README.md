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

1. url연결 태그`<a>`
```html
<a href="http://google.com">Google</a>
```
- href : 링크이름과 연결되어 있는 리소스의 주소
- title : 연결되어 있는 리소스에 대한 설명, 롤오버 했을 때 툴팁으로 표시
- target : 문서가 로드될 대상으로 아래의 속성값들이 있다.
    - _self : 현재의 문서가 로드된 프래임, 현재문서 사라짐
    - _blank : 새로운 창(탭)을 띄우고 거기에 문서를 로드
    - _parent : 현재 문서가 frame나 iframe에 로드된 경우 현재 문서를 로드한프래임에 문서로를 로드
    - 프래임의 이름

2. iframe태그 `<iframe>`
```html
    <iframe id="sample" src="http://w3c.org" width="100%" height="400" sandbox></iframe>
```
- 외부문서를 자신의 문서에 삽입하는 태그이며 `src`속성에 해당 문서 주소를 넣는다.
- `width`와 `height`등으로 크기를 조절할 수 있으며 `sandbox`속성을 사용하면 비신뢰적인 문서에 대해서 보안성이 생긴다.

3. 문단,줄바꿈,띄어쓰기
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