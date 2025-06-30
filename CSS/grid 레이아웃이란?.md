## grid 레이아웃이란?

### 1. 정의

- **Grid Layout(그리드 레이아웃)** 은 CSS에서 2차원(행과 열)을 기준으로 **아이템을 정렬, 배치** 할 수 있는 레이아웃 시스템입니다.
- **Flexbox가 1차원(행 또는 열)** 중심이라면, **Grid는 행(Row) + 열(Column)을 동시에** 제어할 수 있습니다.

---

### 2. 기본 구조

- `display: grid` 또는 `display: inline-grid`로 부모 요소를 **그리드 컨테이너** 로 지정
- 자식 요소는 **그리드 셀(grid cell)** 에 자동 배치되며, 행/열을 명시적으로 정의할 수 있음

---

### 3. 주요 속성

#### (1) 컨테이너에 적용하는 속성

| 속성                  | 설명                    | 예시                          |
| --------------------- | ----------------------- | ----------------------------- |
| display               | 그리드 선언             | `display: grid`               |
| grid-template-columns | 열의 개수 및 너비 설정  | `repeat(3, 1fr)`, `200px 1fr` |
| grid-template-rows    | 행의 개수 및 높이 설정  | `auto 100px`                  |
| gap                   | 셀 사이의 간격 설정     | `gap: 10px;`                  |
| row-gap, column-gap   | 행/열 간격 개별 설정    | `row-gap: 10px`               |
| justify-items         | 셀 내 아이템 가로 정렬  | `start`, `center`, `end`      |
| align-items           | 셀 내 아이템 세로 정렬  | `stretch`, `center` 등        |
| justify-content       | 전체 그리드의 수평 정렬 | `center`, `space-between` 등  |
| align-content         | 전체 그리드의 수직 정렬 | `center`, `space-around` 등   |

#### (2) 아이템(자식)에 적용하는 속성

| 속성         | 설명                            | 예시             |
| ------------ | ------------------------------- | ---------------- |
| grid-column  | 열 위치 또는 병합 (시작 / 종료) | `1 / 3`          |
| grid-row     | 행 위치 또는 병합               | `2 / 4`          |
| grid-area    | 이름 붙인 영역을 지정하여 배치  | `header`, `main` |
| justify-self | 개별 셀 내 가로 정렬            | `center`         |
| align-self   | 개별 셀 내 세로 정렬            | `end`            |

---

### 4. 예시 코드

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: auto;
  gap: 10px;
}
```

```html
<div class="container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
  <div>5</div>
  <div>6</div>
</div>
```

### 5. 요약

- Grid 레이아웃은 2차원(행 + 열) 배치에 적합하며 복잡한 레이아웃 구조도 명확하고 강력하게 구현할 수 있습니다.
- 반응형 웹, 대시보드, 카드형 UI 등에 자주 활용됩니다.
