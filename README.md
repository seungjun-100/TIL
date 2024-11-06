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

## HTML 작성 규칙
* 웹 페이지를 구성하고 있는 요소(element) 하나 하나를 “태그”라는 표기법으로 작성

* 태그를 통해 어떤 요소인지 (제목, 본문, 이미지, 비디오 등) 명시

* 태그의 이름은 HTML5 웹 표준에 맞게 작성

* 여는 태그와 닫는 태그로 요소의 범위를 지정한다.
    ```
      <p>내용(content)</p> // 요소(element)
    ```

* 태그의 경우 대소문자를 구분하지 않는다.

* HTML5 에서는 모두 소문자로 작성하는 것을  권장한다.

<br>

## 빈 요소 ( Empty elements )
* 닫는 태그 없이 단독으로 사용되는 요소

* 이미지, 수평선, 줄바꿈 등
    ```
      <br>
      <hr>
      <img src=“http:image.url/images/icon.jpg”>
      <meta charset=“”utf-8>
      <input type=“text” name=“name”>
    ```

* Empty element, Self-Closing element, Void element, Single tag, …

* XHTML은 굉장히 엄격한 문법이여서 빈 요소인 경우에는 뒤에 슬래쉬(/)를 넣어줘야지만 브라우저가 Closing tag를 찾지 않고 동작을 하는 형태였다.

* HTML5 에서는 빈 요소의 슬래쉬(/) 작성은 자유지만 한가지의 형태로 일관성있게 코드를 작성해야한다.
    ```
      <br> = <br />
    ```

<br>

## HTML 문서의 구조
* HTML5의 표준을 지키는 HTML의 기본 골격
    ```
      <!DOCTYPE html>
      <html>
        <head>
          <!— HEAD 영역 —>
        </head>
        <body>
          <!— BODY 영역 —>
        </body>
      </html>
    ```

* DOCTYPE : Document Type(문서의 타입)을 명시한다.
  
  * HTML5 표준 이전에는 버전을 명시하여 브라우저가 명시된 버전에 맞는 문법으로 해석하였다.

  * 현재는 대부분의 브라우저가 HTML5의 표준을 준수하고 있기때문에 html이라고만 적어도 해석이 가능하다.

* html : 페이지 전체의 컨텐츠를 감싸는 최상위(root) 요소

* head : 메타데이터와 스크립트, CSS 등이 위치

* body : 웹 브라우저 화면에 나타나는 모든 컨텐츠(HTML 문서의 내용)

<br>

## HEAD 태그
* 웹 브라우저 화면에 직접적으로 나타나진 않는 웹 브라우저가 식별할 수 있는 문서 정보를 담는다.

* title : HTML 파일의 제목으로 웹 브라우저 타이틀에 나타난다.
    ```
    <title>웹 페이지 제목</title>
    ```

* 문자 인코딩
  * 사용하는 텍스트 에디터의 문자 인코딩과 HTML의 문자 인코딩과 동일해야 웹 브라우저에서 옳바르게 표시된다.

  * 유니코드인 UTF-8로 지정한다.

* 메타데이터
  * 메타데이터를 기술하면 웹 검색에 유리하다.

  * HTML에 대한 문서의 정보를 기록할 수 있다.

* Script, CSS등이 위치한다. (외부 파일 연결)

<br>

## 콘텐츠 카테고리
* HTML5부터 비슷한 특징을 가진 요소끼리 묶어서 7가지 카테고리로 세분화

* 하나의 HTML 요소가 여러 콘텐츠 카테고리 내의 포함관계에 들어갈 수도 있다. (교집합)

* 메타데이터 콘텐츠 ( Metadata Content )
  * 문서의 메타 데이터(정보), 다른 문서를 가리키는 링크 등을 나타내는 요소

* 플로우 콘텐츠 ( Flow Content )
  * 웹 페이지상에 메타데이터를 제외하고 거의 모든 요소, 보통 텍스트나 임베디드 콘텐츠를 포함

* 섹션 콘텐츠 ( Section Content )
  * 웹 문서의 구획(Section)을 나눌 때 사용

* 헤딩 콘텐츠 ( Heading Content )
  * 섹션의 제목(Heading)과 관련된 요소

* 프레이징 콘텐츠 ( Phrasing Content )
  * 문단에서 텍스트를 마크업할 때 사용

