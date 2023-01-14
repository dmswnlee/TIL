# 단축평가(short-circuit evaluation)
📌[poiemaweb](https://poiemaweb.com/) , 모던자바스크립트(deep dive)

<br>

* 논리 연산자를 사용한 단축평가
* 논리 연산의 결과를 결정하는 피연산자를 타입 변환하지 않고 그대로 반환
* 표현식을 평가하는 도중에 평가결과가 확정된 경우 나머지 평가를 생략하는 것

<br>

`논리곱(&&)`과`논리합(||)`은 언제나 2개의 피연산자 중 어느 한쪽으로 평가 된다.

<br>

### 논리곱(&&)
```js
true && true // true
true && false // false
false && false // false

'cat' && 'dog' // dog
```
* AND 그리고
* 평가는 좌항에서 우항으로 진행
* 논리곱은 두개의 피연산자 모두가 true여야 true가 반환되기 때문에 두번째 피연산자까지 평가가 진행되야 평가 결과를 반환 가능 
* 논리 연산의 결과를 결정하는 두 번째 피연산자를 그대로 반환

<br>

### 논리합(||)
```js
true && true // true
true && false // true
false && false // false

'cat' && 'dog' // cat
```
* OR 또는
* 평가는 좌항에서 우항으로 진행
* 논리합은 두개의 피연산자중 하나만 true여도 true를 반환하기 때문에 첫번째 피연산자까지만 평가가 진행되어 평가 결과를 반환 함
* 논리 연산의 결과를 결정한 첫번째 피연산자를 그대로 반환

<br>

### 옵셔널 체이닝(optional chaining)
* ES11 (ECMAScript 2020)
* ?.
* 좌항의 피연산자가 null 또는 undefined인 경우 undefined을 반환하고 아니면 우항의 프로퍼티 값 참조 
* 논리연산자를 사용하는것 보다 간단해짐

<br>

### null 병합 연산자(Nullish Coalescing Operator)
* ES11 (ECMAScript 2020)
* ??
* 좌항의 피연산자가 null 또는 undefined인 경우 우항의 피연산자를 반환하고 아니면 좌항의 피연산자 반환
* 변수의 기본값을 설정할 때 유용 