# Position
📌 [김버그의css는재밌다](https://edu.goorm.io/lecture/20583/%25EA%25B9%2580%25EB%25B2%2584%25EA%25B7%25B8%25EC%259D%2598-html-css%25EB%258A%2594-%25EC%259E%25AC%25EB%25B0%258C%25EB%258B%25A4)

<br>

* 요소를 원하는 위치에 자유롭게 이동시키기 위해 사용하는 프로퍼티 

<br>

* static
* relative
* absolute
* fixed
* sticky (아직 지원하는 브라우저가 많이 없음)

<br>

* Type → 기준점 (타입에 따라 기준점이 많이 달라진다.)

<br>

## position : static
* 모든 요소의 기본값

<br>

## position : relative
* 기준점 : 원래 자기자신이 있던 자리
* float와 다른점은 자신의 자리가 유지 된다는 것
* 주변에 있는 부모, 형제요소에 영향을 미치지 않는다. 

<br>

## position : absolute
* float를 사용했을떄와 동일한 현상
* 대신 인라인이 피해서 적용되진 않는다.
* 기준점 : 직접 정할 수 있음, position : static이 아닌 요소(자신의 부모요소의 position)
* 어떤 기준점을 기준으로 움직일건지 정하는게 중요
* 보통 기본이 되는 기준점은 relative
* 단, 기본적으로 body는 position : relative가 적용 되어 있기 떄문에 따로 적용 안해줘도 됨

<br>

## position : fixed
* position : absolute와 동일한 현상이 일어난다. 대신 기준점이 다르다.
* 기준점 : viewport를 기준으로 한다. 
* 레이어개념 본문 위에 위치, 주변에 영향을 줌
* 스크롤바가 나타나더라도 항상 같은 위치에 배치됨

<br>

## top | bottom | left | right 
* 보통 사용 할 떄는 top or bottom / left or right 중 하나만 사용 

<br>

## z-index 
* 레이어 순서 바꿈
* z축으로 내가 몇번째에 속해 있는지 
* 숫자가 클수록 맨 위에 위치
* position 을 쓴곳에서만 사용 가능 
