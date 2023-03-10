# DOM(Document Object Model)
π λͺ¨λμλ°μ€ν¬λ¦½νΈ Deep dive 

<br>

- λΈλΌμ°μ μ λ λλ§ μμ§μ HTML λ¬Έμλ₯Ό νμ±νμ¬ λΈλΌμ°μ κ° μ΄ν΄ν  μ μλ μλ£κ΅¬μ‘°μΈ DOMμ μμ±νλ€.
- DOMμ HTML λ¬Έμμ κ³μΈ΅μ  κ΅¬μ‘°μ μ λ³΄λ₯Ό νννλ©° μ΄λ₯Ό μ μ΄ν μ μλ API, μ¦ νλ‘νΌν°μ λ©μλλ₯Ό μ κ³΅νλ νΈλ¦¬ μλ£κ΅¬μ‘°λ€.

<br>

## λΈλ

**HTML μμμ λΈλ κ°μ²΄**

- HTML μμλ λ λλ§ μμ§μ μν΄ νμ±λμ΄ DOMμ κ΅¬μ±νλ μμ λΈλ κ°μ²΄λ‘ λ³ννλ€.
- μ΄λ HTML μμμ μ΄νΈλ¦¬λ·°νΈλ μ΄νΈλ¦¬λ·°νΈ λΈλλ‘, νμ€νΈλ νμ€νΈ λΈλλ‘ λ³νλλ€.
- HTML μμκ°μλ μ€μ²©κ΄κ³μ μν΄ κ³μΈ΅μ μΈ λΆμκ΄κ³κ° νμ±λλ€.
- μ΄λ° λΆμκ΄κ³λ₯Ό λ°μνμ¬ HTML μμλ₯Ό κ°μ²΄νν λͺ¨λ  λΈλ κ°μ²΄λ€μ **νΈλ¦¬ μλ£κ΅¬μ‘°**λ‘ κ΅¬μ±νλ€.
    - νΈλ¦¬ μλ£κ΅¬μ‘°λ λΈλλ€μ κ³μΈ΅κ΅¬μ‘°λ‘ μ΄λ€μ§λ€.
    - λΆλͺ¨λλμ μμλΈλλ‘ κ΅¬μ±λμ΄ λΈλκ°μ κ³μΈ΅μ κ΅¬μ‘°(λΆμ, νμ  κ΄κ³)λ₯Ό νννλ λΉμ ν μλ£κ΅¬μ‘°λ₯Ό λ§νλ€.
    - νλμ μ΅μμ λΈλμμ μμνλ€.
    - λ£¨νΈ λΈλ(root node) λΌκ³  λΆλ¦¬λ μ΅μμ λΈλλ 0κ° μ΄μμ μμλΈλλ κ°λλ€
    - μμ λΈλκ° μλ λΈλλ₯Ό λ¦¬νλΈλ(leaf node) λΌκ³  νλ€.
- λΈλ κ°μ²΄λ€λ‘ κ΅¬μ±λ νΈλ¦¬ μλ£μ£Όκ³ λ₯Ό DOM μ΄λΌ νλ€. (DOM νΈλ¦¬)

<br>

**λΈλ κ°μ²΄μ νμ**

- λΈλ κ°μ²΄λ μ’λ₯κ° μκ³  μμ κ΅¬μ‘°λ₯Ό κ°λλ€.
- λΈλ κ°μ²΄λ μ΄ 12κ°μ μ’λ₯(λΈλνμ)κ° μκ³  κ·Έ μ€ μ€μν λΈλνμμ 4κ°μ§ μ΄λ€.

<br>

λ¬ΈμλΈλ(document node)

