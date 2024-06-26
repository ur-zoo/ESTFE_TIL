# CSS 선택자 우선순위

## 1. 후자우선의 원칙

- 뒤에 나오는 CSS가 우선순위가 높음
- 동일한 선택자에 동일한 속성이 사용되었을 경우 뒤에 적힌 속성을 따르게 함

## 2. 구체성의 원칙

- 어떤 선택자가 더 구체적인지가 기준
- **가중치**
    1. inline 스타일 속성
    2. id
    3. class, 가상 클래스, 속성 선택자
    4. type, 가상 요소 선택자
    - 순서대로 가중치가 높음
- **우선 순위 계산**

| inline-style | 1000점 |
| --- | --- |
| id 선택자 # | 100점 |
| class ., 가상클래스, 속성선택자 | 10점 |
| 타입, 가상요소 선택자 | 1점 |
| 전체선택자 * | 0점 |

## 3. 중요성의 원칙

- `!important`
    - 상속을 깨트리기 때문에 오류와 버그 발생 시 수정을 어렵게 만듦
    - 다른 CSS의 어떤 선언보다도 우선함
    - 선택자 우선순위에 직접적인 영향
