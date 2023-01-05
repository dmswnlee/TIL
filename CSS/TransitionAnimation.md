# Transition

스르륵

**호버부분에는 transform 부모부분엔 transition(효과줄때)**

<br>

```css
.box{
	transition: font-size 1000ms ease-out, background-color: 2000ms cubic-bazier
	(0.08,0.57,0.97,-0.78) 1000ms;
}
```

* transition : property duration timingfunction delay
* property : 모든속성 또는 일부 속성에 애니메이션 적용
* duration : 작동시간, 시작해서 끝날때까지 시간, 초단위로 지정(ms , s)
* timingfunction : 가속도 , 생략 가능
    * ease , linear 길이증가 , ease-in 가속, ease-out 감속, ease-in-out, cubic-beizer 베이지어곡선 중 선택
* delay : 입력 시간만큼 지난 후 작동, 생략 가능
* 한개이상의 요소에 각각 효과를 주고 싶다면 , 쉼표로 구분하여 사용 가능 

<br>

## transform
요소를 2차원, 3차원 공간에서 변형할 수 있도록 해준다.

<br>

### rotate(Ndeg)
* 요소를 회전할때 사용(시계방향)
* rotate(x,y) | rotateX() | ratateY()
* 주변에 영향 안줌

<br>

### scale(N)
* 자신의 크기를 조절할 때 사용
* scale(x,y) | scaleX() | scaleY()
* 주변에 영향 안줌

<br>

### translate(x,y)
* 요소를 원하는 위치에 옮길때 사용
* translate(x,y) | translateX | translateY
* 단위를 사용할때 px, %(자신의크기 기준)을 사용
* 주변에 영향 안줌

<br>

transform-origin
* 중심축
* top , bottom, center, left, right 사용

perspective
* 앞뒤로 이동
* 부모요소가 앞뒤공간 마련(3D)

<br>
<br>

# Animation
```css
.animation{
	animation: animation-name 1000ms ease-in-out 500ms infinite;
}

@keyframes name{
	from{
		/* Rules */
	}
	to{
		/* Rules */
	}
}

@keyframes name{
	0%{
		/* Rules */
	}

	50%{
		/* Rules */
	}
	
	100%{
		/* Rules */
	}
}
```
* animation : name 작동시간 가속도 딜레이시간 반복횟수 방향
* 다른건 transition과 같음
* animation-iteration-count : 반복횟수 횟수지정(정수) / infinite 무한반복
* animation-direction : 방향 normal / alternate(왕복) / reverse
* animation-fill-mode : 애니메이션이 시작되기 전이나 끝나고 난 후 효과 
    * forward / backward / both / none
* animarion-play-state : 애니메이션의 실행 상태를 설정 paused
* animation-steps() : 애니메이션 동작 지정 steps(10)

