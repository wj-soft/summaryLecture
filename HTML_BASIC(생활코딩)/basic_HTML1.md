## https://www.inflearn.com/course/html-%EA%B8%B0%EB%B3%B8/


* 기술소개
    - HTTP : Hyper Text Markup Language (하이퍼텍스트기반의 마크업 언어)
    - 프로그래밍언어는 컴퓨터와 인간의 약속이라고 할 수 있는데 HTML은 웹브라우저에서가 읽을 수 있는 언어라고 할 수 있다.

* 기본문법과 하이퍼텍스트 속성
    - 확장자가 html인 파일을 웹브라우저기 읽어서 view를 만든다.
    - tag : <> 태그는 안의 내용은 약속된 의미를 나타낸다. (예제참조)
    ```
        // 제목을 의미하는 태그
        <h1> TITLE </h1>
        // 텍스트 '자신의 힘'을 강조하는 의미를 가지는 태그
        우리는 <strong> 자신의 힘 </strong> 으로 ....
    ``` 
    - 속성 : tag에게 부여되는 정보, 속성의 이름에 따라 기능이 정의됨
    ```
       //아래의 href, target, title처럼 a태그에게 정보를 제공하는 것을 속성이라고 함
        <a href="https://naver.com" 
        target="_blank"
        title="네이버링크">링크</a>
    ```
    - a태그 : anchor, 하이퍼텍스트언어라는점에서 매우 중요한 특성이다. 팀버너스리는 SGMLguid에 a태그를 추가하여 HTML을 만들었다. (HTML의 역사 :GML(1960년대 말) => SGML => SGMLguid => HTML ) 

* 태그의 중첩과 목록 
    -  `<ul> <li>` ul또는 ol li를 그룹화 함
    ```
        //순서가 없는 목록
        <ul>
            <li>1번 목록</li>
            <li>2번 목록</li>
            <li>3번 목록</li>
        </ul>
        //순서가 있는 목록
        <ol>
            <li>1번 목록</li>
            <li>2번 목록</li>
            <li>3번 목록</li>
        </ol>
    ```

* 문서의 구조
    - head태그 : 브라우저에게 제공하는 부가적인 정보 
    - body태그 : 화면에 표시되는 본문영역
    - html태그 : head와 body태그를 포함
    ```
    <html>
        <head>
            <title> Title of tab </title>
            <meta charset="utf-8">
        </head>
        <body>
            <h1>Main Title</h1>
            <ul>
                <li>1번 목록</li>
                <li>2번 목록</li>
                <li>3번 목록</li>
            </ul>
            <h2>1번목록 상세</h2>
            1번목록은 ......
        </body>
    </html>
    ```
* DOCTYPE  `<!DOCYTYPE html>`
    - Document Type Declaration (문서타입선언)
    - 작성된 문서의 타입을 브라우저에게 알려주기 위해 선언한다.
    - HTML5의 경우 `<!DOCYTYPE html>`, 만
    약 그외 버전을 사용한다면 아래의 그 타입을 선언해야함 (링크참조)
    https://www.w3schools.com/tags/tag_doctype.asp