* 임베디드 콘텐츠 ( Embedded Content )
  * 이미지나 비디오 등 외부 소스를 가져오거나 삽입할 때 사용되는 요소

* 인터렉티브 콘텐츠 ( Interactive Content )
  * 사용자와의 상호작용을 위한 컨텐츠 요소

* MDN : https://developer.mozilla.org/ko/docs/Web/HTML/Content_categories

<br>

## 텍스트 요소
* 법칙을 준수하여 작성하면 웹 표준과 웹 접근성이 좋은 페이지를 만들 수 있다.

* 제목
    ```
    <h1> ~ <h6>
    - 웹 브라우저가 제목의 정보를 사용해 자동으로 문서의 목차를 만드는 등의 작업을 수행할 수 있다.
    - 제목 단계는 <h1>, <h2>, …, <h6> 순차적으로 기입해야 한다.
    - 페이지 당 하나의 <h1>만 사용해야 스크린 리더 사용자와 SEO에 적합하다.
    ```

* 본문
    ```
    <p>
    - 하나의 문단을 나타낸다.
    - 일관성 있는 데이터라면 이미지나 입력 폼 등 콘텐츠를 포함할 수 있다.
    - 내부에 있는 자식 태그가 블록 요소이면 자동으로 <p>태그가 닫힌다.

    <br>
    - 문단 구분을 <br>로 하는것은 나쁜 사례이다. 스크린 리더가 요소의 존재는 알려주겠지만, <br>에는 아무런 내용도 없기 때문에 사용자는 내용이 어딨는지 혼란을 느낄 수 있다.

    <blockquote>
    - 인용 블록 요소
    - 안쪽의 텍스트가 긴 인용문임을 나타낸다.
    - 앞쪽에 여백이 들어간다.
    - cite 속성 : 인용문의 출처 문서나 메시지를 가리키는 URL
      <blockquote cite="">
        <p>...</p>
      </blockquote>

    <q>
    - 인라인 인용문 요소
    - 둘러싼 텍스트가 짧은 인라인 인용문임을 나타낸다.
    - 기본으로 앞, 뒤로 쌍따움표를 붙여준다.
    - cite 속성 : 인용문의 출처 문서나 메시지를 가리키는 URL
      <p><q cite="">APPLE</q> - PEN</p> -> "APPLE" - PEN

    <pre> 
    - preformatted
    - 미리 서식을 지정한 텍스트를 나타낸다.
    - HTML에 작성한 내용 그대로 표현한다. (spacing 포함)
    - 고정폭 글꼴을 갖고있다.

    <figure>
    - 독립적인 콘텐츠를 표현한다.
    - <figcaption> 요소를 사용해 설명을 붙일 수 있다.
    - 앞쪽에 여백이 들어간다.
      <figure>
        <img>, <video>, <p>, <pre>, <blockquote> 등
        <figcaption>...</figcaption>
      </figure>

    <hr>
    - Horizon - 수평선
    - 의미적으로 무언가 전환을 하고 싶을때 사용한다.

    <abbr>
    - Abbreviation - 약어
    - title이라는 속성은 전역 속성(Global Attributes)이라서 어떤 태그에도 사용이 가능하다. 
      하지만 title 속성은 abbr태그의 특성에 좀 더 의미가 있다.
      <abbr title="World Wide Web">WWW</abbr>

    <address>
    - 오프라인 주소, 메일 주소, 웹사이트 주소, SNS 주소 등

    <cite>
    - 인용의 출처
    - 인용구의 출처를 브라우저에서 눈에 보이게끔 사용하기 위해 사용한다.
    - cite="" 속성은 눈에 보이지 않는다.

    <bdo>
    - Bidirectional Override - 양뱡향
      <bdo dir="rtl"><bdo> // 텍스트가 오른쪽에서 왼쪽으로 정렬
      <bdo dir="ltr"><bdo> // default 텍스트가 왼쪽에서 오른쪽으로 정렬
    ```