- DOM νΈλ¦¬μ μ΅μμμ μ‘΄μ¬νλ λ£¨νΈ λΈλλ‘μ document κ°μ²΄λ₯Ό κ°λ¦¬ν¨λ€.
- λΈλΌμ°μ κ° λ λλ§ν html λ¬Έμ μ μ²΄λ₯Ό κ°λ¦¬ν€λ κ°μ²΄λ‘μ μ μ­ κ°μ²΄ windowμ document νλ‘νΌν°μ λ°μΈλ©λμ΄ μλ€.
- λ¬ΈμλΈλ, μ¦ document κ°μ²΄λ DOM νΈλ¦¬μ λ£¨νΈ λΈλμ΄λ―λ‘ DOM νΈλ¦¬μ λΈλλ€μ μ κ·ΌνκΈ° μν μ§μμ  μ­ν μ νλ€.
- μμ, μ΄νΈλ¦¬λ·°νΈ, νμ€νΈ λΈλμ μ κ·Όνλ €λ©΄ λ¬Έμ λΈλλ₯Ό ν΅ν΄μΌ νλ€.

<br>

μμλΈλ(element node) 

- μμ λΈλλ HTML μμλ₯Ό κ°λ¦¬ν€λ κ°μ²΄
- μμκ°μ μ€μ²©μ μν΄ λΆμκ΄κ³λ₯Ό κ°μ§λ©° μ λ³΄λ₯Ό κ΅¬μ‘°ννλ€.
- λ¬Έμμ κ΅¬μ‘°

<br>

μ΄νΈλ¦¬λ·°νΈ λΈλ(attribute node) 

- μ΄νΈλ¦¬λ·°νΈ λΈλλ HTML μμμ μ΄νΈλ¦¬λ·°νΈλ₯Ό κ°λ¦¬ν€λ κ°μ²΄
- μμλΈλμ μ°κ²°λμ΄ μλ€.
- λΆλͺ¨λΈλκ° μμ΄ μμμ νμ  λΈλλ μλλ€.
- μ΄νΈλ¦¬λ·°νΈ λΈλμ μ κ·Όνμ¬ μ°Έμ‘°νκ±°λ λ³κ²½νλ €λ©΄ λ¨Όμ  λΈλ μμμ μ κ·Όν΄μΌ νλ€.

<br>

νμ€νΈ λΈλ(text node)

- νμ€νΈ λΈλλ HTML μμμ νμ€νΈλ₯Ό κ°λ¦¬ν€λ κ°μ²΄
- λ¬Έμμ μ λ³΄
- μμλΈλμ μμλΈλμ΄λ©° μμλΈλλ₯Ό κ°μ§ μ μλ λ¦¬νλΈλμ΄λ€.
- μ¦ DOM νΈλ¦¬μ μ΅μ’λ¨
- νμ€νΈ λΈλμ μ κ·Όνλ €λ©΄ λΆλͺ¨μΈ μμ λΈλμ μ κ·Όν΄μΌ νλ€.

<br>

**λΈλ κ°μ²΄μ μμ κ΅¬μ‘°**

- DOMμ κ΅¬μ±νλ λΈλ κ°μ²΄λ ECMAScript μ¬μμ μ μλ νμ€ λΉνΈμΈ κ°μ²΄κ° μλλΌ λΈλΌμ°μ  νκ²½μμ μΆκ°μ μΌλ‘ μ κ³΅νλ νΈμ€νΈ κ°μ²΄λ€.
- νμ§λ§ λΈλκ°μ²΄λ μλ°μ€ν¬λ¦½νΈ κ°μ²΄μ΄λ―λ‘ νλ‘ν νμμ μν μμκ΅¬μ‘°λ₯Ό κ°λλ€.

<br>

β¨μμ½! 

- DOMμ HTML λ¬Έμμ κ³μΈ΅μ  κ΅¬μ‘°μ μ λ³΄λ₯Ό νν
- λΈλ κ°μ²΄μ μ’λ₯, μ¦ λΈλ νμμ λ°λΌ νμν κΈ°λ₯μ νλ‘νΌν°μ λ©μλμ μ§ν©μΈ DOM APIλ‘ μ κ³΅
- DOM APIλ₯Ό ν΅ν΄ HTMLμ κ΅¬μ‘°λ λ΄μ© λλ μ€νμΌ λ±μ λμ μΌλ‘ μ‘°μ κ°λ₯

