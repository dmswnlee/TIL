# 표 table

```html
<table>
    <thead>
        <tr>
            <th>이름</th>
            <th>직업</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>제이</td>
            <td>프론트엔드개발자</td>
        </tr>
        <tr>
            <td>이영희</td>
            <td>백엔드개발자</td>
        </tr>
    </tbody>
    <tfoot></tfoot>
</table>
```
<br>

* 데이터를 담은 표를 만들 떄 사용
* `th`가 있다면 `td`도 반드시 입력해줘야함, 빈칸이라도 공백으로 입력
* 시맨틱마크업을 위해 thead, tbody, tfoot 사용
* 표를 만들때는 몇개의 칸이 들어가는지(tr) 인지하고 시작해야함
* rowspan="숫자" 행
* colspan="숫자" 열 
* scop="row/col"  `th`에서만 사용가능, 브라우저에 더 풍부한 정보를 전달