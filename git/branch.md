# 브랜치(branch)란?

📌 모두의 깃& 깃허브

<br>

버전을 여러흐름으로 나누어 관리하는 방법 

<br>



**버전을 나누어 관리하는건 쉽게 3단계로 관리할 수 있다.**

1. 브랜치를 나눈다.
2. 각자의 브랜치에서 작업한다.
3. (필요한 경우) 나눈 브랜치를 합친다.

<br>

**버전을 나누어 관리하는 이유는 무엇일까?**

예를들어 여러명의 개발자가 협업을 할 때 각자 다른 기능을 구현한다고 하면 하나의 브랜치를 통째로 복사해 그곳에서 각각의 기능을 구현하면 다시 합쳐야 할 때 하나하나 비교해야되는 어려움이 있다. 따라서 브랜치를 나누어 각각의 기능을 구현하고 다시 합치면 같은 코드를 다르게 수정한 부분만 살펴 보면 되는 것이다.

<br>

### 브랜치 나누기 

- master 브랜치 : 깃이 제공하는 가장 기본적인, 최초의 브랜치
- HEAD : 현재 작업 중인 브랜치의 최신 커밋을 가리키는 표시
- 체크아웃 : 특정 브랜치에서 작업할 수 있도록 작업 환경을 바꾸는 것
- 브랜치를 나누고 합치는 과정에서 체크아웃을 통해 HEAD의 위치를 바꿀 수 있음

<br>

### 브랜치 병합하기

- merge : 나뉜 브랜치를 하나로 통합하는 것

<br>

**브랜치 이름을 마음대로 지어도 될까?**

- 깃을 연습할 때는 브랜치 이름을 임의로 지어도 되지만 실무에서는 브랜치 이름을 암묵적으로 정해두는 경우가 많다.
- 목적에 따라 브랜치 이름을 관리하면 무엇을 위해 만들어진 브랜치 인지 알 수 있다.

<br>

브랜치를 병합하는 과정에서 충돌이 난다면?

- 충돌이란 병합하려는 두 브랜치가 서로 같은 내용을 다르게 수정항 상황을 말한다.
- 충돌이 발생하면 깃이 자동으로 해결해 주지 않는다.
- 어떤 브랜치 내용을 사용할 지 정해서 선택해서 충돌을 해결하면 된다.

<br>

충돌이 발생 했을 때 대처법(정리)

1. 충돌을 해결한다.(어떤 브랜치의 내용을 반영할지 직접 선택한다)
2. 다시 커밋한다. 

<br>

### 브랜치 재배치하기

- rebase : 브랜치가 뻗어나온 기준점을 변경하는 것