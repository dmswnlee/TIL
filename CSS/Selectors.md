# Selectors
π [κΉλ²κ·Έμcssλμ¬λ°λ€](https://edu.goorm.io/lecture/20583/%25EA%25B9%2580%25EB%25B2%2584%25EA%25B7%25B8%25EC%259D%2598-html-css%25EB%258A%2594-%25EC%259E%25AC%25EB%25B0%258C%25EB%258B%25A4)

<br>

### μμ, ν΄λμ€, IDμ νμ (Type, Class & ID Selector)
```css
/* element μμ μ νμ , type νμ μ νμ : μ°μ μμ 1μ  */
h1{
	color:#fff;
}

/* class ν΄λμ€ μ νμ : μ°μ μμ 10μ  */
.box{
	background:#fff;
}

/* id μμ΄λ μ νμ : μ°μ μμ 100μ  */
#box{
	font-size:20px;
}
```

<br>

### μμ, μμ, νμ μ νμ (Child, Descendant & Sibling Combinators)
* νμμ νμ ex) `div.title p{color:red;}`
* μμμ νμ ex) `div.title > p{color:green;}3`
* μΈμ νμ μ νμ ex) `h1 + h2{color:blue}`
* νμ μ νμ  ex) `h1 ~ h2{background-color:yellow;}`

<br>

### κ΅¬μ‘°μ  κ°μ ν΄λμ€ μ νμ (Structural Pseudo-Classes)
* element : first-child μ²« λ²μ§Έ μμμ μ€μ μ μ©
* element : last-child λ§μ§λ§ μμμ μ€μ μ μ©
* element : nth-child(n) ν­λͺ©μ€μμ nλ²μ§Έ μμμ μ ν
* element :nth-of-type(n) μ νμ΄ κ°μ nλ²μ§Έ μ ν
* λ³΄ν΅ κ°μ νμμ μ€μ μ μ μ©ν΄μ€λλ `nth-of-type first-of-type` μ΄λ°μμ μμλ₯Ό μ°λκ² λ μ§κ΄μ μ΄κ³  μ¬μ©μ΄ μ©μ΄ν¨

<br>

### λμ  κ°μ ν΄λμ€ μ νμ(User Pseudo-classes)
User Action Pseudo-clsses : μ΄λ€ μνλ μ‘°κ±΄μ λΆν©νμλ νΉλ³ν ν¨κ³Όλ₯Ό μ£ΌκΈ°μν κ² 

* element:hover  λ§μ°μ€λ₯Ό μ¬λ €λ μν
* element:active λ§μ°μ€λ‘ ν΄λ¦­ν μν
* element:focus ν¬μ»€μ±λ μν
* element:link λ°©λ¬Έν μ μ΄ μλ λ§ν¬
* element:visited λ°©λ¬Έν μ μ΄ μλ λ§ν¬
    
