# 데이터 관리하기

📌 [별코딩 | 리액트 훅스 시리즈](https://youtu.be/G3qglTF-fFI)


📌 [한입 크기로 잘라 먹는 리액트(React.js)](https://www.inflearn.com/course/%ED%95%9C%EC%9E%85-%EB%A6%AC%EC%95%A1%ED%8A%B8)


<br>

## context API
- 컴포넌트를 만들다 보면 Props drilling 이라는 불필요한 props 전달이 일어나는 경우가 있음
- 단방향으로만 전달되는 리액트 컴포넌트의 단점이라고 할 수 있음
- 이러한 Props drilling은 코드작성과 수정에 번거로움이 생김 이걸 해결하기 위해 Context 생김
- 하나의 파일에 여러개의 context 생성가능

<br>

```js
//context 생성
const MyContext = React.createContext(defaultValue);

//context Provider를 통한 데이터 공급
<MyContext.Provider value={전역으로 전달하고자하는 값}>
	{/*이 context안에 위치할 자식 컴포넌트들*/}
</MyContext.Provider>
```

- props 대신 context를 사용하면 최상위 컴포넌트가 선언하면 필요한 컴포넌트에서 받아오기만 하면 된다.
- 이때 받아오는 컴포넌트는 useContext를 사용하면 된다.

<br>

**그럼 context API를 사용하면 되니까 Props는 필요 없는거 아닌가요?**

<br>

- context는 꼭 필요할때만!
- context를 사용하면 컴포넌트를 재사용하기 어려워 질 수 있다
- context의 주된 목적은 다양한 레벨에 있는 많은 컴포넌트들에게 전역적인 데이터를 전달하기 위해서 이다.
- 단지 Prop drilling을 피하기 위한 목적이라면 Component Composition(컴포넌트 합성)을 먼저 고려해보자.

<br>

### useContext

<br>

사용예시 

```js
import React, { useContext } from "react";
import { Context } from "./App";

const DiaryEditor = () => {
    const { onAdd } = useContext(Context);
    ...
    const handleClick = () => {
    ...
    onAdd(person.name, person.age, person.job);
    };
}
```

<br>

## useReducer
- 복잡한 상태변화 로직을 컴포넌트에서 분리하자
- useState 처럼 리액트의 상태관리를 돕는 도구
- 복잡한 코드를 깔끔하게 정리할 수 있어서 유지보수에 좋음
- Readucer / Dispatch / Action 으로 이루어져 있다.

<br>

- reducer : state를 업데이트 하는 역할
- dispatch : state 업데이트를 위한 요구
- action : 요구의 내용

<br>

```js
import React, { useReducer, useState } from 'react';

const ACTION_TYPES = {
   deposit: 'deposit',
   withdraw: 'withdraw',
}

const reducer = (state, action) => {
   switch (action.type){
      case ACTION_TYPES.deposit : 
         return state + action.payload;
      case ACTION_TYPES.withdraw :
         return state - action.payload;
      default:
         return state;
   }
};


function App() { 
   const [number, setNumber] = useState(0); 
   const [money, dispatch] = useReducer(reducer, 0);

   return (
      <div>
         <h2>useReducer 은행에 오신것을 환영합니다.</h2>
         <p>잔고: {money}원</p>
         <input 
            type='number'
            value={number}
            onChange={(e) => setNumber(parseInt(e.target.value))}
            step='1000'
         />
         <button onClick={() => {
            dispatch({type: ACTION_TYPES.deposit, payload: number});
         }}>예금</button>
         <button onClick={() => {
            dispatch({type: ACTION_TYPES.withdraw, payload: number});
         }}>출금</button>
      </div>
   );
}

export default App;
```

- dispatch에 action을 전달할 때 그안에는 보통 {} 객체 형태로 전달하고 type을 적어준다.
- type 안에는 요구를 적어준다. 
- reducer가 리턴하는 값이 새로 업데이트되는 값이다. 
- 보통 reducer 안에는 if..else문, switch..case문을 사용한다. 
- reducer의 장점은 전달받은 action 대로만 state를 업데이트 시켜준다. 