* 포매팅
    * 포매팅 요소들을 사용하면 태그들 안에 있는 내용들은 다른 태그들에 비해서 무언가 의미를 더 갖게 된다.
    ```
    <b>
    - 굵은 글씨 요소

    <strong>
    - 굵은 글씨 요소
    - 높은 중요도 요소 !!
    - 스크린 리더에서 강조하여 읽는다.

    <i>
    - italic체
    - 주위와 구분해야 하는 부분
    - 고유 명사, 기술 용어, 외국어 구절, 등장인물의 생각 등

    <em>
    - italic체
    - 강세 요소 (strong 태그와는 다른 강세)

    <mark>
    - 중요한 표시 또는 하이라이트한 부분을 나타낸다.
    - 배경색이 들어가 표시가 된다.

    <small>
    - 덧붙이는 글이나 저작권과 법률 표기 등의 작은 텍스트를 나타낸다.

    <sup>
    - 위 첨자 요소

    <sub>
    - 아래 첨자 요소

    <del>
    - 문서에서 제거된 텍스트의 범위를 나타낸다.
    - 표시 : line-through
    - cite 속성 : 어떤걸로 인해서, 혹은 어떤 시점에, 무엇으로 얘가 삭제 됐는지 변경점을 설명하는 리소스
    - datetime 속성 : 변경이 발생한 일시

    <ins>
    - 문서에서 추가된 텍스트의 범위를 나타낸다.
    - 표시 : underline
    - cite 속성 : 어떤걸로 인해서, 혹은 어떤 시점에, 무엇으로 얘가 추가 됐는지 변경점을 설명하는 리소스
    - datetime 속성 : 변경이 발생한 일시

    <code>
    - 인라인 코드 요소
    - 짧은 코드 조각을 나타낼때 사용
    - 고정폭 글꼴을 사용
    - 여러 줄의 코드를 나타내려면 <code> 요소를 <pre> 요소로 감싸서 사용

    <kbd>
    - 키보드 입력 요소
    - 고정폭 글꼴을 사용
    ```

* a태그와 하이퍼링크
    ```
    <a>
    - 앵커 요소는 href 속성을 통해 링크 경로를 지정
    - <a href="" target=""></a>
    - 절대경로 : 현재의 위치와 관련이 없이 무조건 절대값의 위치로 이동하는 경로
    - 상대경로 : 현재의 위치에서 부터 이동할 목적지로 이동하는 경로
    - 이메일 : <a href="mailto:aaa@email.com">email</a>
    - 전화 : <a href="tel:555-5309">phone</a>
    - target 속성은 목적지를 어디에 띄울것 인가 결정한다.
    - _self : default, 현재 브라우저 창에서 표시
    - _blank : 새로운 브라우저 창에서 표시
    - _parent : 현재 브라우저 창의 부모 창이 있다면 그 부모 창에서 표시
    - _top : 최상위 브라우저 창에서 표시
    - https://developer.mozilla.org/ko/docs/Web/HTML/Element/a
    ```

<br>

## 구조를 나타내는 요소
* 구조를 나타내는 요소
    ```
    <div>
    - 콘텐츠 분할을 위한 블록 컨테이너
    - 태그에 아무 의미가 없는게 특징
    - 주로 스타일링이나 레이아웃을 위해 묶는다.

    <span>
    - 구문 콘텐츠를 위한 통용 인라인 컨테이너
    - 태그에 아무 의미가 없는게 특징
    <header>
    - 소개 및 탐색에 도움을 주는 콘텐츠
    - 제목, 로고, 검색 폼, 작성자 이름 등을 포함할 수 있다.
    - 전체 페이지를 대표하는 제목으로 들어갈 수 있다.
    - 한 기사, 논문의 글 제목으로 들어갈 수 있다. 

    <footer>
    - 구획의 작성자, 저작권 정보, 관련 문서 등을 포함할 수 있다.
    - 사이트의 전체를 아우를 수 있는 링크들을 포함할 수 있다.

    <nav>
    - 현재 페이지 내, 또는 다른 페이지로의 링크를 보여주는 구획
    - Home > menu_1 > menu_1_1 > menu_1_1_1

    <aside>
    - 문서의 주요 내용과 간접적으로만 연관된 부분을 나타낸다.
    - 추가적인, 부가적인 정보지만 없다고 해서 본문에 크게 문제가 되지 않은 것들을 포함한다. 
    - 사이드바 혹은 콜아웃 박스

    <main>
    - body 태그의 하위 자식으로 사용되며 단 하나만 사용이 가능하다.
    - 여러개 사용시에는 유일한 main 요소 외에 나머지 요소는 hidden 속성을 사용하여 눈에 보이지 않게 해야한다.

    <article>
    - 독립적으로 구분해 배포하거나 재사용할 수 있는 구획을 나타낸다.
    - 독립적인 컨텐츠라서 그것만의 의미를 갖고 있으므로 다른 곳에서도 사용이 가능하다.
    - 게시판과 블로그 글, 매거진이나 뉴스 기사 등에 사용이 된다.
    - 식별할 수단으로 주로 제목(<h1> ~ <h6>) 요소를 넣어준다.
      <article>
        <header>
          <h2></h2>
        <header>
        <section><section>
        <footer><footer>
      </article>

    <section>
    - 문서의 독립적인 구획을 나타낸다.
    - <article>과는 다르게 단독적으로 사용 불가
    - 요소의 콘텐츠를 따로 구분해야 할 필요가 있으면 <article> 요소로 사용하는걸 고려해봐야 한다.
    ```

