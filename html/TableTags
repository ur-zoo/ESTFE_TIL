# table의 셀
* `table` : 표 생성 시 사용

### tr, th, td
* `tr` : 테이블의 행
  * `th` : 열 제목
  * `td` : 셀 내용

### caption
* 테이블의 제목이나 설명을 의미
* `table`의 첫번째 자식으로 사용
* 선택적으로 사용
* `caption-side` : top, bottom 로 위치를 설정 가능

### thead, tbody, tfoot
* `thead` : 헤더 콘텐츠들을 하나의 그룹으로 묶을 때 사용
* `tbody` : 내용 콘텐츠들을 하나의 그룹으로 묶을 때 사용
* `tfoot` : 푸터 콘텐츠들을 하나의 그룹으로 묶을 때 사용
* 구역을 나누는 요소로 사용
* 선택적으로 사용
* 코드의 가독성을 위해 명시적으로 사용하면 좋음

### colgroup
* 테이블 내의 열 그룹 생성 시 사용

### col
* 테이블 열을 하나 이상 묶을 때 사용
* `colgroup` 요소 내부에 포함
* 선택적 사용
* CSS와 함께 col에 스타일을 지정 가능

<br/>

## 속성값

### scope
* `scope` 속성은 `th` 태그에 사용하여, 테이블의 헤더 셀이 어떤 행이나 열에 속하는지를 명확하게 지정하는 역할
* 접근성 도구가 테이블의 구조를 이해하기 쉽게 해줌
* 행(`row`) 또는 열(`col`), 행그룹(`rowgroup`), 열그룹(`colgroup`)의 속성값으로 셀의 범위를 지정

### colspan, rowspan
* `colspan` : 열 병합
* `rowspan` : 행 병합
* 셀병합 속성

<br/>

## 표 접근성 높이는 법

### scope
* 제목 셀이 명확한 단순한 표에 적용하여 표 구조를  나타냄

### id - headers
* 셀이 병합된 표거나 내용이 많아 복잡한 경우, 제목 셀이 2줄 이상이 되어 복잡한 경우 해당 속성으로 명확하게 연결하는 것이 좋음
* 아예 접근성만을 위해서 쓰는 편

### scope
* 제목 셀이 명확한 단순한 표에 적용하여 표 구조를  나타냄

### id - headers
* 셀이 병합된 표거나 내용이 많아 복잡한 경우, 제목 셀이 2줄 이상이 되어 복잡한 경우 해당 속성으로 명확하게 연결하는 것이 좋음
* 아예 접근성만을 위해서 쓰는 편

<br/>
<br/>

# 표 만들기 (실습)

```html   
    <table>
      <thead>
        <tr>
          <th>구분</th>
          <th scope="col" rowspan="2">한국사 영역</th>
          <th scope="col">국어영역</th>
          <th scope="col">수학영역</th>
          <th scope="col" rowspan="2">언어 영역</th>
          <th scope="colgroup" colspan="2">탐구 영역</th>
          <th>제 2 외국어 / 한문 영역</th>
        </tr>
        <tr>
          <th scope="row">선택 과목</th>
          <th scope="col">화법과 작문</th>
          <th scope="col">확률과 통계</th>
          <th scope="col">생활과 윤리</th>
          <th scope="col">지구 과학 1</th>
          <th scope="col">독일어</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">표준 점수</th>
          <td rowspan="2">&nbsp;</td>
          <td>131</td>
          <td>137</td>
          <td rowspan="2">&nbsp;</td>
          <td>53</td>
          <td>64</td>
          <td rowspan="2">&nbsp;</td>
        </tr>
        <tr>
          <th scope="row">백분위</th>
          <td>93</td>
          <td>95</td>
          <td>75</td>
          <td>93</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <th scope="row">등급</th>
          <td>2</td>
          <td>2</td>
          <td>2</td>
          <td>1</td>
          <td>1</td>
          <td>2</td>
          <td>2</td>
        </tr>
      </tfoot>
    </table>
```         
              
![
  표 만들기 실습 완성본
](img/blog/section.png)
