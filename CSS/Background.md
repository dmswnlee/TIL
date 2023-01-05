# Background
```css
.box{
	background: #ccc url(images/smile.jpg) no-repeat 100% 100% fixed;
}
```

<br>

### background-color
* hex , rgb, rgba

<br>

### background-image
* url(이미지가 있는 경로)
* 자체적으로 가지고 있는 이미지 or 이미지 주소

<br>

### background-repeat
* repeat(기본값) | no-repeat (반복안함) | repeat-x 가로로 반복 | repeat-y 세로로 반복

<br>

### background-size
* contain → 요소 안에 이미지크기 그대로 들어가는것
* cover → 요소안에 이미지가 꽉차게 들어가는것 (이미지 크기에 따라 잘라짐)
* custom → 가로,세로크기 조절하는 것 (%, px로 사용)

<br>

### background-position
* x , y 
* top, bottom, center, left, right  혹은 px, %로 조절
* center center를 제일 많이 사용
* scroll(기본값) | fixed(스크린화면을 기준 고정)

