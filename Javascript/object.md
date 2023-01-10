# 객체(Object)

* 다양한 타입의 값을 하나로 묶어주는 자료구조 
* 객체는 0개 이상의 프로퍼티로 구성된 집합
* `{key : value}`
* 프로퍼티와 메서드
    * 프로퍼티 : 객체의 상태를 나타내는 값
    * 프로퍼티를 참조하고 조작할 수 있는 동작(함수)
* 객체는 상태와 동작을 하나로 구조화할 수 있어 유용

<br>

### 객체 생성 방법
* 객체리터럴
* 생성자 함수 
* object.create 메서드

<br>

```js
let person = {
    name : 'jay',
    age : 20
};

//마침표접근법
console.log(person.name); 

//대괄호접근법
console.log(person['name']);
```
* 같은 프로퍼티키를 중복으로 선언하면 나중에 선언한 프로퍼티가 적용됨 

<br>

```js
let person = {
    name: 'jay'
};

//갱신
person.name = 'lee';

//추가
person.age = 20;

//삭제
delete person.age;
```

<br>

프로퍼티 축약
```js
let obj = { x: x, y: y };

let obj = { x, y }
```
* 변수이름과 프로퍼티키가 동일한 이름일 때 프로퍼티 키 생략가능




