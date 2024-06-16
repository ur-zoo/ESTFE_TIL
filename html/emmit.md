# 알고 가기

### Web
* 공용 웹페이지의 상호 연결 시스템
* 인터넷을 기반으로 한 서비스 <br/>
&nbsp; &nbsp; :  web, 파일 전송 등이 인터넷에 포함됨

### Internet
* 네트워크와 네트워크가 모인 것
* 여기서 네트워크는 컴퓨터와 컴퓨터를 연결해주는 망임

### HTML
* 프로그래밍 언어가 아닌 콘텐츠의 구조를 정의하는 마크업 언어임
* 확장자 : `.html`

### CSS
* 웹페이지의 스타일임
* 확장자 : `.css`

### JS
* 웹페이지의 기능 및 동작임
* 확장자 : `.js`

### HTML5
* 최신 웹 기술을 가르키는 유행어
* 기존 버전의 단점을 없애고 개발자에게 가능성과 유연성을 제공함
* Living standard <br/>
&nbsp; &nbsp; : HTML의 최신 버전을 지속적으로 업데이트하는 방식을 가진 HTML의 유일한 버전

<br/>
<br/>
<br/>

# 에밋 해석

### 에밋
* 웹 개발 시 필요한 플러그인임
* ! + tab 누르면 자동 생성 (언어코드 : en)

```html   
<!DOCTYPE html>
<html lang="ko-KR">
  <head>
    <meta charset="utf-8">
		<meta http-equiv="X-UA-Compatible" content="IE=edge" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My test page</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image">
		<script src="./script.js"></script>
  </body>
</html>   
```

### !DOCTYPE html
* html living standard 문서라는 선언문이며, 문서 최상단에 위치함
* 완전 표준 모드로 렌더링 되며, 제거 시 쿼크 모드로 렌더링 됨
&nbsp; &nbsp; : 쿼크 모드는 브라우저마다 구현 방식이 다르기 때문에 작동 시 다르게 작동될 수 있음

### html
* 최상위 태그이며, 잘못된 언어를 지정하면 오류가 남
* 주 언어를 설정할 수 있으며, 검색엔진과 스크린리더, 번역 기능 등에 영향을 끼침
* 언어 코드 : 소문자 / 국가 코드 : 대문자 로 설정해야 함

|          언어코드 |              언어 |                                               국가코드 |
| --- | --- | --- |
|               ko |            한국어 |   KR(대한민국), KP(북한) |
|               en |              영어 |   US(미국), GB(영국), PH(필리핀)  |
|               zh |            중국어 |   CN(중국), HK(홍콩), TW(대만), Hans(간체), Hant(번체) |
|            ja, de |        일본어, 독일 |   X |

### body
* 사용자에게 보이는 영역이다.

### head
* 기계가 식별할 수 있는 문서 정보를 담음
* 사용자에게는 제목과 파비콘, 뷰포트 정보 등이 보이게 됨

#### meta
* 메타데이터란? 어떤 목적을 위해 만들어진 데이터를 말함
* meta charset="utf-8"
    * 어떤 언어로 작성하더라도 웹페이지를 읽을 수 있게 하며, 국제적 코드 규약임
* meta http-equiv="X-UA-Compatible" content="IE=edge"
&nbsp; &nbsp; * IE의 최신 포준 모드를 보여주겠다는 의미
* meta name="description" content="”
    * 어떤 페이지인지 정보를 수집하게 해줌
    * name : 화면 전체 페이지에 적용되는 '문서 레벨 메타데이터'
    * content : 실제 메타데이터의 요소
* meta name="viewport" content="width=device-width, initial-scale=1.0"
    * width : "viewport"의 너비를 제어
    * height : "viewport"의 높이를 제어
    * initial-scale : 페이지가 처음 로드될 때 확대 및 축소 수준을 제어
    * minimum-scale : 축소 정도를 제어
    * maximum-scale : 페이지에 허용되는 확대 정도를 제어
    * user-scalable=no : 특수한 상황이 아니라면 사용하지 않는 것이 좋음

#### title
* 작업 표시줄이나 페이지 탭에 보이는 문서 제목이며, 특수문자는 넣지 않음
* 약 60자를 넘지 않아야 함
* 핵심 내용을 넣어두는 것이 좋음

#### link
* 현재 문서와 외부 리소스의 관계를 명시
* 스타일시트나 폰트 등등을 추가해줄 때에 링크 태그를 통해 연결
* 한 줄로 체러되는 빈 태그이며, 속성만을 포함
* rel : 관계 대상 파일의 속성
* href : 연결 시 참조할 파일의 위치
