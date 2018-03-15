* 자주 사용되는 태그
    - `<p></p>` : 단락
        - 단락의 구분을 위한 태그, 단락간의 간격이 생김
        - 간격은 CSS를 이용하거나 br태그를통해 추가의 줄바꿈이 가능

    - `<br>` : 강제 줄바꿈, 닫침태그가 없음
        - `<p>`의 기능을 보완하거나 대체할 수 있음 `<br><br>`
        - 하지만 시각적인 요소 뿐만아니라 단락이라는 의미를 부여하기 위해 p태그의 사용이 권장 됨 

    - `<img>` : 웹페이지에 이미지를 포함하는 태그
        - `<img src="file.jpg" width="100" height="300" alt="이미지설명 title="이미지설명"">`
        - alt속성은 반드시 부여하는 것이 좋다 (웹접근성)
        - title는 툴팁의 역할
    -`<table></table>` : 웹페이지에 표를 넣기위한 태그
        - `<td></td>` : 표의 개별항목을 나타내는 항목 (table data)
        - `<tr></tr>` : 표의 행을 나타내는 항목 (table row)
        - `<thead></thead>` : 표의 개요
        -`<th></th>` : thead의 개별항목
        - `<tbody></tbody>` : 표의 내용
        -`<tfoot></tfoot>` : 표의 가장 아래쪽에 위치
        - rowspan : 행병합 (td의 속성)
        - colspan : 행병합
         ```
        <table border="1">
            <thead>
                <th>no</th>
                <th>name</th>
                <th>money</th>
            </thead>
            <tbody>
                <tr>
                    <td>1</td>
                    <td>kim</td>
                    <td>500</td>
                </tr>
            </tbody>
            <tfoot>
                <tr>
                    <td colspan="2">합계</td>
                    <td>500</td>
                </tr>
            </tfoot>
        </table>
        ```
        
        <table border="1">
            <thead>
                <th>no</th>
                <th>name</th>
                <th>money</th>
            </thead>
            <tbody>
                <tr>
                    <td>1</td>
                    <td>kim</td>
                    <td>500</td>
                </tr>
            </tbody>
            <tfoot>
                <tr>
                    <td colspan="2">합계</td>
                    <td>500</td>
                </tr>
            </tfoot>
        </table>
    

    * `<form>` : 사용자가 입력한 정보를 서버로 전송할때 사용
       - `<input type="text">` : 텍스트를 입력상자
       - `<input type="password">` : 비밀번호 입력상자
       - `<input type="submit">` : 제출하기 버튼
       - `<input type="" name="" value="">`
       - `<textarea cols="" rows=""></textarea>`
   ```
    <form action="url">
        <input type="text" name="id">
        <input type="password" name="pwd">
        <input type="submit">
    </form>
   ```
    * 다양한 폼의 종료
        - 드롭다운 : 버튼을 누르면 option의 value값이 전송됨
        ```
        <form action="url">
            <select name="color">
                <option value="1">1번</option>
                <option value="2">2번</option>
                <option value="3">3번</option>
            </select>
            <input type="submit">
        </form>
        ```

        - 라디오 : name으로 그룹화된 항목 중 하나만 선택이 가능
        - 체크박스는 다중으로 선택가능
        ```
            <input type="radio" name="color" value="1" checked>1번
            <input type="radio" name="color" value="2">2번

            <input type="checkbox" name="color" value="1" checked>1번
            <input type="checkbox" name="color" value="2">2번
        ```
        
        - 버튼 : 자바스크립트와 같이 사용
        ```
            <input type="button" onclick="alert("d")">
            <input type="reset"> 초기화
        ```

        - hidden : 화면에는 보이지 않지만 서버로 데이터를 전송할때 사용
        ```
            <form action="">
                <input type="text" name="hide" value="hiddenValue"></input>
                <input type="submit">
            </form>
        ```

        - labal : input태그의 의미를 부여, labal위치를 클릭해도 입력영역으로 커서가 이동, 권장사항
        ```
            <p>
                <label for="myid">이름</label>
                <input id="myid" type="text" name="id">
            </p>

             <p>
                <label>이름
                    <input id="myid" type="text" name="id">
                </label>
            </p>
        ```

        - method : 서버로 데이터를 전송하는 방법
            * GET : url로 데이터를 전송하는 방식
            ```
            <form action="url" method="get">
                <input type="text" name="id">
                <input type="submit">
            </form>
            ```
            * POST : url이 아닌 다른방법으로 숨겨서 전송
            ```
            <form action="url" method="post">
                <input type="text" name="id">
                <input type="submit">
            </form>
            ```

        - 파일업로드
        ```
            <form action="url" method="post" enctype="multipart/form-data">
                <input tpe="file" name="profile">
                <input type="submit">
            </form>
        ```



