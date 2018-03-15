* 정보로서의 HTML : HTML은 정보를 담은 그릇이므로 정보와 의미에 집중해야한다.

* font태그
    - font태그의 경우 어떠한 의미와 정보를 담고있지 않으므로 사용하지 않아야 함 (퇴출)
    - 디자인 영역은 CSS가 담당하도록 해야 함
```
<font color="red">Hello<font> World
```

* Meta 태그
    - 웹페이지에 표현되지는 않지만 웹브라우저에게 부가적인 설명을 하는 태그
    - `<meta charset="utf-8">` : 인코딩 방식을 웹브라우저에게 설명
    - `<meta name="description" content="생활코딩소개자료">` : 웹브라우저에게 요약된 내용을 설명
    - `<meta name="keywords" content="html,css,javascript">` : 웹브라우저의 키워드를 설명
    - `<meta name="author" content="lee">` : 웹브라우저에게 저자를 설명
    - `<meta http-equiv="refresh" content="30">` : 웹브라우저에게 30초간격으로 새로고침하도록 설명

* semantic : 의믜론적인 
    - html의 내용의 의미를 표현하기 위한 태그 (별도의 기능은 없음)
    - `<header>` : 웹페이지의 헤더임을 의미
    - `<footer>` : 웹페이지의 푸터임을 의미 (주소, 회사소개 등)
    - `<nav>` : 컨텐츠 탐색을 위한 네비게이션을 의미
    - `<article>` : 웹페이지의 본문을 의미
    - `<section>` : 공통된 성질을 구분한다는 의미의 태그 (여러개의 article)

* 검색엔진 최적화
http://static.googleusercontent.com/media/www.google.com/ko//intl/ko/webmasters/docs/search-engine-optimization-starter-guide-ko.pdf

    - HTML을 의미론적으로 잘 사용하는 것이 가장 좋은 방법
    - title태그의 내용은 검색결과에 반영 (컨텐츠를 대표하는 키워드)
    - title은 각각의 웹페이지에 다르게 지정함
    - meta태그를 활용
    - url구조를 개선 (이해하기 쉽고 간결한 url)
    - 단순한 디렉토리 구조
    - 특정문서에 도달하기 위한 한가지 형태의 url 제공 (canocical 또는 301리다이랙션) 
    ```
    <link rel="canocical" href="./xxx.html">
    ```
    - 사이트내 이동하기 쉽게 만들기 (링크, 현재위치표시)
    - 404페이지에 연결링크 만들기
    - 사이트의 이동은 하이퍼텍스트 (HTML)
    - 우수한 품질의 컨텐츠 (검색엔진을 위한 컨텐츠가 아닌 사용자를 위한 컨텐츠를 생산할 것)
    - a태그 : 정보로서의 가치를 담기, 사용자가 링크태그인지 인지 할 수 있도록하기
    - img태그 : alt속성 잘 작성하기, 이미지를 위한 전용폴더 만들기, 이미지의 파일명에 의미를 부여
    - 제목은 제목태그로 작성할 것
    - robots.txt : 검색에 노출이 필요하지 않은 부분을 제어, 검색엔진최적화를 위해서는 사용하지 않고, 사이트맵을 제공
    - 페이지랭크 : 링크를 많이 받는 사이트가 우선노출 됨, 웹의 본질은 하이퍼텍스트에 있다.

* 웹개발자 도구 (크롬)

* 모바일지원
```
<meta name="viewport" content="width=divice-width, initial-scale=1.0">
```




