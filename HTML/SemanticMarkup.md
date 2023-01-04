# 시맨틱 마크업
1. Semantic Markup?
* 의미와 구조에 맞게 마크업 하는 것(의미있는 마크업)
* 문서의 구조와 정보위계가 명확하게 보이는 코드를 작성하자
* **HTML을 시맨틱하게 작성해야 하는 이유**
    * 다양한 html 태그를 사용해서 그 정보 컨텐츠의 의미에 맞게 구조적으로 마크업 하기 위해 
    * SEO(Search Engine Optimization) 검색 엔진 최적화에 도움 됨
    * 어떤 코드를 사용하는지 쉽게 파악할 수 있음
    * 웹접근성이 좋아짐

<br>

### div & span

<br>

* 주어진 요소가 문서의 콘텐츠 흐름에 들어가게 하는 방법
* 의미없음
* css 스타일링을 위해 요소를 묶어야 할 떄 사용 
* `div` : 블록레벨요소, 요소들을 그룹화 할때 사용
* `span` : 인라인요소, 텍스트 감싸서 스타일링 할때 사용
* 의미없는 태그이므로 너무 남발하여 사용하지 않는것이 좋음!

<br>


### Sectioning Elenments 요소들
* section
* article 
* nav
* aside

<br>

### 문서의 구조를 표현하는데 도움이 되는 3가지 요소 
* header
* main
* footer

<br>

### **올바른 Sectioning Elenments 사용방법**
공통적으로 지켜야 할 룰
* Sectioning Elenments = 단원
* 단원의 주제, 제목이 반드시 필요
* Sectioning Elenments 내에는 반드시 **heading** 태그를 작성해야 함

<br>

### Header
* div와 비슷한 기능
* Sectioning Elenments가 아니기 때문에 heading 태그 생략가능

<br>

### Nav
* 문서간으로 이동하는 메뉴가 있으면 유용하게 사용하는 태그
* 반드시 heading 태그를 사용해서 제목을 명시해줘야 함

<br>

### Main
* 한개의 html 안에서는 한개의 main 밖에 쓰지 못함
* 본문의 구조상 제일 핵심적인 내용을 묶어줄 때 사용
* section, article, nav, aside 안에 사용할 수 없음 감싸주는건 가능
* Sectioning Elenments가 아니기 때문에 heading 태그 생략가능

<br>

### Section
* 독립된 부분을 나타낼 때 사용
* 반드시 heading 태그를 사용해서 제목을 명시해줘야 함

<br>

### Article
* 뉴스기사, 블로그, 트윗 같이 안에 있는 정보 컨텐츠가 완결성이 있으며 혼자 독립적으로 존재하는 것을 나타낼 떄 사용 
* 반드시 heading 태그를 사용해서 제목을 명시해줘야 함

<br>

### Aside 
* 위젯, 광고등 사이드바에서 본문과는 직접적인 연관이 없는 동떨어진 내용을 나타낼 떄 사용 
* 반드시 heading 태그를 사용해서 제목을 명시해줘야 함

<br>

### Footer
* 꼬리말, 페이지의 정보등의 내용을 나타낼 때 사용 
* Sectioning Elenments가 아니기 때문에 heading 태그 생략가능

<br>

### **엔티티 Entity**
* `&lt;`(<)  
* `&gt;`(>)