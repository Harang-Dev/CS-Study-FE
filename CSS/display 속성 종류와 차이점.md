## display 속성 종류와 차이

### 1. 정의

- CSS의 `display` 속성은 **요소가 페이지에서 어떻게 배치되고 보일지** 를 결정하는 핵심 속성입니다.

---

### 2. 주요 display 값과 특징

| 값           | 특징 및 설명                                                                    |
| ------------ | ------------------------------------------------------------------------------- |
| block        | 한 줄 전체를 차지하는 박스(블록 레벨 요소), 줄 바꿈 발생                        |
| inline       | 내용만큼만 차지, 줄 바꿈 없음, width/height/padding/margin-top/bottom 지정 불가 |
| inline-block | inline처럼 한 줄에 나란히, block처럼 width/height/padding/margin 모두 지정 가능 |
| none         | 요소가 화면에 **아예 표시되지 않음** (공간도 차지하지 않음)                     |
| flex         | 플렉스 컨테이너로 지정, 하위 요소를 유연하게 배치                               |
| inline-flex  | flex처럼 배치하되, 컨테이너 자체는 inline처럼 동작                              |
| grid         | 그리드 컨테이너로 지정, 하위 요소를 행/열 기반으로 정렬                         |
| inline-grid  | grid와 같으나, 컨테이너 자체는 inline처럼 동작                                  |
| table        | 요소와 자식이 테이블 레이아웃처럼 동작                                          |
| list-item    | 목록(list) 항목처럼 동작                                                        |

---

### 3. 예시

```html
<div style="display: block;">Block</div>
<span style="display: inline;">Inline</span>
<div style="display: inline-block; width:100px;">Inline-block</div>
<div style="display: none;">보이지 않음</div>
<div style="display: flex;">
  <div>Flex Item 1</div>
  <div>Flex Item 2</div>
</div>
```

---

### 4. 요약

- block : 한 줄 전체 차지, 줄 바꿈 발생
- inline : 내용만큼만 차지, 옆에 다른 요소 배치
- inline-block : 옆에 배치+크기조정 가능
- none : 화면에 표시되지 않음
- flex/grid : 레이아웃 컨테이너(자식 유연하게 배치)
- display는 요소의 배치, 레이아웃, 표시 여부에 핵심적 역할을 한다.
