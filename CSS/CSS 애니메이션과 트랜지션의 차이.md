## CSS 모듈이란?

### 1. 정의

- **CSS Modules(모듈)** 은  
  각 CSS 파일을 **해당 컴포넌트에만 적용되도록 스코프(scope)를 제한** 하는 방식입니다.
- **클래스 이름 충돌 없이 컴포넌트 단위로 스타일을 적용** 할 수 있도록 해줍니다.
- React, Vue, Svelte 등 다양한 프레임워크에서 사용됩니다.

---

### 2. 특징

| 특징                      | 설명                                             |
| ------------------------- | ------------------------------------------------ |
| 로컬 스코프               | 클래스명이 자동으로 고유하게 변환되어 충돌 방지  |
| 컴포넌트 단위 스타일링    | 하나의 컴포넌트에만 적용되는 스타일 분리 가능    |
| 자동 네이밍               | 예: `title` → `title__3abx9` (빌드 시 자동 변환) |
| 일반 CSS 문법 그대로 사용 | SCSS처럼 별도 문법 없이 CSS를 그대로 사용 가능   |

---

### 3. 사용 방법 (React 기준)

#### 파일 구조

- Button.js
- Button.module.css

```css
.button {
  background-color: green;
  color: white;
  padding: 10px;
}
```

```jsx
import styles from "./Button.module.css";

export default function Button() {
  return <button className={styles.button}>클릭!</button>;
}
```

---

### 4. 장점

- 클래스 충돌 방지 (대규모 프로젝트에서 안정적)
- 전통적인 CSS 문법 그대로 사용 가능
- 컴포넌트 기반 UI에 잘 어울림

---

5. 단점

- 전역 스타일 정의가 번거로울 수 있음
- 동적 스타일링에는 한계가 있음 (조건부 class 조합 필요)
- CSS-in-JS만큼 강력한 기능(조건, 중첩 등)은 부족

---

6. 요약

- CSS 모듈은 CSS를 컴포넌트 단위로 관리하고, 클래스 충돌 없이 스타일을 적용하는 방법입니다.
- React 등 컴포넌트 기반 프로젝트에서 널리 사용되며, 유지보수성과 안정성이 뛰어납니다.
