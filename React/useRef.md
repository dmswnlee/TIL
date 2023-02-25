# DOM 요소 접근하기 

📌 [별코딩 | 리액트 훅스 시리즈](https://youtu.be/G3qglTF-fFI)


📌 [한입 크기로 잘라 먹는 리액트(React.js)](https://www.inflearn.com/course/%ED%95%9C%EC%9E%85-%EB%A6%AC%EC%95%A1%ED%8A%B8)


<br>

```js
const ref= useRef(value)
{current : value}
```

<br>

- 함수형 컴포넌트에서 useRef를 부르면 `ref`를 반환해준다.
- 우리가 정해준 초기값은 ref안에 current값에 저장된다.
- 오브젝트는 수정이 가능하기 때문에 언제든 우리가 원하는값으로 변경해줄 수 있다.
- 반환된 ref는 컴포넌트의 전 생애주기를 통해 유지가 된다. 즉 컴포넌트가 계속 렌더링 되어도 언마운트 되기 전까지는 값을 유지할 수 있다.

<br>

### useRef 는 언제 사용이 될까?

```js
const [count, setCount] = useState(0);
const countRef = useRef(0);

const increaseCountState = () => {
    setCount(count + 1);
};

const increaseCountRef = ()=> {
    countRef.current = countRef.current + 1;
    console.log('Ref:', countRef.current);
}

return (
    <div>
        <p>state:{count}</p>
        <p>Ref : {countRef.current}</p>
        <button onClick={increaseCountState}>State 올려</button>
        <button onClick={increaseCountRef}>Ref 올려</button>
    </div>
);
```

<br>

1. 저장공간

- state와 비슷하게 어떤 값을 저장하는 저장공간으로 사용된다.
- state의 변화 → 렌더링 → 컴포넌트 내부변수들 초기화  
- 이런경우 우리가 원치않은 렌더링 때문에 곤란해질때가 있다.

<br>

```js
const authorInput = useRef();

const handleSubmit = () => {
  if (state.author.length < 1) {
    authorInput.current.focus();
    return;
  }
  alert("저장 성공!");
};

<input ref={authorInput} value={state.author} onChange={handleChangeState}
name="author" placeholder="작성자" type="text" />
```

<br>

2.DOM 요소에 접근

- 자바스크립트에서 `document.querySelector()` 를 생각하면 된다.

<br>

### state 대신 ref에 저장한다면 어떤 장점이 있을까?

- 예를들어 state 버튼과 ref 버튼이 있다 둘다 클릭하면 숫자가 하나씩 증가하는 형태인데 이때 state 버튼을 클릭하면 렌더링 되면서 화면의 값이 바뀌는데 ref 버튼을 클릭하면 아무런 변화가 일어나지 않는다. 이때 state 버튼을 클릭하여 화면을 렌더링 해주면 ref 버튼을 클릭했을 때 만큼의 숫자가 업데이트 되어있다. 즉 ref는 내부적으로는 변화값을 저장하지만 렌더링이 되지 않아 화면에는 보이지 않는 것.
- Ref의 변화 → No 렌더링 → 변수들의 값이 유지됨 ☞ 불필요한 렌더링을 막을 수 있다.
- state의 변화 → 렌더링 → state값은 업데이트  Ref의 값은 그대로 유지됨
- 컴포넌트가 아무리 렌더링이 되어도 Ref 안에 저장되어 있는 값은 바뀌지 않고 그대로 유지가 된다.
- 변경시 렌더링을 발생시키지 말아야하는 값을 다룰때 편리

<br>

***변수를 쓰지 않고 굳이 ref를 사용하는 이유는?***

변수와 ref는 동시에 렌더링 시키면 값을 기억하고 있는 ref는 렌더이전의 값을 그대로 화면에 나타내주고 변수는 초기화 되어 처음값 그대로 화면에 표시된다.

<br>

즉, 변화는 감지하지만 그 변화가 렌더링을 발생시키면 안되는 값을 다룰때 편리하다.






