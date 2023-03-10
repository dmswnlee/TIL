# 스코프(Scope)
📌[poiemaweb](https://poiemaweb.com/) , 모던자바스크립트(deep dive)

<br>

### 스코프란?
* 유효범위
* 자바스크립트를 포함한 모든 언어의 기본적이고 중요한 개념
* 변수를 참조할 수 있는 유효한 범위
* 모든 식별자(변수이름, 함수이름, 클래스이름 등)가 유효한 범위
* 블록안에서만 유효(if, for, function ....)

<br>
자바스크립트 엔진은 스코프를 통해 어떤 변수를 참조해야 할것 인지 결정한다.

```js
const x = 'global';

function foo(){
    const x = 'local';
    console.log(x) // local
}

foo()

console.log(x) // global
```

<br>

### 스코프의 종류
* 전역(global)
    * 코드 가장 바깥영역
    * 전역은 전역 스코프를 만든다
    * 전역변수는 어디서든지 참조 가능

<br>

* 지역(local)
    * 함수 몸체 내부
    * 지역은 지역 스코프를 만든다
    * 자신이 선언된 지역과 하위지역에서만 참조 가능

<br>

### 스코프체인
* 자바스크립트 엔진이 스코프체인을 통해 상위 스코프방향으로 참조할 변수를 검색
* 스코프가 계층적으로 연결된 것
* 모든 지역스코프의 최상위는 전역스코프 

