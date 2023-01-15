# callback
📌 [드림코딩 유튜브](https://youtu.be/s1vpVCrT8f4)

<br>

### 동기와 비동기

* 자바스크립트는 동기적
* hoisting이 된 이후 부터 작성한 순서에 맞춰 하나씩 실행된다는 것
* hoisting? var, function declaration(함수선언) 같은 선언들이 제일 위로 올라가는것
* synchronous(동기)는 정해진 순서에 맞게 코드가 실행되는것이고 asynchronous는 비동기적으로 언제코드가 실행될지 예측할 수 없는것

<br>

```js
console.log(1);
console.log(2);
console.log(3);
```
* 자바스크립트 엔진은 코드를 제일 위에서 부터 밑으로 실행하기 때문에 순서대로 작동된다. 

<br>

```js
console.log(1);
setTimeout(() => console.log(2),1000);
console.log(3);
```
* 하지만 이렇게 setTimeout을 콜백해서 사용한다면? 1,3,2 이렇게 출력될것
* 브라우저에 요청하고 브라우저가 응답을 하면 그때 실행되기 때문이다. 이것이 비동기 이다. 

<br>

### callbalk 마지막정리
* 콜백은 항상 비동기 일때만 쓰일까? ❌ 콜백도 두가지로 나뉜다.

<br>

* Synchronous callback
```js
function printImmediately(print) {
    print();
}
printImmediately(()=> console.log('hello'))
```

<br>

* Asynchronous callback
```js
function printWithDelay(print, timeout) {
    setTimeout(print, timeout);
}
printWithDelay(() => console.log('async callbalk'), 2000);
```
* 자바스크립트는 함수를 이렇게 콜백형태 인자로 다른함수에 전달 할 수도 있고 변수에 할당할 수도 있는 언어이다.
* 언어들마다 콜백을 지원하는 방식이 다르다. 

<br>

### callback체인의 문제점
* 가독성이 떨어진다.
* 에러가 발생하거나 디버깅을 해야할 때 어려움이 있다.
* 유지보수가 어렵다.

<br>

# Promise
* 자바스크립트에서 제공하는 비동기를 간편하게 처리할수있도록 도와주는 오브젝트

* 정해진 장시간의 기능을 수행하고 나서 정상적으로 기능이 수행됐다면 성공의 메세지와 함께 처리 된 결과 값을 전달해주고 만약 기능을 수행하다가 예상치 못한 문제가 발생했다면 에러를 전달해 준다.

<br>

**어떻게 callbbalck을 사용하지 않고 promise를 통해 비동기 코드를 깔끔하게 처리할 수 있을까?**
* promise는 자바스크립트 안에 내장되어 있는 오브젝트 이며 비동기적인 수행할 때 콜백함수 대신에 유용하게 사용하는 오브젝트이다. 
* state(상태): pending -> fulfilled or rejected 
* Producer vs Consumer 

<br>
​

### promise 만들기

<br>

​Producer
* 새로운 promise가 만들어 질때는 우리가 전달한 executor 함수가 자동적으로 바로 실행된다.
```js
const promise = new Promise((resolve, reject) => {
    console.log('doing something...');
    setTimeout(() =>{
        //resolve('ellie');
        reject(new('no network...'));
    },2000);
});
```
* Promise 생성자를 보면 executor라는 콜백함수를 전달해줘야 하는데 이 콜백함수에는 두가지의 콜백함수를 받는다. 성공할땐 resolve / reject을 수행하다가 중간에 문제가 생기면 호출하게 됨
* 보통 무거운일을 하게 되면 시간이 꽤 걸리는데 그걸 동기적으로 처리하게 되면 다음 라인에 있는 걸 수행하기에는 시간이 걸리기 때문에 Promise를 사용해 비동기적으로 하는게 좋다. 
* promise를 만드는 순간 우리가 전달한 함수가 바로 실행되기 때문에 유의할 점이 있다. ☞ 예를들어 네트워크 요청을 사용자가 요구 했을 때만 해야되는 상황인데 이런식이라면 사용자가 요구하지 않아도 불필요한 네트워크 통신이 일어날 수 있다. 

<br>

### promise 사용하기
* Consumers: then, catch, finally 
```js
promise
    .then(value => { // 성공한값
        console.log(value);
    })
    .catch(error => { // 실패한값 
        console.log(error);
    })
    .finally(() => { // 성공하든 실패하는 상관없이 어떤기능을 마지막에 수행하는것 
        console.log('finally');
    });
```

<br>

### promise 연결하기(체이닝)
```js
const fetchNumber = new Promise((resolve, reject) => {
    setTimeout(() => resolve(1), 1000);
});

fetchNumber
.then(num => num*2)
.then(num => num*3)
.then(num => {
    return new Promise((resolve,reject) => {
        setTimeout(() => resolve(num-1),1000);
    });
})
.then(num => console.log(num));
```
* then은 바로 값을 전달할 수도 있고 promise를 전달해도 된다.

<br>

### Error Handling
```js
const getHen = () =>
    new Promise((resolve,reject) => {
        setTimeout(() => resolve('🐔'), 1000);
    });
const getEgg = hen =>
    new Promise((resolve,reject) => {
        // setTimeout(() => resolve(`${hen} => 🥚`), 1000);
        setTimeout(() => reject(new Error(`error! ${hen} => 🥚`)), 1000);
    });
const cook = egg =>
    new Promise((resolve,reject) => {
        setTimeout(() => resolve(`${egg} => 🍳`), 1000);
    });

getHen()
.then(getEgg)
.catch(error => {
    return '🥖';
})
.then(cook)
.then(console.log)
.catch(console.log);
```
* 에러를 처리하고 싶을때 그 다음에 바로 캐치를 써서 해결할 수 있다. 

<br>

# async & await
### async
무언가 오래걸리는 코드를 비동기적인 처리를 하지 않으면 자바스크립트 엔진은 한줄이 끝나야 그 다음줄로 넘어가는 동기적인 처리를 하기 때문에 오래걸린다. 이것을 빠르게 하기 위해 비동적으로 promise를 사용한것인데 promise를 사용하지 않고 간편하게 비동기를 작성할 수 있는 방법이 async이다. 함수앞에 async를 써주면 사용할 수 있다.

<br>

```js
// Promise사용
function fetchUser(){
    return new Promise((resolve, reject) => { 
        //do network reqeust in 10 secs... 
        resolve('ellie'); 
    });
}

const user = fetchUser();
console.log(user);

// async 사용
async function fetchUser(){
    //do network reqeust in 10 secs... 
    return 'ellie';
}
```

<br>

###  await
await라는 키워드는 async가 붙은 함수 안에서만 사용할 수 있다. 

<br>

``` js
function delay(ms) {
    return new Promise(resolve => setTimeout(resolve, ms));
}

async function getApple() {
    await delay(2000);
    return '🍎';
}

async function getBanana() {
    await delay(1000);
    return '🍌';
}

async function pickFruits() {
    const apple = await getApple();
    const banana = await getBanana();
    return `${apple} + ${banana}`;
}

pickFruits().then(console.log)
```

<br>

### await 병렬처리
보통 순차적으로 코드를 진행하게 되면 서로 연관되지 않는 것은 순차적일 필요가 없음에도 순차적으로 느리게 작동하는데 그럴필요없이 병렬적으로 동시에 출력하게 만드는 방법이 있다. 

​<br>

### 유용한 promise APIs
```js
function pickAllFruits(){
    return Promise.all([getApple(),getBanana()])
    .then(fruits => fruits.join('+'));
}
pickAllFruits().then(console.log);

function pickOnlyOne() {
    return Promise.race([getApple(),getBanana()]);
}
pickOnlyOne().then(console.log);
```
* all : promise 배열을 전달하게 되면 모든 promise들이 병렬적으로 다 받을 때까지 모아주는 것

* race : 배열에 전달된 promise 중에서 가장 먼저 값을 리턴하는 값만 전달이 된다. 
