# set 과 map ... symbol
📌[poiemaweb](https://poiemaweb.com/) , 모던자바스크립트(deep dive)

<br>

## Set
* 중복되지 않는 유일한 값들의 집합체
* 인덱스 ❌
* 순서 ❌
* 중복 ❌
* 수학적 집합을 구현하기 위한 자료구조

<br>

### set 객체 생성
```js
const set = new Set([1,2,3]);
```

<br>

### 프로퍼티, 메서드
```js
// 요소 개수 확인
set.size()

// 추가
set.add()

// 존재확인, 불리언값 반환
set.has()

// 삭제, 불리언값 반환
set.delete()

// 일괄 삭제
set.clear()

// 요소 순회
set.forEach(() => {})
```

<br>

## Map
* 키와 값으로 구성
* 순서 ❌
* 키만 다르다면 중복 가능
* 오브젝트와 유사
* 키로만 프로퍼티, 메서드 사용가능

<br>

### map 객체 생성
```js
const map = new Map(['key1', 'value1'], ['key2', 'value2']);
```

<br>

### 프로퍼티, 메서드
* set과 같음

<br>

## Symbol
* es6 
* 변경 불가능한 원시값
* 유일한 프로퍼티 키를 만들기 위해 사용
* Symbol 함수로 호출
* 생성된 값은 외부로 노출되지 않음

<br>

```js
const key1 = Symbol('key');
const key2 = Symbol('key');
```
* 값이 같아도 키 값이 다르면 생성 가능








