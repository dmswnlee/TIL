# DOM(Document Object Model)
📌 모던자바스크립트 Deep dive 

<br>

- 브라우저의 렌더링 엔진은 HTML 문서를 파싱하여 브라우저가 이해할 수 있는 자료구조인 DOM을 생성한다.
- DOM은 HTML 문서의 계층적 구조와 정보를 표현하며 이를 제어할수 있는 API, 즉 프로퍼티와 메서드를 제공하는 트리 자료구조다.

<br>

## 노드

**HTML 요소와 노드 객체**

- HTML 요소는 렌더링 엔진에 의해 파싱되어 DOM을 구성하는 요소 노드 객체로 변환한다.
- 이때 HTML 요소의 어트리뷰트는 어트리뷰트 노드로, 텍스트는 텍스트 노드로 변환된다.
- HTML 요소간에는 중첩관계에 의해 계층적인 부자관계가 형성된다.
- 이런 부자관계를 반영하여 HTML 요소를 객체화한 모든 노드 객체들을 **트리 자료구조**로 구성한다.
    - 트리 자료구조는 노드들의 계층구조로 이뤄진다.
    - 부모도느와 자식노드로 구성되어 노드간의 계층적구조(부자, 형제 관계)를 표현하는 비선형 자료구조를 말한다.
    - 하나의 최상위 노드에서 시작한다.
    - 루트 노드(root node) 라고 불리는 최상위 노드는 0개 이상의 자식노드는 갖는다
    - 자식 노드가 없는 노드를 리프노드(leaf node) 라고 한다.
- 노드 객체들로 구성된 트리 자료주고를 DOM 이라 한다. (DOM 트리)

<br>

**노드 객체의 타입**

- 노드 객체는 종류가 있고 상속 구조를 갖는다.
- 노드 객체는 총 12개의 종류(노드타입)가 있고 그 중 중요한 노드타입은 4가지 이다.

<br>

문서노드(document node)

- DOM 트리의 최상위에 존재하는 루트 노드로서 document 객체를 가리킨다.
- 브라우저가 렌더링한 html 문서 전체를 가리키는 객체로서 전역 객체 window의 document 프로퍼티에 바인딩되어 있다.
- 문서노드, 즉 document 객체는 DOM 트리의 루트 노드이므로 DOM 트리의 노드들에 접근하기 위한 진입점 역할을 한다.
- 요소, 어트리뷰트, 텍스트 노드에 접근하려면 문서 노드를 통해야 한다.

<br>

요소노드(element node) 

- 요소 노드는 HTML 요소를 가리키는 객체
- 요소간의 중첩에 의해 부자관계를 가지며 정보를 구조화한다.
- 문서의 구조

<br>

어트리뷰트 노드(attribute node) 

- 어트리뷰트 노드는 HTML 요소의 어트리뷰트를 가리키는 객체
- 요소노드와 연결되어 있다.
- 부모노드가 없어 요소와 형제 노드는 아니다.
- 어트리뷰트 노드에 접근하여 참조하거나 변경하려면 먼저 노드 요소에 접근해야 한다.

<br>

텍스트 노드(text node)

- 텍스트 노드는 HTML 요소의 텍스트를 가리키는 객체
- 문서의 정보
- 요소노드의 자식노드이며 자식노드를 가질 수 없는 리프노드이다.
- 즉 DOM 트리의 최종단
- 텍스트 노드에 접근하려면 부모인 요소 노드에 접근해야 한다.

<br>

**노드 객체의 상속 구조**

- DOM을 구성하는 노드 객체는 ECMAScript 사양에 정의된 표준 빌트인 객체가 아니라 브라우저 환경에서 추가적으로 제공하는 호스트 객체다.
- 하지만 노드객체도 자바스크립트 객체이므로 프로토타입에 의한 상속구조를 갖는다.

<br>

✨요약! 

- DOM은 HTML 문서의 계층적 구조와 정보를 표현
- 노드 객체의 종류, 즉 노드 타입에 따라 필요한 기능을 프로퍼티와 메서드의 집합인 DOM API로 제공
- DOM API를 통해 HTML의 구조나 내용 또는 스타일 등을 동적으로 조작 가능

<br>

## 요소 노드 취득

- HTML의 구조나 내용 또는 스타일 등을 동적으로 조작하려면 먼저 요소 노드를 취득해야한다.
- 텍스트 노드, 어트리뷰트 노드를 조작하고자 할때도 마찬가지이다.

