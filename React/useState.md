# 상태관리하기

📌 [별코딩 | 리액트 훅스 시리즈](https://youtu.be/G3qglTF-fFI)


📌 [한입 크기로 잘라 먹는 리액트(React.js)](https://www.inflearn.com/course/%ED%95%9C%EC%9E%85-%EB%A6%AC%EC%95%A1%ED%8A%B8)


<br>

```js
// 하나의 상태값을 관리할 때
const [state, setState] = useState(초기값);

// 여러개의 상태값을 관리할 때 
const [state, setState] = useState({
	// name : 기본값
    author: '',
    content: '',
});
```

<br>

* state란? 컴포넌트의 상태
* 현재 상태값은 state라는 변수에 들어있고 state를    변경시켜주고 싶을 때는 setState라는 변수를 이용해서 변경시켜줄수 있다.
* setState로 값이 변경될 때마다 렌더링 된다. 
* 전달되는 props가 있으면 그 props가 변경되거나 내부에서 가지고 있는 useState에 있는 상태가 변경되면 (호출할때) 내부상태가 변경될 때 마다 리액트는 변경된 해당 컴포넌트 전체를 다시 호출한다. vdom 때문에 변경된 부분만 업데이트 됨. 






