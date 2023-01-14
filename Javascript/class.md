# 클래스(Class)
📌[poiemaweb](https://poiemaweb.com/) , 모던자바스크립트(deep dive)

<br>

* es6 도입
* 생성자 함수와 같이 템플릿처럼 사용하여 동일한 객체 여러가지를 간편하게 생성
* 기존에 사용하던 생성자함수 대신 사용할 수 있는 문법적 설탕(syntactic sugar) 이라고 할 수 있음
* 프로토타입 기반을 클래스 기반 처럼 사용할 수 있도록 함
* 클래스는 함수이며 일급객체 즉 일급객체 특징을 가짐


<br>

### 기본구조
```js
class Book {
    constructor(title) {
        this.title = title;
    }

    display = () => {
        console.log(`The title of this book is ${name}`);
    }
}

const book  = new Book('harry potter');
console.log(book.title);
```
* 클래스에서는 반드시 new 연산자와 함께 호출해야 함
* 한 개의 constructor 존재
* 정적메서드 사용 가능

<br>

### 메서드 
* constructor 메서드 
    * 생성자 함수와 같이 내부에 this를 사용
    * 최대 한 개만 존재 할 수 있음
    * 생략가능, 빈 객체 생성
* 정적메서드(static)
    * 인스턴스를 생성하지 않아도 호출할 수 있는 메서드

<br>

### 프로퍼티
* 접근자 프로퍼티(Accessor Property)
    * 자체적으로 값을 갖지 않고 다른 데이터 프로퍼티 값을 읽거나 저장할 때 사용
    * getter ➡ 인스턴스 프로퍼티에 접근 ➡ get
    * setter ➡ 인스턴스 프로퍼티에 할당 ➡ set

<br>

### 클래스 필드(field)
* 클래스가 생성할 인스턴스의 프로퍼티를 가리키는 것

<br>

### 캡슐화
* 클래스 필드는 기본적으로 public
* 접근을 제어하기 위해서는 필드 선두에 # 을 붙여줌
* 캡슐화를 시키면 내부에서는 접근이 가능 하지만 외부에서는 접근이 불가능함 

<br>

### 상속, 확장
* 기존의 클래스를 상속받아 새로운 클래스를 확장하는 것
* extends 
    * 상속받을 클래스 정의
* super
    * this 처럼 참조할 수 있음 






