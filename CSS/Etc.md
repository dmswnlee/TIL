# Etc

### Box Shadow
```css
.box{
	box-shadow: 0 10px 16px 49px rgba(255,73,73,0.35);
}
```
* 그림자 효과 
* 순서대로 작성
* h-offset(x축)  v-offset(y축)  blur(흐린정도)  spread(그림자사이즈)  color(색상)
* 한번에 쉼표(,)를 사용해서 여러개를 사용할 수 있다.

<br>

### Opacity
* 불투명도
* 0 ~ 1

<br>

### Overflow
* hidden :넘어간 부분 안보이게 숨김 처리
* visible(기본값)  : 기본값, 넘어간 부분 보이게 처리
* scroll : 넘어간 부분 스크롤바로 보여줌
* auto : 넘어가면 자동으로 스크롤바 안넘어가면 안생김
* scroll은 내용이 줄어들어도 스크롤이 있음 auto는 내용이 줄어들면 스크롤이 사라짐
* overflow-x , overflow-y

<br>

### list-style
* none : 가장 많이 씀, 리스트 불렛을 없애줌

<br>

### Visivility
* 보여줄거냐 안보여줄거냐 하는것
* visible(기본값) | hidden(안보이는것)
* 안보이게 처리해도 opacity 0 이랑 비슷 자리는 유지하고 보이지만 않게 처리하는것 (display = none 과 비슷하지만 다른점)