<br>

## 시맨틱 웹 ( Semantic Web )
* Semantic : 의미의, 의미론적인
  
* 요소의 의미를 고려하여 구조를 설계하고 코드를 작성한다.
  
* 의미론적인 마크업을 사용하면 좋은점
  * 검색 엔진은 의미론적 마크업을 분석하여 페이지의 검색 랭킹에 영향을 줄 수 있는 중요한 키워드로 간주한다.
  
  * 시각 장애가 있는 사용자가 스크린리더로 페이지를 탐색할 때 의미론적 마크업을 푯말로 사용할 수 있다.
  
  * 의미가 없는 끊임없는 div 들을 탐색하는 것보다 의미있는 코드 블록을 찾는 것이 훨씬 쉽다.
  
  * 개발자에게 태그 안에 채워질 데이터 유형을 제안한다.
  
  * 의미있는 이름짓기(Semantic naming)는 적절한 사용자 정의 요소 / 구성 요소의 이름짓기(naming)를 반영한다.




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




<br>




## VScode 단축키
* 에디터 창 제어
  <table style="width: 100%; border-collapse: collapse; table-layout: fixed;">
    <tr>
      <th>Control</th>
      <th>Window</th>
      <th>Mac</th>
    </tr>
    <tr>
      <td>현재 창 닫기</td>
      <td>Ctrl + w</td>
      <td>Cmd + w</td>
    </tr>
    <tr>
      <td>닫은 창 다시 열기</td>
      <td>Ctrl + Shift + t</td>
      <td>Cmd + Shift + t</td>
    </tr>
    <tr>
      <td>사이드바 토글</td>
      <td>Ctrl + b</td>
      <td>Cmd + b</td>
    </tr>
    <tr>
      <td>사이드바 - 탐색기</td>
      <td>Ctrl + Shift + e</td>
      <td>Cmd + Shift + e</td>
    </tr>
    <tr>
      <td>사이드바 - 전체 검색</td>
      <td>Ctrl + Shift + f</td>
      <td>Cmd + Shift + f</td>
    </tr>
    <tr>
      <td>에디터 확대</td>
      <td>Ctrl + ( + )</td>
      <td>Cmd + ( + )</td>
    </tr>
    <tr>
      <td>에디터 축소</td>
      <td>Ctrl + ( - )</td>
      <td>Cmd + ( - )</td>
    </tr>
  </table>

* 소스코드 편집
  <table style="width: 100%; border-collapse: collapse; table-layout: fixed;">
    <tr>
      <th>Control</th>
      <th>Window</th>
      <th>Mac</th>
    </tr>
    <tr>
      <td>들여쓰기</td>
      <td>Tab 혹은 Ctrl + &#93;</td>
      <td>Tab 혹은 Cmd + &#93;</td>
    </tr>
    <tr>
      <td>내어쓰기</td>
      <td>Shift + Tab 혹은 Ctrl + &#91;</td>
      <td>Shift + Tab 혹은 Cmd + &#91;</td>
    </tr>
    <tr>
      <td>아래에 행 삽입</td>
      <td>Ctrl + Enter</td>
      <td>Cmd + Enter</td>
    </tr>
    <tr>
      <td>위에 행 삽입</td>
      <td>Ctrl + Shift + Enter</td>
      <td>Cmd + Shift + Enter</td>
    </tr>
    <tr>
      <td>현재 행 이동</td>
      <td>Ctrl + &uarr;/&darr;</td>
      <td>Cmd + &uarr;/&darr;</td>
    </tr>
    <tr>
      <td>현재 행 복사</td>
      <td>Ctrl + Shift + &uarr;/&darr;</td>
      <td>Cmd + Shift + &uarr;/&darr;</td>
    </tr>
    <tr>
      <td>현재 행 삭제</td>
      <td>Ctrl + Shift + k</td>
      <td>Cmd + Shift + k</td>
    </tr>
    <tr>
      <td>주석 토글</td>
      <td>Ctrl + /</td>
      <td>Cmd + /</td>
    </tr>
  </table>

