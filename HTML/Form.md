# ํผ Form
๐ [๊น๋ฒ๊ทธ์html์์ฌ๋ฐ๋ค](https://edu.goorm.io/lecture/20583/%25EA%25B9%2580%25EB%25B2%2584%25EA%25B7%25B8%25EC%259D%2598-html-css%25EB%258A%2594-%25EC%259E%25AC%25EB%25B0%258C%25EB%258B%25A4)

<br>

### ๊ธฐ๋ณธ๊ตฌ์กฐ 
```html
<form action="/" method=""></form>
```
<br>

* action="API์ฃผ์" : ์์ฑ์ด ์ด๋๋ก ๊ฐ๋์ง ์ ์ด 
* API(Application Programming Interface) : ์ด์์ฒด์ ์ ์์ฉํ๋ก๊ทธ๋จ ์ฌ์ด์ ํต์ ์ ์ฌ์ฉ๋๋ ์ธ์ด๋ ๋ฉ์ธ์ง ํ์
* method="GET / POST" : ์ด๋ค ์ ํ์ HTTP ๋ฉ์๋๋ฅผ ์ฌ์ฉํ ์ง ์ ์ด

<br>

### input
```html
<input type="text" placeholder="์ด๋ฆ์ ์๋ ฅํ์ธ์" minlength="5" maxlength="13" required disabled value="๊ฐ">
```
<br>

* ์ฌ์ฉ์์๊ฒ ๊ฐ์ ์๋ ฅ๋ฐ๊ณ  ํ๋์ ์ ๋ฌํ๋ ๊ฐ์ฅ ๊ธฐ๋ณธ์ ์ธ ํ๊ทธ
* ๋ซ๋ํ๊ทธ๊ฐ ๋ฐ๋ก ์์
* ์ฌ๋ฌ๊ฐ์ง์ type์ด ์์
    * text
    * password
    * url
    * email
    * number (max,min)
    * color 
    * file (accept="ํ์ผํ์") ...
* ํผ ์ ํจ์ฑ๊ฒ์ฌ
    * required ํ์๊ฐ
    * disabled ์ฌ์ฉ์๊ฐ ์ฌ์ฉํ  ์ ์๊ฒ ๋ง์๋๊ณ  ์ถ์ ๋
    * minlength ์ต์๊ธ์์
    * maxlength ์ต๋๊ธ์์ 

<br>

### label
```html
<label for="์ด๋ฆ">๋ผ๋ฒจ์ด๋ฆ</label>
<input id="์ด๋ฆ" type="text">
```
<br>

* ํผ ์์์ ์ด๋ฆ์ ๋ถ์ด๋ ํ๊ทธ
* input๊ณผ ํจ๊ป ์ฐ๊ฒฐํด์ ์ฌ์ฉ 
* input๊ณผ ์ฐ๊ฒฐํ๋ฉด ๋ผ๋ฒจ์ ๋๋ฅด๋ฉด ์ฐ๊ฒฐ๋ ์ธํ๊ฐ์ ํฌ์ปค์ฑ ๋จ

<br>

### name
* `<input name="">`
* ๋ชจ๋  input์๋ name์ ์จ์ค์ผ ํ๋ค. ์๋ฒ๋ก ์ ์ก๋๊ธฐ ๋๋ฌธ!
* input ๊ฐ์ ๋ฐ์ดํฐ๊ฐ ์๋ฒ๋ก ์ ์ก๋๋ ๊ฐ์ ์ง์นญ

<br>

### Radio
```html
<input type="radio" name="subscription" value="01" id="subscribed" />
<label for="subscribed">๊ตฌ๋์ค</label>

<input type="radio" name="subscription" value="02" id="unsubscribed" />
<label for="unsubscribed">๋ฏธ๊ตฌ๋</label>
```
<br>

* ์ฌ๋ฌ ํญ๋ชฉ ์ค ํ๋๋ง ์ฌ์ฉํ  ์ ์๋ ์ธํฐํ์ด์ค
* ๊ฐ์ name์ ์ฌ์ฉํด์ผ ํ ๊ทธ๋ฃน์ผ๋ก ์ธ์ํ๊ณ  ๋ ์ค ํ๋๋ฅผ ๊ณ ๋ฅผ ์ ์์
* name / value ๊ฐ์ ํ์๋ก ์๋ ฅ, ์๋ก ๋ค๋ฅธ๊ฐ์ผ๋ก ์๋ ฅํด์ค์ผ ํจ ๊ทธ๋์ผ ๊ฐ์๊ทธ๋ฃน(name)์ ๋ค๋ฅธ๊ฐ(value)์ ์ ํํ๋ค๋ ๊ฒ์ ์๋ฒ๋ก ์ ๋ฌ ๊ฐ๋ฅ

### Checkbox
```html
<input type="checkbox" name="skills" value="html" id="html" />
<label for="html">HTML</label>
<input type="checkbox" name="skills" value="css" id="css" />
<label for="css">CSS</label>
<input type="checkbox" name="skills" value="js" id="js" />
<label for="js">Javascript</label>
```
<br>

* ๋ค์ค ์ ํ ๊ฐ๋ฅ
* ํ๊ทธ๋ฃน์ผ๋ก ๋ฌถ๊ธฐ์ํด name์ ํ์๋ก ์๋ ฅํด์ค์ผ ํจ

<br>

### Select & Option
```html
<label for="skill">์คํฌ</label>
<select multiple name="skill" id="skill">
    <option value="html">HTML</option>
    <option value="css">CSS</option>
    <option value="js">Javascript</option>
</select>
```
<br>

* `select` ์์์๋ง name์ ์จ์ฃผ๋ฉด ์๋์ ์ผ๋ก ์์์์์ธ `option` ์ ๊ทธ๋ฃน์ผ๋ก ๋ฌถ์
* option์ ๊ฐ๊ฐ ๊ตฌ๋ถํด์ค ์ ์๋ value๋ฅผ ์๋ ฅ(์ ์ถํ์ ๋ ์๋ฒ๋ก ์ ์ก๋๋ ๊ฐ)
* multiple์ ์ถ๊ฐํด์ฃผ๊ณ  ctrl์ ๋๋ฅด๋ฉด ๋ค์ค ์ ํ ๊ฐ๋ฅ

<br>

### Textarea
```html
<label for="field">์๊ธฐ์๊ฐ:</label>
<textarea for="field" rows="40" cols="50" >์๊ธฐ์๊ฐ</textarea>
```
<br>

* ์ฌ๋ฌ ์ค์ ๊ฑธ์ณ์ ๋ง์์์ ๊ธ์ ๋ฐ์ ๋ ์ฌ์ฉ

<br>

### Button
```html
<button type="button">๋ฒํผ</button>
<button type="submit">์ ์ถํ๊ธฐ</button>
<button type="reset">๋ค์์ฐ๊ธฐ</button>
```

