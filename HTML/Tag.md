📌 [tag](http://www.tcpschool.com/html-tags/intro)

📌 [김버그의html은재밌다](https://edu.goorm.io/lecture/20583/%25EA%25B9%2580%25EB%25B2%2584%25EA%25B7%25B8%25EC%259D%2598-html-css%25EB%258A%2594-%25EC%259E%25AC%25EB%25B0%258C%25EB%258B%25A4)

<br>

## 태그(Tag)?
* 꺽쇠에서 시작해서 꺽쇠에서 끝나는 <태그>
* 속성(attribute)을 통해 추가적인 정보를 제공 
* 다양한 태그와 웹 표준에 맞는 올바른 사용법을 익힌다 

<br>

### **제목과 문단**

<br>

```html
<h1>제목</h1>
```
* 머리말, 제목(headings)
* `<h1></h1> ~ <h6></h6>`
* `<h1>` 태그는 페이지 당 하나만 사용가능
* `<h1>` 이 없다면 `<h2>` 는 사용할 수 없음

<br>

```html
<p>문단</p>
```
* 단락, 문단(paragraph)
* 블록레벨요소

___

<br>

### **강조(Emphasis)**

<br>

```html
<em>약한강조</em>
<strong>강한강조</strong>
```

<br>

* 보여지는 효과는 css로 조절할 수 있음 중요한 건 브라우저에 중요한 문단인지 아닌지 전달할 수 있는것!

___

<br>

### **링크(Anchor)**

<br>

```html
<a href="주소">링크</a>
```

<br>

* 하이퍼링크를 만드는데 사용하는 요소 
* 현 위치에서 다른 위치로 이동할 때 사용
* href(hypertext reference) 코딩에서 주소값이라는 뜻을 가짐
* 인라인 요소 
* href 주소값 표기방법
    * URL 그대로 붙여넣기
    * 페이지 내 이동 (해당 페이지부분에 id값을 href부분에 입력) 
    * 메일주소 (`mailto:메일주소`)
    * 전화걸기, 모바일 사용시 전화번호 누르면 바로 전화 걸수있게 이동 (`tel:전화번호`)
    * `target="_blank"` 새탭으로 열어서 이동
___

<br>

### **이미지(Image)**

<br>

```html
<img src="이미지경로, 이미지 주소" alt="이미지 설명">
```

<br>

* src(source)
* alt(alternative text) : 대체텍스트 간혹 이미지가 안나올때 어떤 이미지가 있는지 알려주는 속성으로 스크린리더에서 읽을 수 있게하는 것, **웹접근성**에서 매우 중요

___

<br>

### **목록(List)**

<br>

```html
<ul>
    <li>항목1</li>
    <li>항목2</li>
</ul>
```

<br>

* ol (ordered list) : 순서가 있는 목록
* ul (unordered list) : 순서가 없는 목록
* li (list item) : 목록 아이템, ol, ul 하위요소
* 목록안에 목록이 필요하다면 중첩해서 사용할 수 있음
* **ul, ol 하위요소는 무조건 li만 가능** (li를 먼저쓰고 다음에 쓰는건 가능)

<br>

### **정의목록(Description List)**

<br>

```html
<dl>
    <dt>
        <dfn>학습</dfn>
    </dt>
    <dd>
        배워서 익히는 일
    </dd>
    <dd>
        심리적, 행동적 경험을 쌓음으로써 행동의 양태가 변화, 발전하는일 
    </dd>
</dl>
```

<br>

* 많이 쓰이는가? 유용하게 사용할 수 있음!
* 용어를 정의할 때 사용
* key-value로 정보를 제공할 때 (예를들어 이름:이영희, 직업:개발자)
* dl (description list)
* dt (description term) key에 해당
* dd (description data)
* `dt`를 해줬다면 `dd` 그에대한 설명을 꼭 해줘야함
* dl의 자식요소는 오직 `div, dt, dd`만 가능하다.

<br>

___

<br>

### **인용(Quotations)**

<br>

```html
<blockquote>인용 내용</blockquote>
<cite>인용출처</cite>

<blockquote cite="인용출처주소">인용 내용</blockquote>
<cite>인용출처</cite>

<q>문단안에 들어가는 인용구</q>

```

<br>

* 출처는 cite로 감싸고 정확한 출처 URl을 가지고 있다면 출처 주소를 넣어주면됨!

<br>

### **기타 Etc**

<br>

```html
<hr> 구분선
<br> 줄바꿈
<sup>윗첨자</sup>
<sub>아랫첨자</sub>
<abbr title="풀네임">약어,약자</abbr>
<address>연락처</address>
<pre>
    내가 작성한
    내용 그대로 출력
</pre>
```

<br>