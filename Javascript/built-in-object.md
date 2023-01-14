# 빌트인객체(built-in-object)
📌[poiemaweb](https://poiemaweb.com/) , 모던자바스크립트(deep dive)

<br>

자바스크립트의 객체는 세가지로 분류된다.
* 표준 빌트인 객체
    * 전역변수처럼 참조가능
    * 전역객체의 프로퍼티로 제공
* 호스트 객체
    * web APIs
* 사용자 정의객체

<br>

🙋‍♀️ 굳이 원시값이 있는데 객체를 생성하는 빌트인객체가 존재하는 이유가 무엇일까?
<br>
원시값에 객체처럼 마침표표기법(대괄호표기법)를 사용하면 자바스크립트 엔진이 원시값을 객체로 변환해주고 다시 원시값으로 되돌린다.

<br>

### 래퍼 객체(Wrapper object)
* 문자열, 숫자, 불리언 같은 원시값에 객체처럼 접근하면 생성되는 임시 객체

<br>

### 전역 객체(global object)
* 코드가 실행되기 이전에 먼저 생성되어 어떤 객체에도 속하지 않은 최상위 객체
* 브라우저 환경에서는 window(this)
* globalThis
    * es11
    * 브라우저환경, node 환경에서 통일된 전역객체 
    * 모든 환경에서 사용 가능

<br>

### Number
📌[Number - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)
### Math
📌[Math - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)
### String
📌[String - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)
### Date
📌[Date - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)



