# 변수(variable)
📌[poiemaweb](https://poiemaweb.com/) , 모던자바스크립트(deep dive)

<br>

## 변수(variable)란?
* 데이터값을 저장할 때 쓰이는 이름이 붙은 저장소
* 값의 위치(주소)를 기억하는 저장소 
* 변수(variable)명 = 식별자(identifier) 

<br>

### 변수선언 
```js
let coffee;
```

### 변수할당
```js
let coffee = latte;
```

### 변수값 재할당
```js
coffee = americano;
```

<br>

### 변수명 규칙
* 문자, 숫자, $, _ 만 가능
* 대,소문자 구분
* cameCase 
* 숫자로 시작 ❌
* 예약어 ❌

<br>

### var 
* 함수레벨스코프
* var 키워드 생략가능
* 재할당 가능
* 변수 호이스팅
* es6 도입 이후 거의 쓰지 않음

### let
* es6
* 재할당 가능

### **const**
* es6
* 상수
* 상수변수
* 재할당 불가능

<br>

## 데이터타입(data type)

변수에는 다양한 데이터를 저장할 수 있다.

<br>

### 원시타입(primitive)
변경 불가능한 값, 값에 의한 전달 
* number
* string
* boolean
* null
* undefined
* symbol (es6)

<br>

### 객체타입(object/reference)
원시타입을 제외한 나머지 값, 참조에 의한 전달 
* object 
* function


