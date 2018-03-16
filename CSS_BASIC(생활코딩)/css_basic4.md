* 배경 (background)
    - https://www.w3schools.com/css/css_background.asp
    - { background-color : red } : 배경색상
    - { background-image : url('ddd.png') } : 배경이미지
    - { background-repeat : no-repeat } : 반복X
    - { background-attchment : fixed} : 이미지고정 (스크롤X)
    - { background-size: 100px 100px } : 이미지크기조정 (CSS3에서 도입)
    - { background-size: cover } 
    - { background-size: contain } : 화면에 전체이미지를 넣기
    - { background-position: reft bottom } : 이미지 위치조정 
    - 축약형 : {background : tomato url('') no-repeat fixed center}

* 필터 (filter)
    - CSS최신기능으로 이미지, 동영상, 텍스트 등에 다양한 효과를 주는 기능
    - http://bennettfeely.com/filters/
    - 최신기능오로 벤더프리픽스가 요구됨
    ```
        img {
            -webkit-filter: grayscale(100%);
            -o-filter: grayscale(100%);
            filter: grayscale(100%);
        }
    ```
    - 코드펜 예제를 보고 연습

* 변형 (transform)
    - { transform: scaleX(0.5), scaleY(0.5) } : x축, y축 0.5배
    - 다양한 변형의 종류 확인
    - https://codepen.io/vineethtr/full/XKKEgM

* transition
    - CSS가 효과가 적용되는 과정에서 부드럽게 전환 하기 위한 기능
    - inline 요소에서는 동작이 안됨 (block 또는 inline-block로 변경)
    ```
        <!doctype html>
        <html>
        <head>
        <style>
            a{
            font-size:3rem;
            display:inline-block;
        /*
            transition-property: font-size transform;
            transition-duration: 0.1s;
            transition:all 0.1s;
        */
            transition:all 0.1s;
            }
            a:active{
            transform:translate(20px, 20px);
            font-size:2rem;
            }
        </style>
        </head>
        <body>
        <a href="#">Click</a>
        </body>
        </html>
    ```
    - https://matthewlein.com/tools/ceaser
    - 코드팬 적용사례 학습
    ```
        <!doctype html>
        <html>
        <head>
        <style>
            body{
            background-color: black;
            transition:all 1s;
            }
            div{
            background-color: black;
            color:white;
            padding:10px;
            width:100px;
            height:50px;
            -webkit-transition: all 500ms cubic-bezier(0.680, 0, 0.265, 1); /* older webkit */
            -webkit-transition: all 500ms cubic-bezier(0.680, -0.550, 0.265, 1.550); 
                -moz-transition: all 500ms cubic-bezier(0.680, -0.550, 0.265, 1.550); 
                -o-transition: all 500ms cubic-bezier(0.680, -0.550, 0.265, 1.550); 
                    transition: all 500ms cubic-bezier(0.680, -0.550, 0.265, 1.550); /* easeInOutBack */
        
            -webkit-transition-timing-function: cubic-bezier(0.680, 0, 0.265, 1); /* older webkit */
            -webkit-transition-timing-function: cubic-bezier(0.680, -0.550, 0.265, 1.550); 
                -moz-transition-timing-function: cubic-bezier(0.680, -0.550, 0.265, 1.550); 
                -o-transition-timing-function: cubic-bezier(0.680, -0.550, 0.265, 1.550); 
                    transition-timing-function: cubic-bezier(0.680, -0.550, 0.265, 1.550); /* easeInOutBack */
            }
            div:hover{
            height:400px;
            }
        </style>
        </head>
        <body onload="document.querySelector('body').style.backgroundColor='white';">
        <div>
            TRANSITION
        </div>
        </body>
        </html>
    ```