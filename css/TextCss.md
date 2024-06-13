# 텍스트 Style

## color
- 폰트의 색상
- -font가 붙지 않으니 주의
- 키워드, HEX, rgb(), rgba(), hsl(), hsla() 등의 방법으로 표기
- transparent : 투명한 색

### curentColor
- 저시력 시각 장애를 위해 폰트의 색상과 배경의 명도 대비도 중요함
- 최소한 4.5:1

## font-family 글꼴 종류
- 사용자의 컴퓨터에 설치되어있지 않은 글꼴을 사용자가 웹 사이트에 접속했을 때 다운로드 시키는 방법
- 3개 정도로 지정을 하는데, 글꼴이 사용자 시스템에 없는 경우 다른 글꼴로 대체하기 위함임

### 1. link로 삽입

```html
<head>
		<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300&display=swap" rel="stylesheet">
    <style> 
				body {font-family: 'Noto Sans KR', sans-serif;}
		</style>
</head>
```

### 2. import로 삽입

```css
@import url("https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300&display=swap");

body{
	font-family: "Noto Sans KR", sans-serif;
}
```

### 3. font-face

```css
@font-face {
    font-family: "Pretendard-Regular";
    src: url("https://cdn.jsdelivr.net/gh/Project-Noonnu/noonfonts_2107@1.1/Pretendard-Regular.woff") format("woff");
    font-weight: 400;
    font-style: normal;
}
body{
	font-family: Pretendard-Regular, "Times New Roman", Dotum, "돋움", sans-serif;
}
```

### 3-1. 웹폰트 업로드 후 사용하기

저장한 폰트 사용

```css
@font-face {
    font-family: "Pretendard-Regular";
    src: url("./font/Pretendard-Regular.woff") format("woff");
    font-weight: 400;
    font-style: normal;
}
```

<aside>
🙋‍♀️ **폰트를 `“”` 으로 묶은 것도 있고 그렇지 않는 것도 있는데 왜 그런건가요?**

1. 한글일 경우에는 `""` 를 사용합니다.
2. 영문이지만 공백이 포함될 경우 `""` 를 사용합니다.
3. 한글폰트의 한글 이름, 영문이름을 제대로 인식 못하는 경우를     대비해서 한글과 영문명을 같이 작성해 주는 것이 좋습니다.
4. generic(sans-serif, serif와 같은 기본 폰트)인 경우 `""` 를 사용하지 않습니다
5. 한글은 한글 폰트로, 영문은 영문폰트으로 나오길 원한다면, 영문폰트명, 한글폰트명 순으로 적어줍니다!

</aside>

[Google Fonts](https://fonts.google.com/)

[눈누](https://noonnu.cc/)

## font-size

---

- px, em, rem

## font- weight

---

- 텍스트 굵기 설정
- `normal`: 기본
- **`bold`**: 굵게 700
- `lighter`: 현재 요소의 굵기를 부모 요소 굵기 보다 한 단계 가볍게
- `bolder`: 현재 요소의 굵기를 부모 요소 굵기 보다 한 단계 두껍게
- **`100` - `900` : 세밀하게 조정 가**

## text-transform

---

- 영문자에만 적용됨
- `none`: 변형되지 않
- **`uppercase`**: 모든 텍스트를 대문자로
- **`lowercase`**: 모든 텍스트를 소문자로
- `capitalize`: 모든 단어의 첫글자를 대문자로

## test-decoration

---

### text-decoration-line

- **`underline`**: 밑줄 긋기
- `overline`: 글 위에 줄 긋기
- `line-through`: 취소선
- `none` : 선 없음

### text-decoration-color

- 밑줄의 색 또는 불투명도 등을 지정

### text-decoration-style

- `solid` : 정석 밑줄
- `double` : 더블 밑줄
- `dotted` : 촘촘한 점선 밑줄
- `dashed` : 느슨한 점선 밑줄
- `wavy` : 물결 밑줄

### text-decoration-thickness

- 점선의 굵기를 px로 지

## text-shadow

---

- 텍스트에 그림자를 추가
- 축약형
- `offset-x | offset-y | blur-radius | color`
- `box-shadow` 는 상자 그림자를 나타냅니다
- https://cssgenerator.org/text-shadow-css-generator.html

        : 그림자 코드 만들어주는 사이트

## text-align

---

- 텍스트의 가로정렬을 설정
- `left` : 왼쪽 정렬
- `right` : 오른쪽 정렬
- `center` : 중앙 정렬
- `justify` : 양쪽정렬
- `justify-all`: 양쪽정렬(마지막 줄 적용)

## vertical-align

---

- 텍스트의 세로 정렬을 지정
- 인라인, 인라인 블록 및 테이블 셀 요소에만 적용됨
- 블록 레벨 요소를 수적으로 정렬하는 데 사용할 수 없다
- 블록 레벨에서 수직정력하고 싶다면 추후 배울 flex를 사용하면 됨
- 그다지 사용하지 않는 속성

```css
      .baseline {
          vertical-align: baseline;
      }
      .sub {
          vertical-align: sub;
      }
      .super {
          vertical-align: super;
      }
      .text-top {
          vertical-align: text-top;
      }
      .text-bottom {
          vertical-align: text-bottom;
      }
      .middle {
          vertical-align: middle;
      }
```

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8f11927-b70c-4524-9227-a3efac08e7aa/90b49799-4eb3-475a-b4bd-75e22694cdb7/Untitled.png)

## line-height

---

- 행간을 설정
- `line-height`의 기본값 : 보통 `1.5`를 많이 사용
- 단위, 배수, % 등의 값으로 설정
    - 배수 : 글자 크기를 기준으로 해서 배수

## letter-spacing

---

- 자간을 설정
- 단위 값으로 설정

## word-spacing

---

- 단어와 단어 사이의 간격 설정
- 단위 값으로 설정

## text-indent

---

- 문단 첫째줄의 들여쓰기 길이를 설

## word-break

---

- 텍스트가 자신의 콘텐츠 박스 밖으로 넘칠 경우 줄바꿈 여부를 지정
- normal 기본 줄 바꿈 규칙 사용
- break-all 글 넘침을 방지하기 위해 어떠한 두 문자 사이에서도 줄바꿈이 발생할 수 있음
    - 한중일 텍스트 제외
- keep-all 한줄일 텍스트에서 줄 바꿀 때 단어를 끊지 않음
    - 비 한중일 텍스트에서는 노멀과 동일
- br 태그 넣으면 안 됨

## text-overflow

---

- 텍스트가 넘칠 경우 어떻게 표시할지 설정
- 말줄임 처리할 때 자주 사용
- ellipsis : 말 줄임

```css
.ellipsis{
  white-space:nowrap;
  overflow:hidden;
  text-overflow:ellipsis;
} /* 한 줄 말 줄임 처리 */

.multi-ellipsis{
  overflow:hidden;  
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3; /* 이게 줄의 수 */
} /* 보이고 싶은 줄의 수 지정 가능 */
```

## font-style

---

- 이탤릭체 사용
- 기울임 글꼴

## font(단축 속성)

---

- font: `font-style` `font-variant` **`font-weight`** `font-stretch` **`font-size`/`line-height`** **`font-family`**
- 순서 중요합니다!
- `line-height` 는 font-size를 꼭 적고 사용해주세요!
- 잘 사용하지 않음
