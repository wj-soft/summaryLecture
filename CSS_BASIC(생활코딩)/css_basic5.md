* link와 import
    - 동일한 css를 여러개의 html이 사용할떄 
    `<link rel="stylesheet" href="style.css">`
    - css에서 다른 css를 사용할떄
    `@import url("ddd.css")`

* 코드경량화 (minify)
    - css의 크기를 최소화 하여 서버에서 보다 빠르게 받기 위한 행위 
    - http://adamburgess.github.io/clean-css-online/
    - https://github.com/jakubpawlowicz/clean-css

* preprocesser
    - less, sass, stylus-lang 등 css 언어를 효과적으로 사용하기 위한 언어
    - preprocesser비교 : https://csspre.com/compile
    - css는 표준으로 신규기능이나 문법이 추가되기 어려우므로 이를 보완하기 위해 preprocesser가 등장했고 preprocesser작업한 파일은 css로 변환하여야 함
    - preprocesser를 사용하기 위해서는 preprocesser의 문법과 컴파일러 사용방법을 학습해야 함.

* Fontello
    - 문자로 이미지 아이콘을 표현하기 위한 방법 (백터방식으로 확대해도 깨지지 않음, 색상이나 크기를 자유롭게 변경할 수 있음)
    - http://fontello.com/
    - 사용법 : fontello.css를 link하고 font-family를 지정하고 '&#코드' 를 입력 함
    - `<i class="icon-name"></i>` : 이 방식으로 사용하면 font-family를 사용하지 않아도 됨. 미리 fontelo.css에 설정이 되어있음
    - animation을 추가할 수 있음.
    - 아이콘을 직접 만들 수 있음 (svg이미지를 만들어 폰텔로에서 폰트를 생성)
    - 픽토그램검색 사이트 : https://thenounproject.com/
    - 기존것을 불러오기 위해서는 config.json을 이용한다.






