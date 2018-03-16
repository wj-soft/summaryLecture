* CSS : HTML에서 정보와 디자인을 분리하기 위해 등장한 언어

* HTML과 CSS가 만나는법
    - 인라인 : `<h1 stype="color:red"></h1>`
    - 스타일태그 : 
    ```
        <style>
            h1 {color : red}
        </style>
    ```

* 선택자와 선언
    - 선택자 { 프로퍼티 : 값; 프로퍼티 : 값 }
    - ID선택자 : #ID {}
    - Class선택자 : .Class {}
    - 부모자식 선택자 : ul li
    - 직계자손 산턱자 : ul>li
    - 동시에 선택 : ul,ol
    - 가상클래스 선택자
        * :link - 방문한적이 없는 링크
        * :visited - 방문한적이 있는 링크
        * :hover - 마우스를 올렸을때
        * :active - 마우스를 클릭했을떄
        * :focus - 포커싱되었을 떄 (마지막에 선언하는것이 좋음)

* 선택자 공부 tip
    - http://flukeout.github.io/  게임으로 배우기
    - CSS Cheat Sheet 활용

* 상속
    - 바깥쪽에서 안쪽으로 상속 (부모의 속성을 자식이 물려받는다)
    - 모든 속성이 상속되는 것은 아니다 (ex border)
    - https://www.w3.org/TR/CSS21/propidx.html

* 캐스캐이딩
    - 하나의 태그에 여러개의 속성이 중첩되어있을때 우선순위를 적용하여 처리됨
    - 우선순위 : 웹브라우저 < 사용자 < 저자
    - style attribute > id selector > class selector > tag selector
    - 구체적일수록 우선순위가 높다.
    - !important 키워드는 가장 높은 우선순위를 가진다

* 서체다루기
    - font-size (폰트의 크기)
        - 단위 : px em rem
        - rem 권장 (html 폰트사이즈에 비례하여 크기가 변함) : 사용자가 브라우저에서 폰트사이즈를 설정하는 경우 px는 고정 됨
    - color (색상)
        - 단위 : colorName, hex, rgb
        - https://www.w3schools.com/cssref/css_colors.asp
    - text-align (정렬)
        - text-align : center;
        - right(오른쪽정렬), left(왼쪽정렬), center(가운데정렬), justfy(균등분할)
    - font-family (글꼴)
        - font-family: arial, verdana, "Helvetica Neue" ,serif;
        - serif vs sans-serif (장식의 유무)
        - monospace (고정폭)
    - font-weight : bold (굵게)
    - line-height : 1.2 (자간, 기본값 1.2배)
    - Web Font
        - 구글웹폰트 : https://fonts.google.com/?authuser=1
        - font-family : '폰트이름'   @font-face에서 지정

        







    