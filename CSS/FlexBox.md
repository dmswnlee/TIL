# Flex box
📌 [김버그의css는재밌다](https://edu.goorm.io/lecture/20583/%25EA%25B9%2580%25EB%25B2%2584%25EA%25B7%25B8%25EC%259D%2598-html-css%25EB%258A%2594-%25EC%259E%25AC%25EB%25B0%258C%25EB%258B%25A4)

<br>

* 여유 공간에 따라 너비나 높이, 위치를 자유롭게 변형할 수 있다. 
* 정렬의 끝판왕

<br>


### 선언하기 
```css
.flexbox{
    display: flex;
    /* flex | inline-flex */
}
```
* 배치 요소들을 감싸는 부모요소에게 선언, 플렉스 컨테이너로 지정
* flex : 플렉스 박스를 블록 레벨요소로 정의, 공간이 줄어들면 자동으로 내용물을 줄여줌
* inline-flex : 플렉스 박스를 인라인 레벨요소로 정의, 공간이 안줄어든다. 

<br>

### 가로, 세로 정렬
```css
.flexbox{
    display: flex;
    flex-direction : row;
    /* row | row-reverse(가로역순) | column | colum-reverse(세로역순) */
}
```
* 플렉스 항목 배치방향 지정
* 보이지 않는 두개의 Axis(축)이 생김
* Main axis(주축) Cross axis(교차축)
* flex-direction : row → 주축은 가로, 교차축은 세로
* flex-direction : column → 주축은 세로, 교차축은 가로

<br>

### 한줄에 정렬
```css
.flexbox{
    display: flex;
    flex-direction : row;
    flex-wrap : nowrap 
    /* nowrap (기본값) | wrap */
}
```
* 플렉스 항목을 한 줄 또는 여러 줄로 배치
* 감싸지 않고 자식의 사이즈를 줄여서라도 한 줄로 정렬해버리는 **nowrap**
* 한 줄에 모두 정렬하기에 공간이 넉넉하지 않으면 여러 줄을 만들어 버리는 **wrap**
* wrap-reverse(역순)

<br>

### justify-content
```css
.flexbox{
    justify-content : flex-start;
}
```
* 플렉스 항목을 **주축 방향**으로 배치할 때(자식요소를 어떻게 배치시킬것인가) 
* flex-start(기본값) | flex-end | center | space-between(사이공간을 똑같이 만들어주는것) | space-around(각각의 플렉스아이템의 양쪽 여백이 같게 위치)

<br>

### align-items
* 플렉스 항목을 **교차축** 기준으로 배치할 떄
* stretch(기본값) | flex-start | flex-end | center | baseline (글자의 아래쪽 기준으로 나머지 높이를 맞춰줌)
* stretch 높이를 지정하지 않았을 경우 해당 영역만큼 늘어남

<br>

### align-self
* 교차축을 기준으로 자식요소인 플렉스 항목을 각각 배치
* auto | stretch (기본값) | flex-start | flex-end | center | baseline

<br>

**align-items를 먼저 해보고 안되면 align-self를 해본다**

<br>

### flex 항목의 배치 순서 바꾸기 
* order 순서 바꾸기 가능 (1,2,3.. 순서대로 바꾸면 됨)