- `document.getElementById()`
- `document.getElementsByName()`
- `document.getElementsByClassName()`
- `document.querySelector()` ✨
- `document.querySelectorAll()` ✨
- `element.matches()` → 특정 요소 노드 취득, 이벤트 위임을 사용할 때 유용

<br>

## 노드 탐색

- 요소 노드를 취득한 다음, 취득한 요소 노드를 기점으로 DOM 트리의 노드를 옮겨 다니며 부모, 형제, 자식 노드 등을 탐색 해야 할 때가 있다.
- DOM 트리 상의 노드를 탐색할 수 있도록 Node, Elenment 인터페이스는 트리 탐색 프로퍼티를 제공한다.
- Node에서 제공하는 프로퍼티
    - parnetNode
    - previousSibling
    - firstChild
    - childNode
- Element 에서 제공하는 프로퍼티
    - previousElementSibling
    - nextElementSibling
    - children
- 노드 탐색 프로퍼티는 모두 접근자 프로퍼티
- 단, setter 없이 getter만 존재하여 참조만 가능한 읽기 전용 접근자 프로퍼티
- 읽기 전용 접근자 프로퍼티에 값을 할당하면 아무런 에러 없이 무시된다.

<br>

**공백 텍스트 노드**

- HTML 요소 사이의 스페이스, 탭, 줄바꿈(개행) 등의 공백 문자는 텍스트 노드를 생성한다.

<br>

**자식 노드 탐색**

- `element.children`
- `node.childNode`
- `node.firstChild`
- `node.lastChild`

<br>

**자식 노드 존재 확인**

- `node.hasChildNode`
- 존재유무는 불리언값으로 반환

<br>

**요소노드의 텍스트 노드 탐색**

- `firstChild`

<br>

**부모 노드 탐색**

- `node.parentNode`

<br>

**형제 노드 탐색**

- `node.previousSibling` → 자신 이전 형제
- `node.nextSibling` → 자신 이후 형제
- `element.previousElementSibling`
- `element.nextElementSibling`

<br>

### 노드 정보 취득

- `node.nodeType` → 노드 객체 종류, 노드타입을 나타내는 상수를 반환
- `node.nodeName` → 노드의 이름을 문자열로 반환

<br>

### 요소 노드의 텍스트 조작

- setter 와 getter가 모두 존재하는 접근자 프로퍼티, 참조와 할당 모두 가능
- `node.nodeValue` → 노드 객체의 값 반환, 텍스트
- `node.textContent` → 텍스트 모두 반환

<br>

## DOM 조작

- DOM 조작은 새로운 노드를 생성하여 DOM에 추가하거나 기존 노드를 삭제 또는 교체하는 것
- 리플로우, 리페인트가 발생하는 원인으로 성능에 영향을 준다.

<br>

**innerHTML**

- `element.innerHTML` → HTML 마크업 변경
- 사용자로부터 입력받은 데이터를 그대로 innerHTML 프로퍼티에 할당하는 것은 크로스 사이트 스크립팅 공격(XSS)에 취약하므로 위험하다.

<br>

**노드 생성과 추가**

- `document.createElement(tagname)` → 요소 노드 생성
- 요소노드를 생성할 뿐 DOM에 추가하지는 않는다.
- 따라서 이루에 생성된 요소 노드를 DOM에 추가하는 처리가 별도로 필요하다.
- `document.createTextNode(text)` → 텍스트 노드 생성

<br>

**노드삽입**

- `node.appendChild(추가할 요소)`
- 부자 관계로 연결한 요소 노드의 마지막 자식 요소로 추가
- `node.insertBefore(newNode, childNode)`

<br>

**노드 복사**

- `node.cloneNode`

<br>

**노드 교체** 

- `node.replaceChild`

<br>

**노드 삭제**

- `node. removeChild(child)`

<br>

## 어트리뷰트

- getter만 존재하는 읽기 전용 접근자 프로퍼티
- 어트리뷰트 값을 취득할 수 있지만 변경할 수 없음
- `element.getAttribute()` → 어트리뷰트값 취득
- `element.setAttribute('class', 'title')` → 어트리뷰트값 변경

<br>

## 스타일

**인라인 스타일 조작** 

- `element.style`
- setter 와 getter가 모두 존재하는 접근자 프로퍼티로서 인라인스타일을 취득하거나 추가 또는 변경 한다.
- 예를들어 `div.style.backgroundColor = ‘blue’;`

<br>

**클래스 조작** 

- `element.className` → 문자열 반환
- `element.classList` → class 어트리뷰트의 정보를 담은 객체를 반환
    - `element.classList.add(className)`
    - `element.classList.remove(className)`