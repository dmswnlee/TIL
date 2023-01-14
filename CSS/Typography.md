# Typography
📌 [김버그의css는재밌다](https://edu.goorm.io/lecture/20583/%25EA%25B9%2580%25EB%25B2%2584%25EA%25B7%25B8%25EC%259D%2598-html-css%25EB%258A%2594-%25EC%259E%25AC%25EB%25B0%258C%25EB%258B%25A4)

<br>

```css
.text{
	font-size:20px;
	line-height:1.5;
	letter-spacing: -.03em;
	font-family:"Poppins",sans-serif;
	font-weight: 400;
	color:#fff;
	text-align:center;
	text-indent:20px;
}
```

<br>

### font-size
* px (절대단위 Absolute unit)
* em , rem (상대단위 Relative unit, 어떤값을 기준으로 하냐에 따라 달라짐)
* em = equal to capital M (실제로 적용된 폰트사이즈)
    * 만약 적용된 폰트사이즈가 24PX 이라면  1em = 24px, 1.5em = 36px
* rem = root em (html에 적용된 폰트사이즈)

<br>

### line-height 
* 행간(줄간격)
* 기본은 폰트크기
* px , **em** , rem
* em을 많이 사용한다, 보통 사용할때는 단위를 써주는게 맞지만 em은 생략하고 사용가능 ex) 1.5em → 1.5
* line-height가 어떤크기가 되든 글자는 줄간격의 가운데에 위치

<br>

### letter-spacing
* 자간
* px, **em**
* 폰트사이즈에 비례해서 몇퍼센트를 줄이는게 좋은지로 하는게 좋기 때문에 em을 사용, 이때 em은 단위를 꼭 써줘야 함 
* word-spacing 단어와단어사이 간격

<br>

### font-family
* 폰트(서체)
* serif (삐침이 있는 서체, 명조) , sans-serif (삐침이 없는 , 굵기가 일정한 서체,고딕)


<br>

### font-weight
* 폰트 굵기
* 100 ~ 900
* 400(Regular) , 700(Bold)를 가장 많이 씀

<br>

### color
* 폰트 컬러
* hex , rgb, rgba(a는 투명도)

<br>

### text-align
* 글자 가로정렬
* left | right | center |  justify (양쪽정렬)
* vertical-align 세로정렬 → top, middle, bottom(기본값)

<br>

### text-indent
* 글자 들여쓰기 
* 문단의 첫줄만, + 들여쓰기, - 내어쓰기

<br>

### text-transform
* 알파벳을 사용 시 적용
* none | capitalize(맨 앞자리 글자가 대문자) | uppercase(대문자) | lowercase(소문자)
* font-variant  : 소문자대문자 변경 
* small-caps : 소문자를 작은 대문자로 바꿀때사용

<br>

### text-decoration
* 텍스트의 줄을 끊는것과 관련된 속성
* none | underline(밑줄) | line-through(취소선) | overline(윗줄)

<br>

### font-style
* normal | italic(기울기) | oblique(거의 사용하지 않음,이탈릭과 비슷)

<br>

### 그외
* white-space : pre 공백, nowrap 줄바꿈안함

<br>

## web font
### 구글폰트 등 링크를 가져오는 경우
* link 태그를 이용하여 가져온 뒤 font-family를 복사해서 사용

<br>

### 다운받은 폰트를 가져오는 경우
```css
@font-face{
	font-family:"kimbug";
	font-style: normal;
	font-weight:400;
	src:url(폰트파일경로)
}
```
* 다운받은 폴더는 따로 폴더에 넣어두고 @font-face 사용 
* html에 import 하는법 link 넣어주기
* css에 import하는법 @import url(경로);

📌 [@font-face](https://css-tricks.com/snippets/css/using-font-face-in-css/)