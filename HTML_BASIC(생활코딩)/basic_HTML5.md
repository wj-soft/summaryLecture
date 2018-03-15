# HTML5

* input type : `<input type="number" min="10" max="15">`
    - 숫자만입력, 입력범위를 제한할 수 있음
    - 사용자의 유효성검증이 가능함
    - 모바일환경에서는 입력창 선택 시 숫자입력창을 띄운다
    - input types 종류
        * color, date, datetime, datetime-local, email, month, number, range, search, tel, time, url, week

* form 태그의 새로운 속성
    - 자동완성 : autocomplete="on"
    - input가이드 : placeholder="메세지"
    - 가장 먼저 입력되는 쪽으로 커서가 이동 : autofocus

* 입력값 체크
    - 필수입력 : required
    - 패턴 : pattern="정규표현식"
    ```
    <input required pattern="[a-zA-z]."></input>
    ```

