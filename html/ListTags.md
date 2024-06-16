## ul
- **정렬되지 않은 비순차적 목록이며, 보통 불릿으로 표현**
- 순서가 중요하지 않는 목록에 적용
    - **항목의 순서를 바꿨을 때 의미가 바뀌면 `ol`, 그렇지 않으면 `ul` 사용**

## li
- **목록의 항목**을 나타냄
- `ol`과 `ul`의 자식요소로만 사용 가능 (단독 사용 불가)
    - `ol`과 `ul` 또한 자식요소로는 `li`만 사용할 수 있으며, 자손요소로는 다른 태그도 가능

- **ol에 사용된 li 특성**

<aside>
<img src="/icons/arrow-down-basic_gray.svg" alt="/icons/arrow-down-basic_gray.svg" width="40px" /> `type`: 넘버링 타입을 나타내는 문자로, ol 요소에서 지정하는 유형을 덮어씀

- `1`: 숫자(기본값)
- `a`: 소문자 알파벳
- `A`: 대문자 알파벳
- `i`: 소문자 로마 숫자
- `I`: 대문자 로마 숫자
- `value`: 항목의 현재 서수 값을 나타내는 정수
</aside>

[data:image/gif;base64,R0lGODlhAQABAIAAAP///wAAACH5BAEAAAAALAAAAAABAAEAAAICRAEAOw==](data:image/gif;base64,R0lGODlhAQABAIAAAP///wAAACH5BAEAAAAALAAAAAABAAEAAAICRAEAOw==)

## dl
- **설명 목록**을 나타냄
- ‘`dt` : 용어, `dd` : 용어 설명’ 을 감싸 설명 목록을 나타냄
- 주로 용어사전 구현, 메타데이터(키-값 쌍의 목록)을 표시할때 사용
- 여러 개의 용어와 하나의 설명, 하나의 용어 하나의 설명도 가능
- `dl`, `dt`, `dd`는 이미 정의 되어 있거나 정해져 있는 경우에만 사용할 수 있음
    - 메뉴나 form에 사용 불가

## dt
- `dl`과 함께 사용하며, **설명 목록의 용어**를 나타냄
- `dl`의 자식, 자손이 아닌 단독으로는 사용 불가
- `dd` 요소가 `dt` 용어의 정의나 기타 관련 글을 제공함
- `dl`, `dt`, `dd`는 이미 정의 되어 있거나 정해져 있는 경우에만 사용할 수 있음
    - 메뉴나 form에 사용 불가

## dd
- `dl`, `dt`과 함께 사용하며, **설명 목록의 용어에 대한 설명, 정의 등**을 제공
- `dl`의 자식, 자손이 아닌 단독으로 사용 불가
- `dl`, `dt`, `dd`는 이미 정의 되어 있거나 정해져 있는 경우에만 사용할 수 있음
    - 메뉴나 form에 사용 불가
