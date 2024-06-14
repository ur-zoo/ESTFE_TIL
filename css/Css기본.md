# CSS

- *Cascading Style Sheets* 의 약자
- 웹 페이지의 스타일을 정리해둔 문서
- 두 가지 이상의 스타일이 있을 때, 이미 규정된 우선순위를 가지고 적용이 됨
- css를 한 번 작성해 여러번 재사용할 수 있음

## 작성 방법

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8f11927-b70c-4524-9227-a3efac08e7aa/91461368-96d9-453e-8fab-6ca4ae458790/Untitled.png)

## 주석

- css의 주석처리 : /* 주석 */

# CSS 적용 방식

## 인라인 방식

: 태그 자체에 `style` 속성으로 직접 명시해주는 방식

- 가상 요소 등에 스타일을 줄 수 없어 사용에 제한이 있음
- 이 방식을 권고하지는 않음 (단일 스타일 적용 시 종종 사용)

## 내부 스타일

: html 문서 head 태그 안에 style 태그를 사용하는 방식

- 코드가 길어질수록 파일 길이가 길어지기 때문에 효율적이지 않음
    - 즉, 잘 사용하지 않음

## 외부 스타일

: css 문서에 스타일을 적은 후에  html 문서와 `link` 태그를 사용해 연결시켜주는 방식

- 현업에서 가장 많이 쓰이며, 권장하는 방식

```html
<!DOCTYPE html>
<html lang="ko-KR">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title></title>
        <!-- rel : 관계 / href : 경로 -->
        <link rel="stylesheet" href="3.css">
    </head>
    <body>
        <p>hello World</p>
    </body>
</html>
```

```css
p {
    color: white;
    background-color: black;
}
```

## 다중 스타일 시트

: css 내부에  @inport 구문을 사용하여 연결한 후, html로 `link`를 이용해 하나의 css만 연결해주면 됨

- css 문서 최상단에 위치해야 함
- 성능 측면에서는 파싱하기 위한 시간이 더 증가하기 때문에 권장하지는 않음

```html
<!-- index.html -->
<!DOCTYPE html>
<html lang="ko-KR">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>외부 스타일</title>
	<link rel="stylesheet" href="style.css">
</head>
<body>
	<p>Hello world</p>
</body>
</html>
```

```css
/* style.css */
@import url("reset.css");
@import url("font.css");
@import url("layout.css");
@import url("main.css");
```

# CSS 선택자

## 전체 선택자 ( * )

- html를 포함한 문서 내의 모든 요소를 선택함

## 타입(유형) 선택자

- 특정한 태그를 선택함
- 선택자 부분에 선택하고 싶은 태그 적은 후 {}

## 아이디 선택자 ( # )

- html 페이지 내에 id 속성값은 유일해야 함
- css 지정을 하는 경우, 아이디 보다는 클래스를 많이 사용
- Js 또는 해시 링크과 함께 사용되는 경우가 많음

## 클래스 선택자 ( . )

- 한 페이지에 여러 개의 클래스 선택자가 존재할 수 있음
    - 따라서 재사용성이 높고, 제일 사용을 많이
    - 하나의 태그에 여러 개의 클래스를 줄 수 있음

<aside>
👉 - id와 class는 숫자 시작할 수 없다.

- 하이픈, 언더바, 문자로는 시작할 수 있다.

</aside>

## 특성 선택자 ( [ ] )

- 주어진 특성을 가진 모든 요소를 선택
- 앞에 태그 선택자를 넣으면 특정 태그를 가지고 특성을 가진 모든 요소를 선택함

```html
<!DOCTYPE html>
<html lang="ko-KR">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title></title>
        <style>
            [type="button"] {
                /* cursor: pointer = 마우스 포인터가 변경되는 속성 */
                border: 0;
                cursor: pointer; 
                color: brown;
            }

            /* ^는 ~~로 시작한다는 의미 */
            [class^="btn"] {
                background-color: brown;
                color: aliceblue;
            }

            /* $는 ~~로 끝난다는 의미 */
            [class$="btn"] {
                background-color: aqua;
                color: azure;
            }
        </style>
    </head>
    <body>
        <input type="text" value="button">
        <input type="button" value="button">
        <input type="text" class="btn-first">
        <input type="text" class="second-btn">
    </body>
</html>
```

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8f11927-b70c-4524-9227-a3efac08e7aa/ed43e887-27d3-43ed-aba1-57d2897155bd/Untitled.png)

## 그룹 선택자 ( , )

```css
h1, h2, h3, h4, h5, h6{ font-weight:bold;}
```

## 복합 선택자

### 자손 선택자

- 기준이 되는 태그의 자식과 자손까지도 모두 선택
- 공백과 띄어쓰기를 통해 구분

### 자식 선택자

- 직계 자손만을 선택
- > 를 통해 구분

### 일반 형제 선택자

- 태그 뒤에 나오는 형제만 선택
- ~ 를 통해 구분

### 인접 형제 선택자

- 바로 뒤에 인접한 형제만 선택
- + 를 통해 구분

# 상속

:  하위 요소에 스타일이 지정되지 않았을 때, 상위 요소의 스타일이 하위 요소에도 적용되는 것

- 상속되지 않는 속성 :  `width`, `height`, `margin`, `padding`, `border` 등

## 상속을 제어하기 위한 속성값

- `inherit` : 상속되지 않는 속성도 상속을 받게 해주는 속성값
- `initial` : 상속을 따르지 않고 초깃값으로 설정하는 속성값
- `unset` : 자연적으로 상속되면 `inherit` 된 것처럼 아니면 `initial` 처럼 작동하는 속성값
- form 관련 태그들은 상속받지 않기도 함
    - 브라우저별로 적용된 스타일이 있기 때문
