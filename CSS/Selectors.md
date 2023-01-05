# Selectors

### 요소, 클래스, ID선택자 (Type, Class & ID Selector)
```css
/* element 요소 선택자 , type 타입 선택자 : 우선순위 1점 */
h1{
	color:#fff;
}

/* class 클래스 선택자 : 우선순위 10점 */
.box{
	background:#fff;
}

/* id 아이디 선택자 : 우선순위 100점 */
#box{
	font-size:20px;
}
```

<br>

### 자식, 자손, 형제선택자 (Child, Descendant & Sibling Combinators)
* 하위선택자 ex) `div.title p{color:red;}`
* 자식선택자 ex) `div.title > p{color:green;}3`
* 인접형제선택자 ex) `h1 + h2{color:blue}`
* 형제선택자  ex) `h1 ~ h2{background-color:yellow;}`

<br>

### 구조적 가상 클래스 선택자 (Structural Pseudo-Classes)
* element : first-child 첫 번째 요소에 설정적용
* element : last-child 마지막 요소에 설정적용
* element : nth-child(n) 항목중에서 n번째 자식을 선택
* element :nth-of-type(n) 유형이 같은 n번째 선택
* 보통 같은 타입에 설정을 적용해줄때는 `nth-of-type first-of-type` 이런식의 요소를 쓰는게 더 직관적이고 사용이 용이함

<br>

### 동적 가상 클래스 선택자(User Pseudo-classes)
User Action Pseudo-clsses : 어떤 상태나 조건을 부합했을때 특별한 효과를 주기위한 것 

* element:hover  마우스를 올려둔 상태
* element:active 마우스로 클릭한 상태
* element:focus 포커싱된 상태
* element:link 방문한 적이 없는 링크
* element:visited 방문한 적이 있는 링크
    
