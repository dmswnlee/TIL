# callback
๐ [๋๋ฆผ์ฝ๋ฉ ์ ํ๋ธ](https://youtu.be/s1vpVCrT8f4)

<br>

### ๋๊ธฐ์ ๋น๋๊ธฐ

* ์๋ฐ์คํฌ๋ฆฝํธ๋ ๋๊ธฐ์ 
* hoisting์ด ๋ ์ดํ ๋ถํฐ ์์ฑํ ์์์ ๋ง์ถฐ ํ๋์ฉ ์คํ๋๋ค๋ ๊ฒ
* hoisting? var, function declaration(ํจ์์ ์ธ) ๊ฐ์ ์ ์ธ๋ค์ด ์ ์ผ ์๋ก ์ฌ๋ผ๊ฐ๋๊ฒ
* synchronous(๋๊ธฐ)๋ ์ ํด์ง ์์์ ๋ง๊ฒ ์ฝ๋๊ฐ ์คํ๋๋๊ฒ์ด๊ณ  asynchronous๋ ๋น๋๊ธฐ์ ์ผ๋ก ์ธ์ ์ฝ๋๊ฐ ์คํ๋ ์ง ์์ธกํ  ์ ์๋๊ฒ

<br>

```js
console.log(1);
console.log(2);
console.log(3);
```
* ์๋ฐ์คํฌ๋ฆฝํธ ์์ง์ ์ฝ๋๋ฅผ ์ ์ผ ์์์ ๋ถํฐ ๋ฐ์ผ๋ก ์คํํ๊ธฐ ๋๋ฌธ์ ์์๋๋ก ์๋๋๋ค. 

<br>

```js
console.log(1);
setTimeout(() => console.log(2),1000);
console.log(3);
```
* ํ์ง๋ง ์ด๋ ๊ฒ setTimeout์ ์ฝ๋ฐฑํด์ ์ฌ์ฉํ๋ค๋ฉด? 1,3,2 ์ด๋ ๊ฒ ์ถ๋ ฅ๋ ๊ฒ
* ๋ธ๋ผ์ฐ์ ์ ์์ฒญํ๊ณ  ๋ธ๋ผ์ฐ์ ๊ฐ ์๋ต์ ํ๋ฉด ๊ทธ๋ ์คํ๋๊ธฐ ๋๋ฌธ์ด๋ค. ์ด๊ฒ์ด ๋น๋๊ธฐ ์ด๋ค. 

<br>

### callbalk ๋ง์ง๋ง์ ๋ฆฌ
* ์ฝ๋ฐฑ์ ํญ์ ๋น๋๊ธฐ ์ผ๋๋ง ์ฐ์ผ๊น? โ ์ฝ๋ฐฑ๋ ๋๊ฐ์ง๋ก ๋๋๋ค.

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
* ์๋ฐ์คํฌ๋ฆฝํธ๋ ํจ์๋ฅผ ์ด๋ ๊ฒ ์ฝ๋ฐฑํํ ์ธ์๋ก ๋ค๋ฅธํจ์์ ์ ๋ฌ ํ  ์๋ ์๊ณ  ๋ณ์์ ํ ๋นํ  ์๋ ์๋ ์ธ์ด์ด๋ค.
* ์ธ์ด๋ค๋ง๋ค ์ฝ๋ฐฑ์ ์ง์ํ๋ ๋ฐฉ์์ด ๋ค๋ฅด๋ค. 

<br>

### callback์ฒด์ธ์ ๋ฌธ์ ์ 
* ๊ฐ๋์ฑ์ด ๋จ์ด์ง๋ค.
* ์๋ฌ๊ฐ ๋ฐ์ํ๊ฑฐ๋ ๋๋ฒ๊น์ ํด์ผํ  ๋ ์ด๋ ค์์ด ์๋ค.
* ์ ์ง๋ณด์๊ฐ ์ด๋ ต๋ค.

<br>

# Promise
* ์๋ฐ์คํฌ๋ฆฝํธ์์ ์ ๊ณตํ๋ ๋น๋๊ธฐ๋ฅผ ๊ฐํธํ๊ฒ ์ฒ๋ฆฌํ ์์๋๋ก ๋์์ฃผ๋ ์ค๋ธ์ ํธ

* ์ ํด์ง ์ฅ์๊ฐ์ ๊ธฐ๋ฅ์ ์ํํ๊ณ  ๋์ ์ ์์ ์ผ๋ก ๊ธฐ๋ฅ์ด ์ํ๋๋ค๋ฉด ์ฑ๊ณต์ ๋ฉ์ธ์ง์ ํจ๊ป ์ฒ๋ฆฌ ๋ ๊ฒฐ๊ณผ ๊ฐ์ ์ ๋ฌํด์ฃผ๊ณ  ๋ง์ฝ ๊ธฐ๋ฅ์ ์ํํ๋ค๊ฐ ์์์น ๋ชปํ ๋ฌธ์ ๊ฐ ๋ฐ์ํ๋ค๋ฉด ์๋ฌ๋ฅผ ์ ๋ฌํด ์ค๋ค.

<br>

**์ด๋ป๊ฒ callbbalck์ ์ฌ์ฉํ์ง ์๊ณ  promise๋ฅผ ํตํด ๋น๋๊ธฐ ์ฝ๋๋ฅผ ๊น๋ํ๊ฒ ์ฒ๋ฆฌํ  ์ ์์๊น?**
* promise๋ ์๋ฐ์คํฌ๋ฆฝํธ ์์ ๋ด์ฅ๋์ด ์๋ ์ค๋ธ์ ํธ ์ด๋ฉฐ ๋น๋๊ธฐ์ ์ธ ์ํํ  ๋ ์ฝ๋ฐฑํจ์ ๋์ ์ ์ ์ฉํ๊ฒ ์ฌ์ฉํ๋ ์ค๋ธ์ ํธ์ด๋ค. 
* state(์ํ): pending -> fulfilled or rejected 
* Producer vs Consumer 

<br>
โ

### promise ๋ง๋ค๊ธฐ

<br>

โProducer
* ์๋ก์ด promise๊ฐ ๋ง๋ค์ด ์ง๋๋ ์ฐ๋ฆฌ๊ฐ ์ ๋ฌํ executor ํจ์๊ฐ ์๋์ ์ผ๋ก ๋ฐ๋ก ์คํ๋๋ค.
```js
const promise = new Promise((resolve, reject) => {
    console.log('doing something...');
    setTimeout(() =>{
        //resolve('ellie');
        reject(new('no network...'));
    },2000);
});
```
* Promise ์์ฑ์๋ฅผ ๋ณด๋ฉด executor๋ผ๋ ์ฝ๋ฐฑํจ์๋ฅผ ์ ๋ฌํด์ค์ผ ํ๋๋ฐ ์ด ์ฝ๋ฐฑํจ์์๋ ๋๊ฐ์ง์ ์ฝ๋ฐฑํจ์๋ฅผ ๋ฐ๋๋ค. ์ฑ๊ณตํ ๋ resolve / reject์ ์ํํ๋ค๊ฐ ์ค๊ฐ์ ๋ฌธ์ ๊ฐ ์๊ธฐ๋ฉด ํธ์ถํ๊ฒ ๋จ
* ๋ณดํต ๋ฌด๊ฑฐ์ด์ผ์ ํ๊ฒ ๋๋ฉด ์๊ฐ์ด ๊ฝค ๊ฑธ๋ฆฌ๋๋ฐ ๊ทธ๊ฑธ ๋๊ธฐ์ ์ผ๋ก ์ฒ๋ฆฌํ๊ฒ ๋๋ฉด ๋ค์ ๋ผ์ธ์ ์๋ ๊ฑธ ์ํํ๊ธฐ์๋ ์๊ฐ์ด ๊ฑธ๋ฆฌ๊ธฐ ๋๋ฌธ์ Promise๋ฅผ ์ฌ์ฉํด ๋น๋๊ธฐ์ ์ผ๋ก ํ๋๊ฒ ์ข๋ค. 
* promise๋ฅผ ๋ง๋๋ ์๊ฐ ์ฐ๋ฆฌ๊ฐ ์ ๋ฌํ ํจ์๊ฐ ๋ฐ๋ก ์คํ๋๊ธฐ ๋๋ฌธ์ ์ ์ํ  ์ ์ด ์๋ค. โ ์๋ฅผ๋ค์ด ๋คํธ์ํฌ ์์ฒญ์ ์ฌ์ฉ์๊ฐ ์๊ตฌ ํ์ ๋๋ง ํด์ผ๋๋ ์ํฉ์ธ๋ฐ ์ด๋ฐ์์ด๋ผ๋ฉด ์ฌ์ฉ์๊ฐ ์๊ตฌํ์ง ์์๋ ๋ถํ์ํ ๋คํธ์ํฌ ํต์ ์ด ์ผ์ด๋  ์ ์๋ค. 

<br>

### promise ์ฌ์ฉํ๊ธฐ
* Consumers: then, catch, finally 
```js
promise
    .then(value => { // ์ฑ๊ณตํ๊ฐ
        console.log(value);
    })
    .catch(error => { // ์คํจํ๊ฐ 
        console.log(error);
    })
    .finally(() => { // ์ฑ๊ณตํ๋  ์คํจํ๋ ์๊ด์์ด ์ด๋ค๊ธฐ๋ฅ์ ๋ง์ง๋ง์ ์ํํ๋๊ฒ 
        console.log('finally');
    });
```

<br>

### promise ์ฐ๊ฒฐํ๊ธฐ(์ฒด์ด๋)
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
* then์ ๋ฐ๋ก ๊ฐ์ ์ ๋ฌํ  ์๋ ์๊ณ  promise๋ฅผ ์ ๋ฌํด๋ ๋๋ค.

<br>

### Error Handling
```js
const getHen = () =>
    new Promise((resolve,reject) => {
        setTimeout(() => resolve('๐'), 1000);
    });
const getEgg = hen =>
    new Promise((resolve,reject) => {
        // setTimeout(() => resolve(`${hen} => ๐ฅ`), 1000);
        setTimeout(() => reject(new Error(`error! ${hen} => ๐ฅ`)), 1000);
    });
const cook = egg =>
    new Promise((resolve,reject) => {
        setTimeout(() => resolve(`${egg} => ๐ณ`), 1000);
    });

getHen()
.then(getEgg)
.catch(error => {
    return '๐ฅ';
})
.then(cook)
.then(console.log)
.catch(console.log);
```
* ์๋ฌ๋ฅผ ์ฒ๋ฆฌํ๊ณ  ์ถ์๋ ๊ทธ ๋ค์์ ๋ฐ๋ก ์บ์น๋ฅผ ์จ์ ํด๊ฒฐํ  ์ ์๋ค. 

<br>

# async & await
### async
๋ฌด์ธ๊ฐ ์ค๋๊ฑธ๋ฆฌ๋ ์ฝ๋๋ฅผ ๋น๋๊ธฐ์ ์ธ ์ฒ๋ฆฌ๋ฅผ ํ์ง ์์ผ๋ฉด ์๋ฐ์คํฌ๋ฆฝํธ ์์ง์ ํ์ค์ด ๋๋์ผ ๊ทธ ๋ค์์ค๋ก ๋์ด๊ฐ๋ ๋๊ธฐ์ ์ธ ์ฒ๋ฆฌ๋ฅผ ํ๊ธฐ ๋๋ฌธ์ ์ค๋๊ฑธ๋ฆฐ๋ค. ์ด๊ฒ์ ๋น ๋ฅด๊ฒ ํ๊ธฐ ์ํด ๋น๋์ ์ผ๋ก promise๋ฅผ ์ฌ์ฉํ๊ฒ์ธ๋ฐ promise๋ฅผ ์ฌ์ฉํ์ง ์๊ณ  ๊ฐํธํ๊ฒ ๋น๋๊ธฐ๋ฅผ ์์ฑํ  ์ ์๋ ๋ฐฉ๋ฒ์ด async์ด๋ค. ํจ์์์ async๋ฅผ ์จ์ฃผ๋ฉด ์ฌ์ฉํ  ์ ์๋ค.

<br>

```js
// Promise์ฌ์ฉ
function fetchUser(){
    return new Promise((resolve, reject) => { 
        //do network reqeust in 10 secs... 
        resolve('ellie'); 
    });
}

const user = fetchUser();
console.log(user);

// async ์ฌ์ฉ
async function fetchUser(){
    //do network reqeust in 10 secs... 
    return 'ellie';
}
```

<br>

###  await
await๋ผ๋ ํค์๋๋ async๊ฐ ๋ถ์ ํจ์ ์์์๋ง ์ฌ์ฉํ  ์ ์๋ค. 

<br>

``` js
function delay(ms) {
    return new Promise(resolve => setTimeout(resolve, ms));
}

async function getApple() {
    await delay(2000);
    return '๐';
}

async function getBanana() {
    await delay(1000);
    return '๐';
}

async function pickFruits() {
    const apple = await getApple();
    const banana = await getBanana();
    return `${apple} + ${banana}`;
}

pickFruits().then(console.log)
```

<br>

### await ๋ณ๋ ฌ์ฒ๋ฆฌ
๋ณดํต ์์ฐจ์ ์ผ๋ก ์ฝ๋๋ฅผ ์งํํ๊ฒ ๋๋ฉด ์๋ก ์ฐ๊ด๋์ง ์๋ ๊ฒ์ ์์ฐจ์ ์ผ ํ์๊ฐ ์์์๋ ์์ฐจ์ ์ผ๋ก ๋๋ฆฌ๊ฒ ์๋ํ๋๋ฐ ๊ทธ๋ดํ์์์ด ๋ณ๋ ฌ์ ์ผ๋ก ๋์์ ์ถ๋ ฅํ๊ฒ ๋ง๋๋ ๋ฐฉ๋ฒ์ด ์๋ค. 

โ<br>

### ์ ์ฉํ promise APIs
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
* all : promise ๋ฐฐ์ด์ ์ ๋ฌํ๊ฒ ๋๋ฉด ๋ชจ๋  promise๋ค์ด ๋ณ๋ ฌ์ ์ผ๋ก ๋ค ๋ฐ์ ๋๊น์ง ๋ชจ์์ฃผ๋ ๊ฒ

* race : ๋ฐฐ์ด์ ์ ๋ฌ๋ promise ์ค์์ ๊ฐ์ฅ ๋จผ์  ๊ฐ์ ๋ฆฌํดํ๋ ๊ฐ๋ง ์ ๋ฌ์ด ๋๋ค. 
