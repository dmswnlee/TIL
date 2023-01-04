# Box

## Box Model
```css
.box {
    width: 500px;
    height: 300px;
    padding: 20px;
    border: 1px solid #000;
    margin: 30px
}
```
<br>

* 내용물 width + 안쪽여백 padding + 테두리 border + 바깥쪽 여백 margin
* content의 **가로** width , **세로** height
* **안쪽여백**, 즉 content와 border 사이의 공간을 나타내는 **padding**
* **테두리**를 나타내는 **border**
    * border: 굵기 스타일 색상 / border: none
* border-radius 테두리 원형
* **바깥여백**, 즉 요소와 요소 사이의 간격을 나타내는 **margin**

<br>

### 속기형 
* 쉽게 시계방향이라고 생각하면 된다
* top right bottom left
* top bottom, right left 
* top, right left, bottom

<br>

## Box Sizing 
```css
* {
    box-sizing : border-box;
    /* content-box(기본값) | border-box */
}
```

* 보통 처음시작할 때 전체에 border-box를 깔고 시작한다.
* content-box는 정한 크기에서 더해지는 것
* border-box는 정한크기내에서 정해는 것 

<br>

## Box
* Box Type ➡ **display**

<br>

### block
* block → 길막 
* 다른 요소들이 자신의 영역에 침범하지 못하게 하는 요소
* 따로 width를 선언하지 않은 경우, width = 부모의 content-box의 100%
* 따로 width를 선언한 경우, 남은공간은 margin으로 채움 
* 따로 부모의 height를 선언하지 않을 경우, 자식 요소의 height의 합 = 부모의 height
* width, height, border, padding, margin 모두 적용 가능
* margin = 0 auto → 블록을 가운데 위치 시키는 것

<br>

### inline 
* inline → 흐름
* 옆으로 흐르다가 자리가 없으면 줄바꿈 되어 다음줄로 흐름
* block(면,영역) vs inline(선,흐름)
* width, height, padding-top, padding-bottom, margin-top, margin-bottom **사용불가** → 인라인의 흐름을 막는 요소들 이기 때문에 

<br>

### inline-block
* inline 처럼 흐르는 동시에 block 처럼 영역을 잡고 있는 요소
* inline에서 사용하지 못하는 요소들 모두 사용 가능!
* 일렬로 정렬 가능, 마진 패딩값 지정 가능 


