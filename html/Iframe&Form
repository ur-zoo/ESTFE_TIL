# iframe

* 현재 웹페이지에 다른 HTML 페이지를 포함시켜 중첩하는 기능을 제공
* **iframe 속성**
    * src : 삽입될 문서의 주소
    * width : 너비 지정(px,%)
    * height : 높이 지정(px,%)
    * title : 콘텐츠의 제목을 지정합니다. 접근성을 위해 사용하는 것이 좋습니다
    * frameborder : 테두리 표시 여부(0: 테두리 있음, 1: 테두리 없음)
    * scrolling : 스크롤바 표시 유무(yes,no,auto)
    * longdesc : 내용을 설명하는 페이지
    * marginwidth : left(좌), right(우), 여백공간(margin)
    * align : 정렬(top, middle, bottom, left, right)
    * allow : iframe 에서 허용할 기능들을 지정합니다.
    * allowfullscreen : 전체화면을 지원합니다.
* 일부 사이트에서는 아이프레임을 거부하기도 함
    * 보안상의 이유, 클릭재킹 , 브랜드 이미지 보호나 다른 이유 등등

# form

* 사용자로부터 입력을 받기 위한 양식을 작성하는 태그들을 통틀어 form이라 부름
* 별도로 제출할 필요가 없다면 form 태그를 사용하지 않아도 됨
    * ex) 단순히 입력받은 값을 화면에 뿌려주는 용도일 경우

## method 속성

---

- 양식을 제출할 때 사용할 HTTP 메서드
- **get**
    - 양식 데이터를 action URL과 ? 구분자 뒤에 이어 붙여서 전송
    - GET 방식의 HTTP 요청은 브라우저에 의해 캐시되어 저장 브라우저 히스토리 등에 저장
        - 보통 쿼리 문자열에 포함되어 전송되므로 길이의 제한이 있음
        - URL 길이제한은 브라우저마다 다름
    - 보안상 취약점이 존재하므로, 중요한 데이터는 POST 방식을 사용하여 요청
- **Post**
    - 폼 데이터를 별도로 첨부하여 서버로 전달하는 방식
    - 브라우저에 의해 캐시되지 않고, 브라우저 히스토리에도 남지 않음
    - POST 방식의 HTTP 요청에 의한 데이터는 쿼리 문자열과는 별도로 전송
    - 데이터의 길이제한이 없고, GET 방식보다 보안성이 높음
    - enctype 속성 (데이터의 포장을 어떻게 할지 지정하는 것)
        - text/plain : 디버깅용 및 단순 텍스트 전송, 단순하게 개발용으로만 사용 권장
        - application/x-www-form-urlencoded : 기본값
        - multipart/form-data : <input type="file">이 존재하는 경우 사용

|  |                                    POST |                                     GET |
| --- | --- | --- |
|           전송 |  양식 데이터를 요청 본문으로 전송 |  https://example.com?name=홍길동&age=20 |
|           캐시 |  X |  O |
|       길이 제한 |  X |  O |
|           보안 |  Get 방식보다 높음 |  취약 |

## action 속성

---

- 양식 데이터를 처리할 프로그램의 URL을 적어줌
- 데이터를 어디로 보낼것인지 지정 (반드시 유효한 URL 이어야 함)
- 이 속성을 지정하지 않으면 데이터는 form이 있는 페이지의 URL로 보내줌

## autocomplete 속성

---

- 입력요소가 자동완성된 값을 기본값으로 가질 수 있는지 나타냄. = 자동완성
- 이전에 해당 양식의 입력된 값이 있을 경우(브라우저에 기록이 남아있을 경우 나타남)
- off : 자동 완성 X / on : 자동 완성 O(기본값)

# input

---

### 공통 속성

- **type**
    - input 양식 컨트롤의 유형
- **name**
    - 각 폼 요소에 고유한 이름을 부여함
    - 서버가 어떤 데이터인지 식별할 수 있게 해줌
    - 필수적으로 설정됨
- **value**
    - 사용자가 입력한 값이나 기본 값, 초기 값
    - 폼이 제출될 때, name 값과 함께 서버로 전송됨
- **autocomplete**
    - on, off 양식 자동완성 기능에 대한 힌트
- **palceholder**
    - 양식 컨트롤이 비어있을 때 나타나는 내용
- **requied**
    - 양식 전송을 위해 필수로 입력해야 하는 값
- **disabled**
    - 비활성화
    - 사용자가 입력할 수 없으며, value가 있어도 넘길 수 있음 = 제출 불가
- **readonly**
    - 수정 불가 (읽기 전용)
    - 사용자가 입력할 수 없으나, value가 있다면 값을 넘길 수 있음 = 제출 됨

---

### input 유형

