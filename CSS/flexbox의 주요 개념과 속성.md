## flexbox의 주요 개념과 속성

### 1. flexbox란?

- **flexbox(Flexible Box Layout)** 는  
  CSS에서 요소들을 **유연하게 정렬, 배치, 분배** 할 수 있는 1차원(행 또는 열) 레이아웃 시스템입니다.
- 복잡한 레이아웃도 적은 코드로 쉽게 구현할 수 있습니다.

---

### 2. 기본 개념

- **컨테이너(Container)** : `display: flex;`를 지정한 부모 요소
- **아이템(Item)**: 컨테이너의 자식 요소들

---

### 3. 주요 속성

#### (1) 컨테이너에 적용하는 속성

| 속성            | 설명                                       | 예시 값                                                                 |
| --------------- | ------------------------------------------ | ----------------------------------------------------------------------- |
| display         | flex 컨테이너 선언                         | flex, inline-flex                                                       |
| flex-direction  | 주축 방향(행/열) 설정                      | row, column, row-reverse, column-reverse                                |
| flex-wrap       | 아이템 줄바꿈 여부                         | nowrap, wrap, wrap-reverse                                              |
| justify-content | 주축 방향(가로/세로) 정렬                  | flex-start, center, flex-end, space-between, space-around, space-evenly |
| align-items     | 교차축(반대축) 정렬                        | stretch, flex-start, center, flex-end, baseline                         |
| align-content   | 여러 줄일 때 교차축 정렬(여러 줄에만 적용) | stretch, center, flex-start, flex-end, space-between, space-around      |

#### (2) 아이템(자식)에 적용하는 속성

| 속성        | 설명                          | 예시 값                     |
| ----------- | ----------------------------- | --------------------------- |
| flex-grow   | 남은 공간을 얼마나 키울지     | 0(기본), 1, 2…              |
| flex-shrink | 공간 부족 시 줄어드는 비율    | 1(기본), 0, 2…              |
| flex-basis  | 기본 크기(길이, %)            | auto, 100px 등              |
| flex        | grow, shrink, basis 단축 속성 | 1, 0 30px 등                |
| align-self  | 개별 아이템의 교차축 정렬     | auto, flex-start, center 등 |

---

### 4. 예시 코드

```css
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.item {
  flex: 1;
}
```

```html
<div class="container">
  <div class="item">A</div>
  <div class="item">B</div>
  <div class="item">C</div>
</div>
```

---

### 5. 요약

- flexbox는 1차원(행/열) 레이아웃에 강력함
- 컨테이너와 아이템 각각에 다양한 속성 적용 가능
- 주로 정렬, 간격 분배, 반응형 레이아웃 구현에 자주 사용됨