* Visual Studio Code tutorial : https://demun.github.io/vscode-tutorial/shortcuts/




<br>




## Git/Github
* Git 이란
  * 형상관리도구(Configuration Management Tool) 또는 버전 관리 시스템(Version Control System)이라고 한다.

  * 프로젝트를 버전별로 관리를 하거나 수정을 해야될 필요가 생길때 사용하는 시스템이다.

  * 변경된 이력을 확인할 수 있다.

  * 이전 이력으로 되돌리기가 가능하다.

  * 각 기능별로 분업 후 하나의 코드로 합칠 수 있다.

  * 협업으로 인한 실수를 예방할 수 있다.

  * 팀원 간의 커뮤니케이션을 지원한다.

* Git 기반의 서비스
  * Git은 로컬에 설치해서 사용하는 방식

  * 소스들을 공통적인 장소에 저장을 해줘야 하는 서비스가 필요하다. 회사 내의 서버에 저장해두고 사용할 수 있지만, 여러가지 기능들을 제공하고 소스코드를 저장하고 공유할 수 있는 클라우드 호스팅 서비스이다.

  * 대표적인 서비스로는 GitHub, GitLab, Bitbucket 등이 있다.

* 사용자 설정 및 세팅
  * 로컬에서 사용할 Git 사용자 이메일과 이름을 설정

  * git config : Git에 관한 설정을 추가, 변경, 삭제하는 명령어

  * System 설정 파일 : 모든 시스템 사용자에게 적용 ( git config --system )

  * Global 설정 파일 : 한 사용자의 전체 Git Repository에 적용 ( git config --global )

  * Local 설정 파일 : 하나의 Repository에만 적용 ( git config --local )

  * Github 계정에 ssh key 등록하기
    * Github를 생성하고 로컬로 프로젝트를 받아와서 작업을 하기 위해서는 ssh 방식으로 받아와야되는 경우들이 있다.
    * 내 컴퓨터에서 직접 ssh key를 만들어 Github 계정에 등록해주면 사용자를 인식하고 여러가지 작업들을 수행할 수 있다.
    * Github 접속 후 오른쪽 상단 프로필 클릭 Setting -> SSH and GPg Keys
    * New SSH Key 클릭해 Title과 복사한 Key 입력 후 Add SSH Key 클릭

* Git 초기화
  * 명령어 : git init

  * 해당 폴더 안에 들어가는 모든 파일이나 소스코드 파일들을 Git으로 관리하겠다고 선언하는 것

  * Git 초기화 시 폴더 안에 숨김 폴더로 .git 폴더가 생성된다.

* Git 삭제
  * 명령어 : rm -rf .git

  * .git 폴더를 삭제 (Git을 더이상 관리하지 않겠다..)

* Gitignore
  * 사용자가 git에 등록(커밋)되지 않길 원하는 파일 또는 폴더들의 목록을 .gitignore 숨김 파일에 저장

  * .gitignore에 등록된 파일(폴더)들은 커밋 시 자동으로 제외됨

  * 작성법
    * #은 주석의 역할
    * 폴더 : /폴더명 ( ex. /docs )
    * 파일 : 파일명.확장자 ( ex. test.txt )
    * 폴더 안 파일 : /폴더명/파일명.확장자 ( ex. /docs/test.txt )
    * 폴더 안 특정 확장자 파일 전부 ( ex. /docs/*.txt )
    * 폴더 하위 모든 특정 확장자 파일 전부 ( ex. /docs/**/*.txt )

  * .gitignore 작성에 유용한 사이트
    * https://www.toptal.com/developers/gitignore/
    * 프로젝트에 따라서 .gitignore 구조가 달라진다.
    * ex : 검색창에 react 입력 -> 생성 -> .gitignore에 등록해주면 좋은 부분들이 나온다.
    * 복사해서 .gitignore 파일에 붙여넣고 추가적으로 등록하고 싶은 것이 있다면 추가해서 작성

