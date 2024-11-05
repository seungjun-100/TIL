# Today I Learned

<br>

## HTML
* Hyper Text Markup Language의 약자
  
  * Hyper Text

    * (내, 외부)링크에 따라 다양한 문서들로 넘어갈 수 있는 형태
  
  * Markup

    * 태그 등을 이용하여 문서나 데이터의 구조를 표기하는 형태이다.

    * content(제목, 글, 이미지, 버튼 등)의 성격을 표시해주는 기능만 있다.
  
    ```
      <html>
          <head>
              <title>Hello, HTML</title>
          </head>
          <body>
              <h1>Heading</h1>
              <p>Paragraph</p>
              <img src="path" alt="text" />
          </body>
      </html>
    ```
  
* 웹 브라우저상에서 보여지도록 디자인된 문서이다.

* 웹 페이지를 구조화 하기 위해 마크업 언어를 사용한다.

<br>

## HTML 역사
* 팀 버너스리에 의해 1990년에 개발되었따. (공식적으로 소개된건 1991년)

* 1993년 HTML 1.0이 IETF(Internet Engineering Task Force)에 의하여 표준으로 등장했다.

* 1995년 HTML 2.0이 IETF에 의하여 표준으로 등장했다.

* 사용자가 많아지고 사용자에게 다양한 브라우저가 보편화되기 시작하면서 웹의 표준화 논의했다.

* 1997년 HTML 3.2가 W3C(World Wide Web Consortium)에 의해 권고안으로 등장했다.

* 1999년 HTML 4.01이 W3C에 의해 권고안으로 등장, 안정된 표준의 HTML 버전, CSS(Cascading Style Sheet)로 디자인적인 요소를 구분하게 되고, HTML로는 웹페이지의 전반적인 구조만을 명시하도록 원칙을 정하였다.

* 2000년 W3C의 새로운 표준 XHTML 권고, XML(Extensible Markup Language)의 엄격함을 주요 내용으로 HTML을 합성한 웹 표준, 반응이 미비했다.

* WHATWG(Web Hypertext Application Technology Working Group) 탄생, 시장 요구에 부응하지 못하는 W3C에 실망하고 대중적인 브라우저를 가지고 있던 기업들(Apple, Mozilla, Opera, Google)이 HTML에 기초하여 웹 기술과 시장의 요구를 분석하여 HTML5 작업을 착수했다.

* W3C의 HTML5 수용, 2008년 W3C에 의해 HTML5 초안 발표, 2009년 XHTML2 개발 중단, 2014년 HTML5 표준안 확정 발표했다.

* WHATWG는 W3C와 협업을 진행하면서도 W3C와는 별도로 독자적인 HTML 표준의 작업을 시작했고, 이를 HTML Living Standard라는 이름으로 발표했다. ( HTML Living Standard는 W3C의 HTML5와는 달리 버전 없이 그때그때 업데이트된다. )

* 표준이 2개면 혼란이 발생하기 때문에 W3C와 WHATWG는 논의를 통해 HTML 표준을 HTML Living Standard로 단일화하여 2019년에 HTML Living Standard가 표준화가 되었다.




<br>




## CSS
* Cascading Style Sheets의 약자

  * 계단식으로 스타일을 정의하는 문서를 뜻한다.

* HTML 요소들이 어떻게 보일지 정의하는 스타일 시트 언어이다.

* 선택자(selector)와 선언부(declaratives)로 구성된다.

  * 선택자는 CSS를 적용하고자 하는 HTML 요소이다.

  * 선언부는 스타일 내용들을 담고 있다.
  
  <pre>
    h1 { // 선택자
        color: #333; // 선언부
        font-size: 26px; // 선언부
    }
  </pre>




<br>




## JavaScript
* 웹 페이지를 동적으로 동작하기 위해 만들어진 프로그래밍 언어(script)이다.

* 주로 웹 브라우저에서 사용되며, 서버 개발(Node.js), 애플리케이션 개발에서도 사용이 가능하다.

* 현재 컴퓨터, 스마트폰 등에 포함된 웹 브라우저는 대부분 JS 인털프리터가 내장되어 있다.

<br>

## JavsScript의 역할

  * HTML 페이지 변경 및 HTML 콘텐츠 추가, 제거

  * CSS 및 HTML 엘리먼트의 스타일 변경이

  * 사용자와의 상호작용

  * 폼(Form)의 유효성 검증

  * 웹 브라우저 제어, 쿠키 설정과 조회

  * 클라이언트 측 데이터 저장(로컬 스토리지)

  * AJAX 기술을 이용한 웹 서버와 통신




<br>




## 웹 표준 ( Web Standards )
* HTML5는 W3C에서 2014년에 공식 표준화 되었다.

* 2019년에 WHATWG에 의해 HTML Living Standard가 표준화 되었다.

* HTML이 표준화 되기 이전에는, 익스플로러의 액티브X처럼 독자적인 플러그인이 존재하기도 했었다.

* 웹 표준을 준수하여 작성한다면 운영체제, 브라우저마다 의도된 대로 보여지는 웹 페이지를 만들 수 있다.

<br>

## 웹 접근성 ( Web Accessibility )
* 웹 접근성은 장애를 가진 사람과 장애를 가지지 않은 사람 모든 사용자들이 웹 사이트를 이용할 수 있게 하는 방식을 가리킨다.

* 웹 접근성은 장애를 갖지 않아도 특정 상황에 따라 문제가 있는 사용자들도 정보와 기능에 동등하게 접근할 수 있다.

  * 작은 화면, 다른 입력 모드 등을 가진 휴대폰, 스마트 워치, 스마트 TV 및 다른 디바이스를 사용하는 사람

  * 나이가 들어감에 따라 기능적 능력이 변한 연로한 사람

  * 팔이 부러지거나 안경을 잃어버려서 "일시적인 장애"를 겪는 사람

  * 밝은 햇빛이나 소리를 듣기 힘든 환경에 있어 "상황적 제약"을 겪는 사람

  * 느린 인터넷을 사용하거나 제한적이거나 비싼 대역폭을 사용하는 사람

* 웹 브라우징에 쓰이는 보조과학기술 : 스크린리더, 화면 돋보기, 음성 인식, 키보드 오버레이 등

<br>

## 웹 호환성 ( Cross Browsing )
* 크롬, 사파리, 엣지, 웨일 등 다양한 웹 브라우저가 있는데 브라우저 마다 화면을 보여주는 렌더링 엔진이 달라 브라우저에 따라서 다르게 보일 수 있기 때문에, 브라우저 버전, 종류와 상관 없이 똑같은 웹 페이지를 보여주기 위해서는 크로스 브라우징을 해야한다.

* 웹 표준 준수를 통한 브라우저 호환성 확보

  * HTML, CSS 문법 준수

  * 동작, 레이아웃, 플러그인 호환성