```html
<!-- 기본 행동 없음. 그냥 버튼임. -->
<input type="button" value="버튼입니다."> <br />

<!-- 텍스트 입력 -->
<input type="text"> <br />

<!-- 이메일 입력 (text로 설정한 것보다 코드 가독성이 더 좋아짐) -->
<input type="email"> <br />

<!-- 전화번호 입력 -->
<input type="tel"> <br />

<!-- 비밀번호 입력 (값 숨김) -->
<input type="password"> <br />

<!-- 단일 값을 선택하거나 선택 해제 -->
<input type="checkbox"> <br />

<!-- 선택 항목 중 하나만 선택 -->
<input type="radio"> <br />

<!-- 날짜 입력 (년, 월, 일) -->
<input type="date"> <br />

<!-- 날짜와 시간 입력 -->
<input type="datetime-local"> <br />

<!-- 연도와 월 입력 -->
<input type="month"> <br />

<!-- 시간 -->
<input type="time"> <br />

<!-- 파일 업로드 -->
<input type="file"> <br />

<!-- 색 선택 -->
<input type="color"> <br />

<!-- 슬라이드 바 형태 -->
<input type="range"> <br />

<!-- 검색 문자열 입력 -->
<input type="search"> <br />

<!-- form 내용을 기본값으로 초기화 -->
<input type="reset"> <br />

<!-- 제출 버튼 생성 -->
<input type="submit"> <br />

<!-- 보이지는 않지만 값은 서버로 전송하는 컨트롤 -->
<input type="hidden"> <br />
```

![input 유형.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8f11927-b70c-4524-9227-a3efac08e7aa/bb34ae19-6ce7-49fa-8045-9d8f0231c841/input_%EC%9C%A0%ED%98%95.png)

- **button, reset, submit**
    - <button type=”___”> 태그와 동일한 기능을 수행

```html
<!-- 박스 안에 텍스트만 넣을 수 있음 -->
<input type="button" value="버튼">
<input type="reset" value="초기화">
<input type="submit" value="전송">

<!-- 텍스트 외의 다른 것들도 박스 안에 넣을 수 있음 -->
<button type="button">버튼</button>
<button type="reset">초기화</button>
<button type="submit">전송</button>
```

- **text / password / url / search / tel**

```html
<!-- maxlength : 문자수 최대 길이 -->
<input type="text" maxlength="20">

<!-- minlength : 문자수 최소 길이 -->
<input type="text" minlength="20">
```

- **checkbox / radio**
    - checkbox
        - 다중선택 가능
    - raido
        - 다중 선택 불가
    - checked
        - 체크 여부

- **file**
    - 파일 업로드 가능
    - accept : 허용하는 파일 유형을 지정할 수 있음
    - multiple : 지정할 경우 사용자가 여러개의 파일을 선택할 수 있음
    - 커스텀 방법
        - input 태그는 css로 안 보이게 한 후 lable 태그 연결하고 lable 태그를 커스텀 하기

- **number**
    - 숫자 입력. 화살표 컨트롤 제공
    - max : 최대값
    - min : 최소값
    - step : 증가값

- **label**
    - 사용자 인터페이스의 항목을 나타냅니다.
    - input과 함께 사용해주세요!
        - 스크린리더기에서 입력해야 하는 내용이 무엇인지 사용자에게 쉽게 이해할 수 있게 합니다.
        - label을 클릭하여 input에 포커스를 이동시키거나 활성화 시킬 수 있습니다.

- **select**
    - 드롭다운 메뉴를 생성
    - multiple : 여러개의 항목을 동시에 선택할 수 있습니다. 리스트박스처럼 보이게 됨
    - size : 한번에 노출되는 항목의 수를 조절
    - required : 선택 필수
    - disabled : 선택 불가

```html
<select name="" id=""> 
	<optgroup label="직업 선택">
	  <option value="Designer">웹 퍼블리셔</option>
	  <option value="FE">프론트엔드 개발자</option>
	  <option value="BE">백엔드 개발자</option>
  </optgroup>
</select>
```

![select.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8f11927-b70c-4524-9227-a3efac08e7aa/3f31d58b-6c70-4a76-8b98-c50ba1a6abfe/select.png)

- **optgroup**
    - `option` 요소를 `optgroup` 요소 안에 배치하면 드롭다운 내에서 옵션그룹을 나눌 수 있음
    - select를 클릭했을 때의 모습 등 원하는 모습으로 완전히 커스텀 하기에는 어려움
        - 그래서 커스텀을 원한다면, select가 아닌 다른 html 요소들과 JavaScript 등을 사용해 완전히 별도의 드롭다운 메뉴를 만들어야 함
- **option**
    - 메뉴의 각 옵션을 정의
    - 모든 `option` 은 자신이 선택됐을 때의 값으로 사용할 value 속성이 필요
        - 지정하지 않은 경우, option 내 텍스트 값으로 사용
    - selected 특성을 지정하면 해당 옵션을 선택한 상태로 페이지를 불러옴

### 크로스브라우징

웹 개발에서 웹사이트나 웹 애플리케이션이 여러 웹 브라우저에서 동일하게 보이고 작동하도록 하는 기술이나 방법

이는 다양한 브라우저 간의 호환성을 확보하여, 사용자가 어떤 브라우저를 사용하더라도 일관된 사용자 경험을 제공하기 위해 중요
