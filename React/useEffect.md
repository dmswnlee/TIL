# 컴포넌트 생애주기

📌 [별코딩 | 리액트 훅스 시리즈](https://youtu.be/G3qglTF-fFI)


📌 [한입 크기로 잘라 먹는 리액트(React.js)](https://www.inflearn.com/course/%ED%95%9C%EC%9E%85-%EB%A6%AC%EC%95%A1%ED%8A%B8)


<br>

### Lifecycle 이란?
React 컴포넌트의 생애주기(생명주기)

<br>

- Mount (화면에 나타나는 것) → Update(업데이트, 리렌더) → UnMount(화면에서 사라짐)
- 마운트, 업데이트, 언마운트 될 때 각 작업을 수행하는 걸 React Lifecycle를 제어한다고 할 수 있다.

<br>

```js
//렌더링 될때마다 매번 실행됨
useEffect(() => {
    console.log('렌더링 🤞');
});

// 마운팅 + count가 변화할때마다 실행됨
useEffect(() => {
    console.log('🍎count 변화');
}, [count]);

// 맨 처음에만 렌더링될때만 실행됨 
useEffect(() => {
    console.log('마운팅🐇');
}, []);

// 언마운트 될때 실행 -> return 으로 콜백함수를 전달하면 됨
useEffect(() => {
	//구독
  console.log("Sub Component Mount");
  return () => {
		//구독해지
    console.log("Sub Component Unmount");
  };
}, []);
```

<br>

- 어떤 컴포넌트가 Mount(화면에 첫 렌더링) → Update(다시렌더링) → Unmount(화면에서 사라질때) 되었을 때 특정작업을 처리할 코드를 실행시켜주고 싶다면 사용
- 인자로 콜백함수를 받는다. (콜백함수란 다른함수의 인자로 전달된 함수를 의미)
- 콜백함수 내부에 우리가 원하는 작업을 처리할 코드를 작성해주면 된다.
- 두번째 인자로 배열을 받을때 이 배열을 의존성배열(Dependency array) 이라고 함
- 매번 렌더링될 때마다 실행되는게 아니라 컴포넌트가 맨 처음 화면에 렌더링이 될 때 **배열안에 들어있는 요소의 값이 바뀔때만** 실행
- 빈배열을 전달해주면 컴포넌트가 맨 처음 렌더링 될때만 실행
- 예를들어 구독을 하고 구독을 해지해주는 작업을 clean up 작업이라고 하는데 return 값 안에 실행시켜줄 작업을 넣어주면 됨
- 구독을 누르면 마운트, 다시 눌러서 구독해지가 되면 언마운트
- 결론적으로 useEffect를 사용하면 마운트, 업데이트, 언마운트 또는 어떤 특정값의 변화를 추적할 수 있는 여러가지 Lifecycle 제어를 할 수 있음!