<br>

## μμ λΈλ μ·¨λ

- HTMLμ κ΅¬μ‘°λ λ΄μ© λλ μ€νμΌ λ±μ λμ μΌλ‘ μ‘°μνλ €λ©΄ λ¨Όμ  μμ λΈλλ₯Ό μ·¨λν΄μΌνλ€.
- νμ€νΈ λΈλ, μ΄νΈλ¦¬λ·°νΈ λΈλλ₯Ό μ‘°μνκ³ μ ν λλ λ§μ°¬κ°μ§μ΄λ€.

- `document.getElementById()`
- `document.getElementsByName()`
- `document.getElementsByClassName()`
- `document.querySelector()` β¨
- `document.querySelectorAll()` β¨
- `element.matches()` β νΉμ  μμ λΈλ μ·¨λ, μ΄λ²€νΈ μμμ μ¬μ©ν  λ μ μ©

<br>

## λΈλ νμ

- μμ λΈλλ₯Ό μ·¨λν λ€μ, μ·¨λν μμ λΈλλ₯Ό κΈ°μ μΌλ‘ DOM νΈλ¦¬μ λΈλλ₯Ό μ?κ²¨ λ€λλ©° λΆλͺ¨, νμ , μμ λΈλ λ±μ νμ ν΄μΌ ν  λκ° μλ€.
- DOM νΈλ¦¬ μμ λΈλλ₯Ό νμν  μ μλλ‘ Node, Elenment μΈν°νμ΄μ€λ νΈλ¦¬ νμ νλ‘νΌν°λ₯Ό μ κ³΅νλ€.
- Nodeμμ μ κ³΅νλ νλ‘νΌν°
    - parnetNode
    - previousSibling
    - firstChild
    - childNode
- Element μμ μ κ³΅νλ νλ‘νΌν°
    - previousElementSibling
    - nextElementSibling
    - children
- λΈλ νμ νλ‘νΌν°λ λͺ¨λ μ κ·Όμ νλ‘νΌν°
- λ¨, setter μμ΄ getterλ§ μ‘΄μ¬νμ¬ μ°Έμ‘°λ§ κ°λ₯ν μ½κΈ° μ μ© μ κ·Όμ νλ‘νΌν°
- μ½κΈ° μ μ© μ κ·Όμ νλ‘νΌν°μ κ°μ ν λΉνλ©΄ μλ¬΄λ° μλ¬ μμ΄ λ¬΄μλλ€.

<br>

**κ³΅λ°± νμ€νΈ λΈλ**

- HTML μμ μ¬μ΄μ μ€νμ΄μ€, ν­, μ€λ°κΏ(κ°ν) λ±μ κ³΅λ°± λ¬Έμλ νμ€νΈ λΈλλ₯Ό μμ±νλ€.

<br>

**μμ λΈλ νμ**

- `element.children`
- `node.childNode`
- `node.firstChild`
- `node.lastChild`

<br>

**μμ λΈλ μ‘΄μ¬ νμΈ**

- `node.hasChildNode`
- μ‘΄μ¬μ λ¬΄λ λΆλ¦¬μΈκ°μΌλ‘ λ°ν

<br>

**μμλΈλμ νμ€νΈ λΈλ νμ**

- `firstChild`

<br>

**λΆλͺ¨ λΈλ νμ**

- `node.parentNode`

<br>

**νμ  λΈλ νμ**

- `node.previousSibling` β μμ  μ΄μ  νμ 
- `node.nextSibling` β μμ  μ΄ν νμ 
- `element.previousElementSibling`
- `element.nextElementSibling`

<br>

### λΈλ μ λ³΄ μ·¨λ

- `node.nodeType` β λΈλ κ°μ²΄ μ’λ₯, λΈλνμμ λνλ΄λ μμλ₯Ό λ°ν
- `node.nodeName` β λΈλμ μ΄λ¦μ λ¬Έμμ΄λ‘ λ°ν

<br>

### μμ λΈλμ νμ€νΈ μ‘°μ

