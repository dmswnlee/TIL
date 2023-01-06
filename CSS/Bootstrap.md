# 부트스트랩(bootstrap) 이란?

📌[bootstarp5](https://getbootstrap.com/docs/5.3/getting-started/introduction/)

<br>

* css FrameWork
* 그리드시스템을 쉽게 css로 구현할 수 있는 프레임워크 
* 반응형 웹사이트를 쉽고 빠르게 만들 수 있음
* 문서에 부트스트랩 css를 삽입하면 사용 가능

<br>

부트스트랩에는 두가지의 주요요소가 있다.
### components
* 앱에 넣어서 사용할 수 있는 다양한 조각을 모아둠(Navbar, Button....)
### grid system
* 웹사이트 레이아웃을 보조하는 시스템 
* 웹사이트의 레이아웃과 공간배치를 도와주고 화면크기에 따라 기존 공간을 재배치 하는 것을 도와줌 

<br>

### bootstrap 시작하기
1. [bootstarp5](https://getbootstrap.com/docs/5.3/getting-started/introduction/) 에 접속
2. Getting started
3. 다운로드 OR CSS,Script 링크코드 복사
4. html 문서에 링크코드 붙여넣기
5. 문서내에 입력해주면 끝!

<br>

### 레이아웃(layout)
```html
<div class="container">
  <div class="row">
    <div class="col">
    <!-- 원하는 요소 입력 -->
      Column
    </div>
  </div>
</div>
```
* ```container → row → col``` 반드시 이 구조를 지켜야 함
* 자식과 부모관계 잘 지키기
* container 전체영역 | column 한칸 | gutter 여백
* 보통 전체영역은 12칸 
* 일정한 여백을 가짐 

<br>

화면 크기마다 차지하는 칸수가 달라지게 하고 싶다면?
```html
<div class="col" col-12 col-sm-6 col-md-4 col-la-3 col-xl-3></div>
```

<br>

### 컴포넌트(components)
* Button
* Badges
    * 보통 카운트나 일종의 레이블을 보여주기 위해 사용
    * heading이나 버튼에 넣어서 사용할 수 있음
    * 프로필 등에 나타나는 일종의 알람, 업데이트 갯수 같은 것
* Button group
    * 여러 개의 버튼을 하나의 그룹으로 묶는 기능
    * 라디오 버튼을 대체하는 선택지를 만들 때 유용
    * 1개 이상의 버튼이 있을 경우 버튼을 그룹으로 묶어서 컨테이너나 상위요소에 부여하면 됨
* Alerts
    * 사용자에게 일종의 피드백을 주는 것
    * 경고사항, 안내말 다양한 상황에 사용가능
    * 만드는 방법은 버튼과 유사

<br>

### 유틸리티(Utilities)
* 가운데 정렬, 색상변경, 테두리 추가, 디스플레이 위치 특성변경, 그림자 추가등의 작업가능 
