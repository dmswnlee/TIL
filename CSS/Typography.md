# Typography
๐ [๊น๋ฒ๊ทธ์css๋์ฌ๋ฐ๋ค](https://edu.goorm.io/lecture/20583/%25EA%25B9%2580%25EB%25B2%2584%25EA%25B7%25B8%25EC%259D%2598-html-css%25EB%258A%2594-%25EC%259E%25AC%25EB%25B0%258C%25EB%258B%25A4)

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
* px (์ ๋๋จ์ Absolute unit)
* em , rem (์๋๋จ์ Relative unit, ์ด๋ค๊ฐ์ ๊ธฐ์ค์ผ๋ก ํ๋์ ๋ฐ๋ผ ๋ฌ๋ผ์ง)
* em = equal to capital M (์ค์ ๋ก ์ ์ฉ๋ ํฐํธ์ฌ์ด์ฆ)
    * ๋ง์ฝ ์ ์ฉ๋ ํฐํธ์ฌ์ด์ฆ๊ฐ 24PX ์ด๋ผ๋ฉด  1em = 24px, 1.5em = 36px
* rem = root em (html์ ์ ์ฉ๋ ํฐํธ์ฌ์ด์ฆ)

<br>

### line-height 
* ํ๊ฐ(์ค๊ฐ๊ฒฉ)
* ๊ธฐ๋ณธ์ ํฐํธํฌ๊ธฐ
* px , **em** , rem
* em์ ๋ง์ด ์ฌ์ฉํ๋ค, ๋ณดํต ์ฌ์ฉํ ๋๋ ๋จ์๋ฅผ ์จ์ฃผ๋๊ฒ ๋ง์ง๋ง em์ ์๋ตํ๊ณ  ์ฌ์ฉ๊ฐ๋ฅ ex) 1.5em โ 1.5
* line-height๊ฐ ์ด๋คํฌ๊ธฐ๊ฐ ๋๋  ๊ธ์๋ ์ค๊ฐ๊ฒฉ์ ๊ฐ์ด๋ฐ์ ์์น

<br>

### letter-spacing
* ์๊ฐ
* px, **em**
* ํฐํธ์ฌ์ด์ฆ์ ๋น๋กํด์ ๋ชํผ์ผํธ๋ฅผ ์ค์ด๋๊ฒ ์ข์์ง๋ก ํ๋๊ฒ ์ข๊ธฐ ๋๋ฌธ์ em์ ์ฌ์ฉ, ์ด๋ em์ ๋จ์๋ฅผ ๊ผญ ์จ์ค์ผ ํจ 
* word-spacing ๋จ์ด์๋จ์ด์ฌ์ด ๊ฐ๊ฒฉ

<br>

### font-family
* ํฐํธ(์์ฒด)
* serif (์์นจ์ด ์๋ ์์ฒด, ๋ช์กฐ) , sans-serif (์์นจ์ด ์๋ , ๊ตต๊ธฐ๊ฐ ์ผ์ ํ ์์ฒด,๊ณ ๋)


<br>

### font-weight
* ํฐํธ ๊ตต๊ธฐ
* 100 ~ 900
* 400(Regular) , 700(Bold)๋ฅผ ๊ฐ์ฅ ๋ง์ด ์

<br>

### color
* ํฐํธ ์ปฌ๋ฌ
* hex , rgb, rgba(a๋ ํฌ๋ช๋)

<br>

### text-align
* ๊ธ์ ๊ฐ๋ก์ ๋ ฌ
* left | right | center |  justify (์์ชฝ์ ๋ ฌ)
* vertical-align ์ธ๋ก์ ๋ ฌ โ top, middle, bottom(๊ธฐ๋ณธ๊ฐ)

<br>

### text-indent
* ๊ธ์ ๋ค์ฌ์ฐ๊ธฐ 
* ๋ฌธ๋จ์ ์ฒซ์ค๋ง, + ๋ค์ฌ์ฐ๊ธฐ, - ๋ด์ด์ฐ๊ธฐ

<br>

### text-transform
* ์ํ๋ฒณ์ ์ฌ์ฉ ์ ์ ์ฉ
* none | capitalize(๋งจ ์์๋ฆฌ ๊ธ์๊ฐ ๋๋ฌธ์) | uppercase(๋๋ฌธ์) | lowercase(์๋ฌธ์)
* font-variant  : ์๋ฌธ์๋๋ฌธ์ ๋ณ๊ฒฝ 
* small-caps : ์๋ฌธ์๋ฅผ ์์ ๋๋ฌธ์๋ก ๋ฐ๊ฟ๋์ฌ์ฉ

<br>

### text-decoration
* ํ์คํธ์ ์ค์ ๋๋๊ฒ๊ณผ ๊ด๋ จ๋ ์์ฑ
* none | underline(๋ฐ์ค) | line-through(์ทจ์์ ) | overline(์์ค)

<br>

### font-style
* normal | italic(๊ธฐ์ธ๊ธฐ) | oblique(๊ฑฐ์ ์ฌ์ฉํ์ง ์์,์ดํ๋ฆญ๊ณผ ๋น์ท)

<br>

### ๊ทธ์ธ
* white-space : pre ๊ณต๋ฐฑ, nowrap ์ค๋ฐ๊ฟ์ํจ

<br>

## web font
### ๊ตฌ๊ธํฐํธ ๋ฑ ๋งํฌ๋ฅผ ๊ฐ์ ธ์ค๋ ๊ฒฝ์ฐ
* link ํ๊ทธ๋ฅผ ์ด์ฉํ์ฌ ๊ฐ์ ธ์จ ๋ค font-family๋ฅผ ๋ณต์ฌํด์ ์ฌ์ฉ

<br>

### ๋ค์ด๋ฐ์ ํฐํธ๋ฅผ ๊ฐ์ ธ์ค๋ ๊ฒฝ์ฐ
```css
@font-face{
	font-family:"kimbug";
	font-style: normal;
	font-weight:400;
	src:url(ํฐํธํ์ผ๊ฒฝ๋ก)
}
```
* ๋ค์ด๋ฐ์ ํด๋๋ ๋ฐ๋ก ํด๋์ ๋ฃ์ด๋๊ณ  @font-face ์ฌ์ฉ 
* html์ import ํ๋๋ฒ link ๋ฃ์ด์ฃผ๊ธฐ
* css์ importํ๋๋ฒ @import url(๊ฒฝ๋ก);

๐ [@font-face](https://css-tricks.com/snippets/css/using-font-face-in-css/)