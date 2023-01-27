# 이벤트(Event)
📌 모던자바스크립트 Deep dive 

<br>

- 브라우저는 처리해야 할 특정한 일이 발생하면 이를 감지하여 특정한 타입의 이벤트를 발생 시킨다. (클릭, 키보드입력, 마우스 이동 등)
- 이벤트 핸들러(event handler) : 이벤트가 발생했을 때 호출될 함수
- 이벤트 핸들러 등록 : 이벤트가 발생했을 때 브라우저에게 이벤트 핸들러의 호출을 위임하는 것

<br>

## 이벤트 타입

- 이벤트 종류를 나타내는 문자열

||||||
|:--:|:--:|:--:|:--:|:--:|
|click|dbclick|mousedown|mouseup|
|mousemove|mouseenter|mouseover|mouseleave|
|mouseout|keydown|keyup|focus|
|blur|submit|resize|scroll|
||||||

<br>

## 이벤트 핸들러 등록

- 이벤트 핸들러를 등록하는 방법은 3가지 이다.

<br>

**이벤트 핸들러 어트리뷰트 방식**

- on 접두사와 이벤트 종류를 나타내는 이벤트 타입으로 이루어져 있다.
- 이벤트 핸들러 어트리뷰트 값은 사실 암묵적으로 생성될 이벤트 핸들러의 함수 몸체를 의미한다.
- 오래된 코드에서 간혹 이 방식을 사용한 것이 있기 때문에 알아둘 필요는 없지만 더는 사용하지 않는것이 좋다.
- HTML 과 자바스크립트는 혼재하는 것보다 분리하는 것이 좋다.
- `<div onclick={handleClick}></div>`

<br>

**이벤트 핸들러 프로퍼티 방식**

- 이벤트 타겟(event target) : 이벤트 핸들러를 등록하기 위해서 이벤트를 발생시킬 객체
- 이벤트 타입(event type) : 이벤트의 종류를 나타내는 문자열
- 이벤트 핸들러  이렇게 3가지를 지정해야 한다.
- `button.onclick = function() {};` → 이벤트타켓.이벤트타입 = 이벤트핸들러(함수)
- 이벤트 핸들러 프로퍼티에 하나의 이벤트 핸들러만 바인딩할 수 있다는 단점이 있다.

<br>

✨ **addEventListener 메서드 방식**

- DOM Level2 에서 도입된 메서드
- `EventTarget.addEventListener ('event type', functionName, useCapture(생략가능))`
- 마지막 매개변수에는 이벤트를 캐치할 이벤트 전파 단계(캡처링 또는 버블링)을 지정한다.
- 생략하거나 false를 지정하면 버블링 단계에서 이벤트를 캐치
- true를 지정하면 캡처링 단계에서 이벤트 캐치
- 하나 이상의 이벤트 핸들러를 등록할 수 있으며 등록된 순서대로 호출된다.

<br>

## 이벤트 핸들러 제거

- `EventTarget.removeEventListener ('event type', functionName, usecapture(생략가능))`
- 대신 addEventListener 메서드와 전달한 인수가 일치하지 않으면 핸들러가 제거되지 않는다.

<br>

## 이벤트 객체

- 이벤트가 발생하면 이벤트에 관련한 다양한 정보를 담고 있는 이벤트 객체가 동적으로 생성된다.
- 생성된 이벤트 객체는 이벤트 핸들러의 첫 번째 인수로 전달된다. (e, event)
- 이벤트 객체는 이벤트 핸들러의 첫 번째 인수로 전달되어 매개변수 e에 암묵적으로 할당 된다.
- 브라우저가 이벤트 핸들러를 호출할 때 이벤트 객체를 인수로 전달하기 때문이다.
- 이벤트 객체 중 일부는 사용자의 행위에 의해 생성된 것이고 일부는 자바스크립트 코드에 의해 인위적으로 생성된 것이다.
- Event 인터페이스는 DOM 내에서 발생한 이벤트에 의해 생성되는 이벤트 객체를 나타낸다.
- Event 인터페이스에는 모든 이벤트 객체의 공통 프로퍼티가 정의되어 있다.
- FocusEvent, MouseEvent, KeyboardEvent, WheelEvent 같은 하위 인터페이스에는 이벤트 타입에 따라 고유한 프로퍼티가 정의되어 있다.

<br>

**이벤트 객체의 공통 프로퍼티** 

- Event 인터페이스의 이벤트 관련 프로퍼티는 모든 이벤트 객체가 상속 받는 공통 프로퍼티다.
- type → 이벤트 타입, 문자열
- target → 이벤트를 발생시킨 DOM요소, DOM 요소 노드
- currentTarget → 이벤트 핸들러가 바인딩 된 DOM 요소, DOM 요소 노드

<br>

**마우스 정보 취득**

- click, mousedown 등 이벤트가 발생하면 생성되는 MouseEvent 타입의 이벤트 객체가 가지는 고유 프로퍼티
- 마우스 포인터의 좌표 정보를 나타내는 프로퍼티
    - screenX / Y
    - client X / Y
    - page X / Y
    - offset X / Y
- 버튼 정보를 나타내는 프로퍼티
    - altkey
    - ctrlkey
    - shiftkey
    - button

<br>

**키보드 정보 취득** 

- keydown, keyup 이벤트가 발생되면 생성되는 keyboardEvent 타입 이벤트 객체가 가지는 고유 프로퍼티
- altkey , ctrlkey, shiftkey, metakey, key, keycode
- input 요소는 한글을 입력하고 엔터 키를 누르면 keyup 이벤트 핸들러가 두 번 호출되는 현상이 발생한다. 이 같은 문제를 회피 하려면 keydown 이벤트를 사용하면 된다.

<br>

## 이벤트 전파

- DOM 트리 상에 존재하는 DOM 요소 노드에서 발생한 이벤트는 DOM 트리를 통해 전파된다. 이를 이벤트 전파(event propagation) 라고 한다.
- 생성된 이벤트 객체는 이벤트를 발생시킨 DOM 요소인 이벤트 타겟을 중심으로 DOM트리를 통해 전파된다.
- 캡처링 단계에서 이벤트를 캐치해야 할 경우는 거의 없다.
- 이벤트는 이벤트를 발생시킨 이벤트 타킷은 물론 상위 DOM 요소에서도 캐치할 수 있다.
- DOM 트리를 통해 전파되는 이벤트는 이벤트 패스에 위치한 모든 DOM 요소를 캐치할 수 있다.

<br>

1. 캡처링 단계(capturing phase) : 이벤트가 상위 요소에서 하위 요소 방향으로 전파
2. 타깃 단계(target phase) : 이벤트가 이벤트 타깃에 도달
3. 버블링 단계(bubbling phase) : 이벤트가 하위 요소에서 상위 요소 방향으로 전파 

<br>

## 이벤트 위임

- 이벤트 위임(event delegation)은 여러개의 하위 DOM 요소에 각각 이벤트 핸들러를 등록하는 대신 하나의 상위 DOM 요소에 이벤트 핸들러를 등록하는 방법을 말한다.
- 이벤트는 이벤트 타깃은 물론 상위 DOM 요소에서도 캐피할 수 있다.
- 이벤트 위임을 통해 상위DOM 요소에 이벤트 핸들러를 등록하면 여러 개의 하위 DOM 요소에 이벤트 핸들러를 등록할 필요가 없다.

<br>

## DOM 요소의 기본 동작 조작

- `e.preventDefault()`  → DOM 요소의 기본 동작 중단
- `e.stopPropagation()` → 이벤트 전파 중단