# Box
๐ [๊น๋ฒ๊ทธ์css๋์ฌ๋ฐ๋ค](https://edu.goorm.io/lecture/20583/%25EA%25B9%2580%25EB%25B2%2584%25EA%25B7%25B8%25EC%259D%2598-html-css%25EB%258A%2594-%25EC%259E%25AC%25EB%25B0%258C%25EB%258B%25A4)

<br>

## Box Model
```css
.box {
    width: 500px;
    height: 300px;
    padding: 20px;
    border: 1px solid #000;
    margin: 30px
}
```
<br>

* ๋ด์ฉ๋ฌผ width + ์์ชฝ์ฌ๋ฐฑ padding + ํ๋๋ฆฌ border + ๋ฐ๊นฅ์ชฝ ์ฌ๋ฐฑ margin
* content์ **๊ฐ๋ก** width , **์ธ๋ก** height
* **์์ชฝ์ฌ๋ฐฑ**, ์ฆ content์ border ์ฌ์ด์ ๊ณต๊ฐ์ ๋ํ๋ด๋ **padding**
* **ํ๋๋ฆฌ**๋ฅผ ๋ํ๋ด๋ **border**
    * border: ๊ตต๊ธฐ ์คํ์ผ ์์ / border: none
* border-radius ํ๋๋ฆฌ ์ํ
* **๋ฐ๊นฅ์ฌ๋ฐฑ**, ์ฆ ์์์ ์์ ์ฌ์ด์ ๊ฐ๊ฒฉ์ ๋ํ๋ด๋ **margin**

<br>

### ์๊ธฐํ 
* ์ฝ๊ฒ ์๊ณ๋ฐฉํฅ์ด๋ผ๊ณ  ์๊ฐํ๋ฉด ๋๋ค
* top right bottom left
* top bottom, right left 
* top, right left, bottom

<br>

## Box Sizing 
```css
* {
    box-sizing : border-box;
    /* content-box(๊ธฐ๋ณธ๊ฐ) | border-box */
}
```

* ๋ณดํต ์ฒ์์์ํ  ๋ ์ ์ฒด์ border-box๋ฅผ ๊น๊ณ  ์์ํ๋ค.
* content-box๋ ์ ํ ํฌ๊ธฐ์์ ๋ํด์ง๋ ๊ฒ
* border-box๋ ์ ํํฌ๊ธฐ๋ด์์ ์ ํด๋ ๊ฒ 

<br>

## Box
* Box Type โก **display**

<br>

### block
* block โ ๊ธธ๋ง 
* ๋ค๋ฅธ ์์๋ค์ด ์์ ์ ์์ญ์ ์นจ๋ฒํ์ง ๋ชปํ๊ฒ ํ๋ ์์
* ๋ฐ๋ก width๋ฅผ ์ ์ธํ์ง ์์ ๊ฒฝ์ฐ, width = ๋ถ๋ชจ์ content-box์ 100%
* ๋ฐ๋ก width๋ฅผ ์ ์ธํ ๊ฒฝ์ฐ, ๋จ์๊ณต๊ฐ์ margin์ผ๋ก ์ฑ์ 
* ๋ฐ๋ก ๋ถ๋ชจ์ height๋ฅผ ์ ์ธํ์ง ์์ ๊ฒฝ์ฐ, ์์ ์์์ height์ ํฉ = ๋ถ๋ชจ์ height
* width, height, border, padding, margin ๋ชจ๋ ์ ์ฉ ๊ฐ๋ฅ
* margin = 0 auto โ ๋ธ๋ก์ ๊ฐ์ด๋ฐ ์์น ์ํค๋ ๊ฒ

<br>

### inline 
* inline โ ํ๋ฆ
* ์์ผ๋ก ํ๋ฅด๋ค๊ฐ ์๋ฆฌ๊ฐ ์์ผ๋ฉด ์ค๋ฐ๊ฟ ๋์ด ๋ค์์ค๋ก ํ๋ฆ
* block(๋ฉด,์์ญ) vs inline(์ ,ํ๋ฆ)
* width, height, padding-top, padding-bottom, margin-top, margin-bottom **์ฌ์ฉ๋ถ๊ฐ** โ ์ธ๋ผ์ธ์ ํ๋ฆ์ ๋ง๋ ์์๋ค ์ด๊ธฐ ๋๋ฌธ์ 

<br>

### inline-block
* inline ์ฒ๋ผ ํ๋ฅด๋ ๋์์ block ์ฒ๋ผ ์์ญ์ ์ก๊ณ  ์๋ ์์
* inline์์ ์ฌ์ฉํ์ง ๋ชปํ๋ ์์๋ค ๋ชจ๋ ์ฌ์ฉ ๊ฐ๋ฅ!
* ์ผ๋ ฌ๋ก ์ ๋ ฌ ๊ฐ๋ฅ, ๋ง์ง ํจ๋ฉ๊ฐ ์ง์  ๊ฐ๋ฅ 