- setter μ getterκ° λͺ¨λ μ‘΄μ¬νλ μ κ·Όμ νλ‘νΌν°, μ°Έμ‘°μ ν λΉ λͺ¨λ κ°λ₯
- `node.nodeValue` β λΈλ κ°μ²΄μ κ° λ°ν, νμ€νΈ
- `node.textContent` β νμ€νΈ λͺ¨λ λ°ν

<br>

## DOM μ‘°μ

- DOM μ‘°μμ μλ‘μ΄ λΈλλ₯Ό μμ±νμ¬ DOMμ μΆκ°νκ±°λ κΈ°μ‘΄ λΈλλ₯Ό μ­μ  λλ κ΅μ²΄νλ κ²
- λ¦¬νλ‘μ°, λ¦¬νμΈνΈκ° λ°μνλ μμΈμΌλ‘ μ±λ₯μ μν₯μ μ€λ€.

<br>

**innerHTML**

- `element.innerHTML` β HTML λ§ν¬μ λ³κ²½
- μ¬μ©μλ‘λΆν° μλ ₯λ°μ λ°μ΄ν°λ₯Ό κ·Έλλ‘ innerHTML νλ‘νΌν°μ ν λΉνλ κ²μ ν¬λ‘μ€ μ¬μ΄νΈ μ€ν¬λ¦½ν κ³΅κ²©(XSS)μ μ·¨μ½νλ―λ‘ μννλ€.

<br>

**λΈλ μμ±κ³Ό μΆκ°**

- `document.createElement(tagname)` β μμ λΈλ μμ±
- μμλΈλλ₯Ό μμ±ν  λΏ DOMμ μΆκ°νμ§λ μλλ€.
- λ°λΌμ μ΄λ£¨μ μμ±λ μμ λΈλλ₯Ό DOMμ μΆκ°νλ μ²λ¦¬κ° λ³λλ‘ νμνλ€.
- `document.createTextNode(text)` β νμ€νΈ λΈλ μμ±

<br>

**λΈλμ½μ**

- `node.appendChild(μΆκ°ν  μμ)`
- λΆμ κ΄κ³λ‘ μ°κ²°ν μμ λΈλμ λ§μ§λ§ μμ μμλ‘ μΆκ°
- `node.insertBefore(newNode, childNode)`

<br>

**λΈλ λ³΅μ¬**

- `node.cloneNode`

<br>

**λΈλ κ΅μ²΄** 

- `node.replaceChild`

<br>

**λΈλ μ­μ **

- `node. removeChild(child)`

<br>

## μ΄νΈλ¦¬λ·°νΈ

- getterλ§ μ‘΄μ¬νλ μ½κΈ° μ μ© μ κ·Όμ νλ‘νΌν°
- μ΄νΈλ¦¬λ·°νΈ κ°μ μ·¨λν  μ μμ§λ§ λ³κ²½ν  μ μμ
- `element.getAttribute()` β μ΄νΈλ¦¬λ·°νΈκ° μ·¨λ
- `element.setAttribute('class', 'title')` β μ΄νΈλ¦¬λ·°νΈκ° λ³κ²½

<br>

## μ€νμΌ

**μΈλΌμΈ μ€νμΌ μ‘°μ** 

- `element.style`
- setter μ getterκ° λͺ¨λ μ‘΄μ¬νλ μ κ·Όμ νλ‘νΌν°λ‘μ μΈλΌμΈμ€νμΌμ μ·¨λνκ±°λ μΆκ° λλ λ³κ²½ νλ€.
- μλ₯Όλ€μ΄ `div.style.backgroundColor = βblueβ;`

<br>

**ν΄λμ€ μ‘°μ** 

- `element.className` β λ¬Έμμ΄ λ°ν
- `element.classList` β class μ΄νΈλ¦¬λ·°νΈμ μ λ³΄λ₯Ό λ΄μ κ°μ²΄λ₯Ό λ°ν
    - `element.classList.add(className)`
    - `element.classList.remove(className)`