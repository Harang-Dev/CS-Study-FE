## BEM 방식이란?

### 1. 정의

- **BEM(Block, Element, Modifier)** 방식은  
  CSS 클래스 이름을 체계적으로 짓기 위한 **네이밍 규칙** 입니다.
- 대규모 프로젝트에서도 **재사용성, 가독성, 유지보수성** 을 높이기 위해 사용됩니다.

---

### 2. 구성

| 구성 요소 | 의미                            | 예시                                    |
| --------- | ------------------------------- | --------------------------------------- |
| Block     | 독립적인 UI 구성 단위(컴포넌트) | `menu`, `button`, `card`                |
| Element   | Block의 구성 요소               | `menu__item`, `card__title`             |
| Modifier  | 속성, 상태, 변형(variation)     | `button--primary`, `menu__item--active` |

---

### 3. 네이밍 규칙

```text
Block:          .block
Element:        .block__element
Modifier:       .block--modifier
Element + Mod:  .block__element--modifier
```

- 예시

```html
<div class="card card--highlighted">
  <h2 class="card__title">제목</h2>
  <p class="card__content">내용</p>
</div>
```

---

### 4. 장점

- 클래스 이름만 보고 구조를 예측할 수 있음
- CSS 충돌 방지
- 컴포넌트 기반 개발과 궁합이 좋음 (React, Vue 등)
- 팀 협업 시 명확한 스타일 가이드 제공

---

### 5. 단점

- 클래스명이 길어질 수 있음
- 간단한 프로젝트에서는 오히려 복잡해 보일 수 있음

---

### 6. 요약

- BEM은 Block\_\_Element--Modifier 형태로 클래스명을 명확히 구분하는 CSS 네이밍 컨벤션
- 일관된 구조로 유지보수에 강하고, 재사용성과 협업에 유리하다.
