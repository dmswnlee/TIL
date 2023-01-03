# HTML 기초

📌 [MDN](https://developer.mozilla.org/en-US/)
<br>
📌 [tag](http://www.tcpschool.com/html-tags/intro)

<br>

## HTML 이란?
* HTML (Hypertext Markup Language) 
* 웹페이지 문서에 마크업 하기 위한 언어 또는 구문

<br>

## HTML 구성
### Doctype & Document & Structure
```html
<!DOCTYPE hmlt> 
--> 브라우저야 이제 HTML5를 쓸거야 라고 선언하는것 
<html>
	<head>
	<!-- 웹문서에 관한 메타 데이터 -->
	</head>
	<body>
	<!-- 웹문서에 들어갈 내용 -->
	</body>
</html>
```
Document Type Declaration

= DTD 선언

= 문서 형식 선언

<br>

### Title
```html
<title>문서의 대제목</title> 
```
* 검색 최적화에 매우중요 
* title 잘 쓰는 방법
    * 키워드 단순 나열은 비추
    * 페이지마다 그에 맞게 변경
    * 무엇에 관한 내용인지 센스있게!

<br>

### Link
```html
<link rel="stylesheet" href="./styles.css">
```
* CSS 스타일시트를 첨부하는 태그

<br>

### Script
```html
<script src="경로"></script>
```
* CSS 처럼 head 안에 써도 되지만 랜더 되는시간을 생각해 body안에 사용하는 경우가 많다 

