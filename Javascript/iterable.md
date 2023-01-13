# 이터러블(iterable)

### 이터레이션 프로토콜
* 순회 가능한 자료구조을 만들기 위해 ES6에 도입된 규칙
* 배열, 문자열, 유사 배열 객체, DOM 등 자신만의 메서드를 가지고 순회하였는데 이터레이션 프로토콜을 준수하는 이터러블로 통일
* for...of문, spread, 배열 디스트럭처링 할당

<br>

```js
[symbol.iterator](){
    next(){
        return {value: 0, done: true};
    }
}
```
<br>

## 이터러블 
* symbol.iterator를 프로퍼티 키로 사용한 메서드를 직접 구현하거나 프로토타입 체인을 통해 상속받은 객체
* 일반 객체는 이터러블이 아니므로 for...of문, spread, 배열 디스트럭처링 할당을 사용할 수 없음
* 이터러블 프로토콜을 준수한 객체 

<br>

## 이터레이터 
* 이터러블의 symbol.iterator 메서드가 반환한 이터레이터는 next 메서드를 가짐
* next 메서드는 각 요소를 순회하는 포인터 역할을 함
* value, done 메서드를 가짐
* 이터레이터 프로토콜을 준수한 객체 