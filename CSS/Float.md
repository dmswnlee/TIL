# Float
📌 [김버그의css는재밌다](https://edu.goorm.io/lecture/20583/%25EA%25B9%2580%25EB%25B2%2584%25EA%25B7%25B8%25EC%259D%2598-html-css%25EB%258A%2594-%25EC%259E%25AC%25EB%25B0%258C%25EB%258B%25A4)

<br>

* float는 왜 하는걸까? **가로배치** 하기 위해서!
* 블록레벨요소를 가로로 정렬할 때 사용

<br>

### float를 하면 무슨일이 일어나는가
* 많은 자식요소중 하나에 float를 주면 다음 자식요소가 해당 자식요소 자리로 끌려오고 부모요소의 크기가 남은 자식요소에 맞게 줄어든다. 

* float를 하면 block 요소가 된다. 

* block이 되긴 하지만 길막을 하지 못하는 block이 된다. → 해당 컨텐츠의 내용물 크기만큼 크기를 가진다.
* block이 되면 나머지 공간에 margin이 생겨야 하는데 float는 안 생김

* block 요소는 float 된 요소를 무시하지만 inline 요소는 float 된 요소를 인식해서 적용된다.
* 글자는 float에 가려지지 않는다. 

<br>

➡ float를 시용하면 되도록 width값을 지정해주는게 좋음
<br>
➡ float를 사용하면 레이아웃이 깨지는 경우가 많음 그래서 요즘은 잘 사용하지 않지만 오래된 코드를 정비할 때 필요할 수 있으니 잘 알아두자! 

<br>

### float로 인해 깨진 레이아웃 정비하기
* 부모요소에 `overflow:hidden;` (or `overflow:auto` 크기가 자동으로 잡힘)
* clearfix(가장 정석인 방법)
    * clear 란? 끌어당기는걸 끊어버리고 자기자기를 지키는 것
    * left | right | both
* 공갈 div (추천하지않음)
* 가상요소 이용하기(가장 추천)
    * 가상요소? html에 존재하지 않는 요소
    * 각 요소당 두개씩 만들 수 있다. (before, after)
    * 가상요소에 반드시 작성해야하는 프로퍼티? content
    * 부모요소에 가상요소를 만들어 주면 된다. 

<br>

```css
.parent::before{
    content:'';
    display:block;
    clear:both
    /* left | right | both */
}
```
