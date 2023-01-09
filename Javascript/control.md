# 제어문(control flow statement)

## 조건문(conditional statement)
주어진 조건식이 참인 경우 코드블록을 실행

<br>

### if문, if...else문 

```js
if(조건) {
    //조건이 참이면 실행
}

if(조건) {
    //조건이 참이면 실행
} else {
    //조건이 거짓이면 실행
}

if(조건1) {
    //조건1이 참이면 실행
} else if(조건2) {
    //조건2가 참이면 실행
} else {
    //조건이 거짓이면 실행
}
```
* 이떄 삼항조건 연산자를 사용하면 간단하게 할 수 있다.

<br>

### switch문

```js
switch (표현식) {
    case 표현식1:
         실행문;
         break;
    case 표현식2;  
         실행문;
         break;
    default:
         실행문;
}
```
* break를 꼭 사용해야 함
* 모든 조건을 만족하지 않을 떄 default 사용 

<br>

## 반복문(Loop statement)
주어진 조건이 참인 경우 코드블럭 실행, 조건이 거짓이 될때 까지 반복

<br>

### for문
```js
for(변수선언문; 조건식; 증감식) {
    실행문
}

for(변수선언문; 조건식; 증감식) {
    for(변수선언문; 조건식; 증감식){
        실행문
    }
    실행문
}
```
* 어떤식도 선언하지 않으면 무한루프에 빠지는데 무한루프에 빠지지 않게 해야함
* 중첩for문 사용 가능

<br>

### while문
```js
while(조건식) {
    실행문
}
```
* 조건식이 참이면 코드블록 반복실행
* 조건식이 거짓이 되면 코드블록 종료 
* 조건식이 항상 참이면 무한루프에 빠지니 주의!

<br>

### do..while문
```js
do{
    실행문
} while(조건식){
    실행문
}
```
* 먼저 코드블록을 실행한 후 조건에 따라 코드블록을 실행
* 코드블록이 무조건 한번 이상 실행됨

<br>

### break문
* 코드블록을 탈출하는 문
* break문을 사용하면 해당조건을 실행한후 다음 조건으로 안넘어가고 빠져나올 수 있음

### continue문
* 반복문에서 continue를 사용하면 그 자리에서 중단하고 반복문의 증감식으로 이동해 조건을 실행함
* continue 밑에 있는 실행문을 무시함 

