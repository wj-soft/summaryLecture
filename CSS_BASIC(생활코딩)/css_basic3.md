* inline vs block level
    - inline : 자신의 크기만큼 영역을 차지
    - block : 화면 전체영역을 차지

* 박스모델
    - border : 박스모델의 기준점
    - margin은 border의 바깥쪽 여백  (다른 엘리먼트와의 간격)
    - padding는 border의 안쪽여백
    - inline 방식에서는 width와 height값이 무시된다.

* box-sizing
    - 컨텐츠영역 기본으로 width와 height가 적용 (기본값)
    - 이를 해결하기 위해 box-sizing속성을 활용한다.
    - { box-sizing : border-box } : border기준으로 박스크기를 설정 (컨텐츠영역에 비해 예측이 쉽기때문에 전체에 적용하고 시작하는 경우가 많다)

* 마진겹침
    - 두 요소 사이에 마진겹침이 발생된다면 큰 값을 기준으로 마진값이 적용이 된다.
    - 부모-자식 요소에 동시에 마진이 합쳐진다. (큰 값을 기준으로 마진값이 적용)
    - 단 border와 같은 효과가 없다면 위아래 기준으로 더 큰값의 마진이 적용된다.

* 포지션(position)
    - top과 buttom이 동시에 있으면 top이 우선, left와 right가 동시에 있으면 left가 우선 적용
    - static : 기본값 (offset값을 무시, 정적으로 위치 함)
    - relative : 부모엘리먼트 기준으로 offset
    - absolute : HTML엘리먼트 기준으로 offset, 상위요소에 relative가 적용되어 있다면 그 기준으로 offset, 부모와의 관계는 해제
    - fixed : 화면의 위치에 고정 (스크롤에 영향을 받지 않게됨)
    - fixed활용 예제
    ```
    <!DOCYTYPE html>
    <html>
     <head>
        <style>
            body{
                padding-top:30px;
            }
            #parent, #other{
                border:5px solid tomato;
            }
            #large{
                height:10000px;
                background-color: tomato;
            }
            #me{
                background-color: black;
                color:white;
                position: fixed;
                left:0;
                top:0;
                text-align: center;
            }
        </style>
    </head>
    <body>
        <div id="other">other</div>
        <div id="parent">
        parent
        <div id="me">me</div>
        </div>
        <div id="large">large</div>
    </body>
    </html>
    ```    

* flex
    - container과 items으로 구성
    ```
    <container>
        <item></item>
        <item></item>
    </container>
    ```
    - 사용되는 속성들

    |    container    	|     items    	|
    |:---------------:	|:-----------:	|
    | display         	| order       	|
    | flex-direction  	| flex-grow   	|
    | flex-wrap       	| flex-shrink 	|
    | flex-flow       	| flex-basic  	|
    | justify-content 	| flex        	|
    | align-items     	| align-self  	|
    | align-content   	|             	|

   
    - flex - grow&shrink
        * container(부모)요소에 flex 속성 부여 {display:flex}
        * flex-direction : items(자식요소)의 정렬 
        * flex-basis: 자식요소의 크기
        * flex-grow : 부모요소의 크기만큼 커지고 비율단위로 영역을 차지하게 됨
        * flex-shrink
        * holy grail layout
        ```
            <!doctype>
            <html>
            <head>
                <meta charset="utf-8">
                <style>
                    .container{
                        display: flex;
                        flex-direction: column;
                    }
                    header{
                        border-bottom:1px solid gray;
                        padding-left:20px;
                    }
                    footer{
                        border-top:1px solid gray;
                        padding:20px;
                        text-align: center;
                    }
                    .content{
                        display:flex;
                    }
                    .content nav{
                        border-right:1px solid gray;
                    }
                    .content aside{
                        border-left:1px solid gray;    
                    }
                    nav, aside{
                        flex-basis: 150px;
                        flex-shrink: 0;
                    }
                    main{
                        padding:10px;
                    }
                </style>
            </head>
            <body>
                <div class="container">
                    <header>
                        <h1>생활코딩</h1>
                    </header>
                    <section class="content">
                        <nav>
                            <ul>
                                <li>html</li>
                                <li>css</li>
                                <li>javascript</li>
                            </ul>
                        </nav>
                        <main>
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reiciendis veniam totam labore ipsum, nesciunt temporibus repudiandae facilis earum, sunt autem illum quam dolor
                        </main>
                        <aside>
                            AD
                        </aside>
                    </section>
                    <footer>
                        <a href="https://opentutorials.org/course/1">홈페이지</a>
                    </footer>
                </div>
            </body>
            </html>
        ```
        * flex 기타속성들
            - https://codepen.io/enxaneta/pen/adLPwv


