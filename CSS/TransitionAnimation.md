# Transition
๐ [๊น๋ฒ๊ทธ์css๋์ฌ๋ฐ๋ค](https://edu.goorm.io/lecture/20583/%25EA%25B9%2580%25EB%25B2%2584%25EA%25B7%25B8%25EC%259D%2598-html-css%25EB%258A%2594-%25EC%259E%25AC%25EB%25B0%258C%25EB%258B%25A4)

<br>

์ค๋ฅด๋ฅต

**ํธ๋ฒ๋ถ๋ถ์๋ transform ๋ถ๋ชจ๋ถ๋ถ์ transition(ํจ๊ณผ์ค๋)**

<br>

```css
.box{
	transition: font-size 1000ms ease-out, background-color: 2000ms cubic-bazier
	(0.08,0.57,0.97,-0.78) 1000ms;
}
```

* transition : property duration timingfunction delay
* property : ๋ชจ๋ ์์ฑ ๋๋ ์ผ๋ถ ์์ฑ์ ์ ๋๋ฉ์ด์ ์ ์ฉ
* duration : ์๋์๊ฐ, ์์ํด์ ๋๋ ๋๊น์ง ์๊ฐ, ์ด๋จ์๋ก ์ง์ (ms , s)
* timingfunction : ๊ฐ์๋ , ์๋ต ๊ฐ๋ฅ
    * ease , linear ๊ธธ์ด์ฆ๊ฐ , ease-in ๊ฐ์, ease-out ๊ฐ์, ease-in-out, cubic-beizer ๋ฒ ์ด์ง์ด๊ณก์  ์ค ์ ํ
* delay : ์๋ ฅ ์๊ฐ๋งํผ ์ง๋ ํ ์๋, ์๋ต ๊ฐ๋ฅ
* ํ๊ฐ์ด์์ ์์์ ๊ฐ๊ฐ ํจ๊ณผ๋ฅผ ์ฃผ๊ณ  ์ถ๋ค๋ฉด , ์ผํ๋ก ๊ตฌ๋ถํ์ฌ ์ฌ์ฉ ๊ฐ๋ฅ 

<br>

## transform
์์๋ฅผ 2์ฐจ์, 3์ฐจ์ ๊ณต๊ฐ์์ ๋ณํํ  ์ ์๋๋ก ํด์ค๋ค.

<br>

### rotate(Ndeg)
* ์์๋ฅผ ํ์ ํ ๋ ์ฌ์ฉ(์๊ณ๋ฐฉํฅ)
* rotate(x,y) | rotateX() | ratateY()
* ์ฃผ๋ณ์ ์ํฅ ์์ค

<br>

### scale(N)
* ์์ ์ ํฌ๊ธฐ๋ฅผ ์กฐ์ ํ  ๋ ์ฌ์ฉ
* scale(x,y) | scaleX() | scaleY()
* ์ฃผ๋ณ์ ์ํฅ ์์ค

<br>

### translate(x,y)
* ์์๋ฅผ ์ํ๋ ์์น์ ์ฎ๊ธธ๋ ์ฌ์ฉ
* translate(x,y) | translateX | translateY
* ๋จ์๋ฅผ ์ฌ์ฉํ ๋ px, %(์์ ์ํฌ๊ธฐ ๊ธฐ์ค)์ ์ฌ์ฉ
* ์ฃผ๋ณ์ ์ํฅ ์์ค

<br>

transform-origin
* ์ค์ฌ์ถ
* top , bottom, center, left, right ์ฌ์ฉ

perspective
* ์๋ค๋ก ์ด๋
* ๋ถ๋ชจ์์๊ฐ ์๋ค๊ณต๊ฐ ๋ง๋ จ(3D)

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
* animation : name ์๋์๊ฐ ๊ฐ์๋ ๋๋ ์ด์๊ฐ ๋ฐ๋ณตํ์ ๋ฐฉํฅ
* ๋ค๋ฅธ๊ฑด transition๊ณผ ๊ฐ์
* animation-iteration-count : ๋ฐ๋ณตํ์ ํ์์ง์ (์ ์) / infinite ๋ฌดํ๋ฐ๋ณต
* animation-direction : ๋ฐฉํฅ normal / alternate(์๋ณต) / reverse
* animation-fill-mode : ์ ๋๋ฉ์ด์์ด ์์๋๊ธฐ ์ ์ด๋ ๋๋๊ณ  ๋ ํ ํจ๊ณผ 
    * forward / backward / both / none
* animarion-play-state : ์ ๋๋ฉ์ด์์ ์คํ ์ํ๋ฅผ ์ค์  paused
* animation-steps() : ์ ๋๋ฉ์ด์ ๋์ ์ง์  steps(10)

