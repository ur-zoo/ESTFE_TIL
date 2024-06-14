# CSS Box Model

![CssBoxModel.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8f11927-b70c-4524-9227-a3efac08e7aa/29f76665-df92-49e0-be70-6459e48eb56e/CssBoxModel.png)

- html 요소를 감싸는 상자
- 요소, 패딩, 테두리, 마진으로 구성
- CSS box model 은 블록박스에 적용되며, 인라인 박스는 박스 모델에 정의된 일부 동작만 사용함
    - inline 요소는 width, height, 상하 margin 값이 적용되지 않음

## width

- 요소의 너비
- 기본값은 콘텐츠 영역의 너비지만, box-sizing 속성을 사용하여 테두리 영역을 너비 설정
- auto 기본값
- min-content

## height

- 요소의 높이

## padding

- 단축 속성
- pading-top padding-right padding-bottom padding-left 순으로 작성함

## margin

- 단축 속성
- margin-top margin-right margin-bottom margin-left 순으로 작성

### 마진병합 현상

- 요소와 요소 사이 마진 값의 공간이 있을 경우 더 높은 값의 마진 값이 적용되는 현상
- 부모 요소와 자식 요소가 존재할 때, 자식 요소의 마진 값이 부모의 높이에 영향을 주는 현상
- **해결방법**
    - 부모 요소에 overflow 속성 값 적용하기
    - 부모 요소에 display: inline-block 값 적용하기
    - 부모 요소에 border 값 적용하기
    - 부모 요소에 display:flow-root 사용하기 (IE 지원 안 )

## border

- 테투리 지정
- 요소가 차지하는 전체 너비와 높이의 일부
- 단축속성
- 선의 두께와 스타일, 색상을 지정할 수 있

## box-sizing

- content-box : 기본값이며, width, height에 border, padding을 포함하지 않음
- border-box : width, height에 border, padding을 포함함
    - width =  콘텐츠 너브 + border + padding

## over, overflow-x, overflow-y

- 박스보다 콘텐츠가 더 커 콘텐츠가 넘치 경우 어떻게 처리할지 지정함
- visible : 기본값, 박스를 넘는 컨텐츠를 자르지 않음
- hidden : 요소의 크기만큼 맞추기 위해 잘라내며, 스크롤바를 제공하지 않음
- scroll : 요소의 크기만큼 잘라내고, 스크롤을 제공
- auto : 자동으로 콘텐츠가 넘칠 경우 스크롤바를 노출
