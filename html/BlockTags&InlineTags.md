# 블록 태그
* 자신의 내용과 앞뒤 태그의 내용을 다른 라인에 출력하는 태그
* 자신의 내용만으로 한 라인을 독점해서 출력하는 태그
* 페이지의 구조적 요소를 나타날 때 사용
* `width`, `height` 크기 지정 가능하며, `padding`, `border`, `margin` 스타일 속성 사용 가능
* 블록요소는 인라인 요소 안에 중첩 될 수 없지만, 인라인 요소는 블록 요소 안에 중첩 가능
    * 인라인요소 중에 `a` 태그의 경우, 안에 블록 요소 중첩 가능

### div
* 레이아웃을 만들 때 주로 사용하며, 상당히 광범위하게 사용
* 공간을 나누는 것 외에 특별한 기능하지 않음
* div 태그 사용은 스타일 적용을 위한 용도로 사용할 것을 권장
* 오래된 웹 브라우저의 호환을 위해서 아직 사용 중
* `div`가 `p`보다 그릇이 큼

### figure
* 주변 콘텐츠의 이해나 흐름과 관련된 이미지, 그림, 도표, 사진, 코드 목록 또는 기타 관련 콘텐츠 등의 독립된 콘텐츠를 나타내는 태그
    * 독립된 콘텐츠 : 콘텐츠가 없어도 맥락의 흐름에 지장이 없이 이해나 흐름과 관련된 자체적인 콘텐츠
    * 즉, 본문과 관계가 있어야 하지만 없어도 딱히 상관 없을 때 사용
* 이미지뿐만 아니라 코드 조각, 인용문 등에도 사용 가능
* `figcaption`를 사용해 캡션(설명) 추가 → 선택 사항

### figcaption
* `figure`의 콘텐츠를 참조할 수 있는 캡션(설명)이나 범례을 나타내기 위해 사용하는 태그
* 선택적으로 사용할 수 있으나, `figure`의 첫번째 자식 요소나 마지막 자식 요소로만 사용

<br/>
<br/>

# 인라인 태그
* 내용물의 크기가 태그의 영역
* `width`, `height` 크기 지정 불가
* `padding`, `border`, `margin` 속성을 사용은 가능하나, 상하 `margin` 속성은 사용 불가
* 항상 블록 레벨 요소 내에 포함
* 어디에 들어가도 줄바꿈 등이 일어나지 않음

### span
* 자체적인 특별한 의미가 없는 인라인 컨테이너
    * 본질적으로 아무것도 나타내지 않음
* 스타일을 적용하거나 인라인 요소를 묶을 때 사용
* 본인만 적용
* 줄바꿈 없음

### img
* 문서에 이미지를 삽입하는 역할
* `src` : 필수이며, 이미지의 경로 지정
* `alt` : 이미지의 텍스트 설명으로, 선택은 아니지만 접근성 차원에서 매우 유용
    * 네트워크 오류, 콘텐츠 차단, 죽은 링크 등 이미지를 표시할 수 없는 경우에 이 속성의 값을 대신 보여줌
* `title` : 이미지에 대한 추가 정보를 제공하는 텍스트 지정
    * 마우스를 이미지 위에 올리면 툴팁으로 표시됨
    * `alt` 의 값을 `title` 에 사용하는 것을 피해야 함
* `img` 태그만 사용해야 하는 경우
    * 단순히 이미지를 표시할 때 (내용과 상관 무)
    * 본문의 일부로 이미지가 꼭 필요할 때

### map
* 이미지 맵을 정의하는 태그

### area
* 미지 맵 내의 클릭 가능한 영역을 정의하는 태그 <br/>
❗ [image-map](https://www.image-map.net/) : 이미지 맵 무료 생성 사이트 (클릭 시 이동)

<br/>
<br/>

# inline-block
* 기본적으로 인라인 요소의 속성을 따르면서 너비와 높이를 조절까지 가능함
* 인라인 요소처럼 전후 줄바꿈 없이 한 줄에 다른 요소들과 나란히 배치
* 블록 요소처럼 너비와 높이 지정 및 `margin`, `padding` 상하 간격 지정 가능
* `button`, `input`, `select` 등이 있음

|  | block | inline | inline-block |
| --- | --- | --- | --- |
| 요소 포함 | 인라인 요소                                              포함 가능 | 블록 요소                            포함 불가 (a 가능) |                     - |
| 줄 바꿈 | O (세로로 쌓임) | X (가로로 쌓임) | X (가로로 쌓임) |
| width, height | O | X | O |
| padding | O | O | O |
| margin | O | left, right만 적용 가능 | O |
| border | O | O | O |