# 폼 Form
📌 [김버그의html은재밌다](https://edu.goorm.io/lecture/20583/%25EA%25B9%2580%25EB%25B2%2584%25EA%25B7%25B8%25EC%259D%2598-html-css%25EB%258A%2594-%25EC%259E%25AC%25EB%25B0%258C%25EB%258B%25A4)

<br>

### 기본구조 
```html
<form action="/" method=""></form>
```
<br>

* action="API주소" : 속성이 어디로 가는지 제어 
* API(Application Programming Interface) : 운영체제와 응용프로그램 사이의 통신에 사용되는 언어나 메세지 형식
* method="GET / POST" : 어떤 유형의 HTTP 메서드를 사용할지 제어

<br>

### input
```html
<input type="text" placeholder="이름을 입력하세요" minlength="5" maxlength="13" required disabled value="값">
```
<br>

* 사용자에게 값을 입력받고 필드에 전달하는 가장 기본적인 태그
* 닫는태그가 따로 없음
* 여러가지의 type이 있음
    * text
    * password
    * url
    * email
    * number (max,min)
    * color 
    * file (accept="파일형식") ...
* 폼 유효성검사
    * required 필수값
    * disabled 사용자가 사용할 수 없게 막아두고 싶을 때
    * minlength 최소글자수
    * maxlength 최대글자수 

<br>

### label
```html
<label for="이름">라벨이름</label>
<input id="이름" type="text">
```
<br>

* 폼 양식에 이름을 붙이는 태그
* input과 함께 연결해서 사용 
* input과 연결하면 라벨을 누르면 연결된 인풋값에 포커싱 됨

<br>

### name
* `<input name="">`
* 모든 input에는 name을 써줘야 한다. 서버로 전송되기 때문!
* input 값의 데이터가 서버로 전송되는 값을 지칭

<br>

### Radio
```html
<input type="radio" name="subscription" value="01" id="subscribed" />
<label for="subscribed">구독중</label>

<input type="radio" name="subscription" value="02" id="unsubscribed" />
<label for="unsubscribed">미구독</label>
```
<br>

* 여러 항목 중 하나만 사용할 수 있는 인터페이스
* 같은 name을 사용해야 한 그룹으로 인식하고 둘 중 하나를 고를 수 있음
* name / value 값을 필수로 입력, 서로 다른값으로 입력해줘야 함 그래야 같은그룹(name)에 다른값(value)을 선택했다는 것을 서버로 전달 가능

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

* 다중 선택 가능
* 한그룹으로 묶기위해 name을 필수로 입력해줘야 함

<br>

### Select & Option
```html
<label for="skill">스킬</label>
<select multiple name="skill" id="skill">
    <option value="html">HTML</option>
    <option value="css">CSS</option>
    <option value="js">Javascript</option>
</select>
```
<br>

* `select` 요소에만 name을 써주면 자동적으로 자식요소인 `option` 은 그룹으로 묶임
* option은 각각 구분해줄 수 있는 value를 입력(제출했을 떄 서버로 전송되는 값)
* multiple을 추가해주고 ctrl을 누르면 다중 선택 가능

<br>

### Textarea
```html
<label for="field">자기소개:</label>
<textarea for="field" rows="40" cols="50" >자기소개</textarea>
```
<br>

* 여러 줄에 걸쳐서 많은양의 글을 받을 떄 사용

<br>

### Button
```html
<button type="button">버튼</button>
<button type="submit">제출하기</button>
<button type="reset">다시쓰기</button>
```