* 기본 동작 원리
  * Working Directory : 현재 작업중인 파일이 있는 디렉토리

  * Staging Area : Git에 등록할(커밋) 파일들이 올라가는 영역

  * Local Repository : 로컬 Git 프로젝트의 메타데이터와 데이터 정보가 저장되는 영역, 여기까지는 PC 영역

  * Remote Repository : Github 등의 서비스를 통한 온라인 상의 저장소, 호스팅을한 온라인 저장소

    <img src="/images/operation.png" alt="기본 동작 원리">

* 기본 용어
  * origin : Remote Repository(Github 등의 온라인 저장소)에 있는 코드
  
  * head : 내가 지금 작업하고 있는 로컬 브랜치
  
  * add : Working Directory에서 Staging Area로 등록하다.
  
  * commit : Staging Area에 등록된 파일을 Local Storage로 등록
  
  * Commit Message : commit 시 함께 작성해 저장하는 메시지 (메모), 협업시 유용하다.
  
  * push : Local Storage에서 변경된 파일들을 Remote Repository로 등록
  
  * fetch : Remote Repository의 변경된 파일들을 Local Repository로 전달
  
  * morge : Local Repository의 변경사항을 Working Directory로 전달
  
  * Branch :독립적으로 어떤 작업을 따로 진행하기 위한 가지
  
  * checkout : 사용할 다른 브랜치를 지정




<br>




## 윈도우 CMD 명령어 목록
  <table style="width: 100%; border-collapse: collapse; table-layout: fixed;">
    <tr>
      <th>Command</th>
      <th>Action</th>
    </tr>
    <tr>
      <td>CD [이동할 경로]</td>
      <td>커맨드창 위치이동</td>
    </tr>
    <tr>
      <td>dir</td>
      <td>현재 위치의 파일과 디렉토리(폴더) 목록 보기</td>
    </tr>
    <tr>
      <td>help</td>
      <td>명령어 도움말 보기 <br>(명령 프롬프트 명령어를 모두 보여준다)</td>
    </tr>
    <tr>
      <td>ipconfig</td>
      <td>네트워크 설정상태 보기 <br>(/all 옵션을 붙여 상세한 설정 정보를 볼 수 있다)</td>
    </tr>
    <tr>
      <td>md [생성할 폴더 이름], mkdir [생성할 폴더 이름]</td>
      <td>디렉토리(폴더) 생성</td>
    </tr>
    <tr>
      <td>rd [삭제할 폴더 이름], rmdir [삭제할 폴더 이름]</td>
      <td>
        디렉토리(폴더) 지우기 <br>
        (/s 입력시 폴더안 파일이 있더라도 삭제가능, 휴지통으로 가지않고 완전삭제이므로 주의해야합니다)
      </td>
    </tr>
    <tr>
      <td>path</td>
      <td>환경변수 path 보기</td>
    </tr>
    <tr>
      <td>cls</td>
      <td>현재 명령 프롬프트 창 초기화 <br>(이전 명령어 결과를 지운다)</td>
    </tr>
    <tr>
      <td>[드라이브 문자열]: <br>(ex. D: -> D드라이브로 변경)</td>
      <td>드라이브 변경</td>
    </tr>
    <tr>
      <td>del [삭제할 파일명]</td>
      <td>파일 삭제 <br>(파일명을 [*.log] 이런식으로 입력하여 여러 파일 삭제 가능하다)</td>
    </tr>
    <tr>
      <td>
        copy [복사할 파일명] [복사할 위치 경로] <br>
        xcopy [복사할 파일명] [복사할 위치 경로]
      </td>
      <td>파일 복사 <br>(xcopy는 숨김파일도 복사할수 있다)</td>
    </tr>
    <tr>
      <td>move [파일명] [이동할 위치 경로]</td>
      <td>파일 이동 <br>(이동한 파일이 이전경로에 남아있지 않는다)</td>
    </tr>
    <tr>
      <td>rename [현재 파일명] [변경후 파일명]</td>
      <td>파일 또는 디렉토리(폴더)명 변경</td>
    </tr>
    <tr>
      <td>date</td>
      <td>현재 날짜 보기 <br>(현재 날짜를 보여준뒤 새로운 날짜를 입력하라고 하면 그냥 엔터치시면 된다)</td>
    </tr>
    <tr>
      <td>tasklist</td>
      <td>현재 실행중인 프로세스 모두 표시</td>
    </tr>
    <tr>
      <td>exit</td>
      <td>재 명령 프롬프트 창 종료</td>
    </tr>
  </table>