* 미디어쿼리
    - 미디어의 종류에 따라 다른 화면을 보여주게하는 기능
    - 문법
        ```
            //500px이하일때 실행되는 미디어쿼리
            @media (max-width:500px){
                body{ }
            }
        ```
    - 캐스캐이딩이 발생되기 때문에 여러개의 미디어쿼리를 작성하기 위해서는 선언하는 순서가 중요함
    - 메타태그 추가
    ```
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    ``` 

* float
    - 주변요소가 float된 요소로 흘러가는 형태가 된다.
    - 이미지를 자연스럽게 삽입하기 위한 태그로 레이아웃배치에 주로 사용되었음
    - { clear:both } : floating을 적용받지 않기 위한 속성
    - holy grail 레이아웃
    ```
        <!doctype html>
        <html>
        <head>
        <style>
            *{
            box-sizing:border-box;
            }
            .container{
            width:540px;
            border:1px solid gray;
            margin:auto;
            }
            header{
            border-bottom: 1px solid gray;
            }
            nav{
            float:left;
            width:120px;
            border-right:1px solid gray;
            }
            article{
            float:left;
            width:300px;
            border-left:1px solid gray;
            border-right:1px solid gray;
            margin-left:-1px;
            }
            aside{
            float:left;
            width:120px;
            border-left:1px solid gray;
            margin-left:-1px;
            }
            footer{
            clear:both;
            border-top:1px solid gray;
            text-align: center;
            padding:20px;
            }
        </style>
        </head>
        <body>
        <div class="container">
            <header>
            <h1>
            CSS
            </h1>
            </header>
            <nav>
            <ul>
                <li>position</li>
                <li>float</li>
                <li>flex</li>
            </ul>  
            </nav>
            <article>
            <h2>float</h2>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sit quae earum enim ab distinctio corrupti eius reprehenderit non, rerum ut nisi autem cum sint perferendis eum id velit, molestias nesciunt. Ullam dignissimos consequuntur explicabo id voluptas vel deleniti nesciunt veritatis iusto commodi, laudantium cumque vero deserunt laboriosam. Ea, quia est?
            </article>
            <aside>
            ad  
            </aside>
            <footer>
            copyleft  
            </footer>
        </div>
        
        </body>
        </html>
    ```
    -   다단만들기
        * { column-count : 2 } : 2개의 다단
        * { column-width : 200ox} : 컬럼을 크기단위로 나누고 화면의 크기에 따라 자동으로 column-count이 지정됨
        * column-gap : 컬럼과의 간격
        * column-rule-style : 컬럼과 컬럼사이의 구분선
        * column-rule-width(or color) : 구분선의 굵기와 색상
        * {column-span: all} : 컬럼무시(타이틀)
        
    ```
            <!DOCTYPE html>
            <html>
            <head>
                <meta charset="UTF-8">
                <meta name="author" content="egoing">
                <style>
                .column{
                    text-align: justify;
                    column-count: 4;
            /*        column-width: 200px;*/
                    column-gap:30px;
                    column-rule-style: solid;
                    column-rule-width: 5px;
                    column-rule-color: red;
                }
                h1{
                    column-span: all;
                }
                </style>
            </head>
            <body>
            <div class="column">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestiae blanditiis nostrum eum ipsam, 
            </div>
            </body>
            </html>

    ```

        