## CSS-in-JS란? (Styled Components, Emotion 등)

### 1. 정의

- **CSS-in-JS** 는 **JavaScript 파일 안에서 CSS를 작성**하 고,  
  컴포넌트 단위로 스타일을 적용할 수 있는 방식입니다.
- 대표적인 라이브러리로는 **Styled Components**, **Emotion**, **Stitches**, **JSS** 등이 있습니다.

---

### 2. 왜 사용하는가?

| 기존 방식(CSS) 문제점                   | CSS-in-JS의 장점                           |
| --------------------------------------- | ------------------------------------------ |
| 전역 스타일 충돌                        | **컴포넌트 단위 스타일링 (Scoped CSS)**    |
| 클래스 이름 관리 불편                   | 자동으로 고유 클래스 생성 (`scoped hash`)  |
| JS 변수, 상태에 따라 스타일 변경 어려움 | **props 기반 동적 스타일링** 가능          |
| 별도 CSS 파일 관리 필요                 | **JS 파일 내에서 스타일과 로직 통합 관리** |

---

### 3. 사용 예시

#### Styled Components

```jsx
import styled from "styled-components";

const Button = styled.button`
  background: ${(props) => (props.primary ? "blue" : "gray")};
  color: white;
  padding: 10px;
`;

export default function App() {
  return <Button primary>Primary Button</Button>;
}
```

**Emotion**

```jsx
import { css } from "@emotion/react";

const buttonStyle = css`
  background: red;
  color: white;
`;

export default function App() {
  return <button css={buttonStyle}>Emotion Button</button>;
}
```

---

### 4. 장단점 요약

**장점**

- 컴포넌트 기반 구조에 자연스럽게 어울림 (React 등)
- 동적 스타일(조건부, props 기반 등)이 쉬움
- 클래스 충돌 방지, 유지보수에 강함

**단점**

- 런타임 성능 이슈 가능성 (스타일 계산)
- 스타일 분리가 안 되어 JS와 CSS가 혼재됨
- 빌드 사이즈 증가 우려

---

### 5. 요약

- CSS-in-JS는 JS 안에서 스타일을 선언하고 적용하는 방식으로, 컴포넌트 기반 개발과 잘 어울리며, 동적 스타일링, 클래스 충돌 방지, 유지보수성 면에서 큰 장점이 있습니다.
