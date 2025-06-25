## z-index가 동작하지 않을 때

### 1. 정의

- `z-index`는 요소의 쌓임 순서(레이어 순서)를 결정하는 CSS 속성입니다.
- 보통 겹쳐진 요소 중 어떤 게 위/아래에 보일지 제어할 때 사용합니다.

---

### 2. 동작하지 않는 대표적 원인

1. **position 속성이 없는 경우**

   - `z-index`는 `position: static`(기본값)에는 적용되지 않습니다.
   - 반드시 `position: relative`, `absolute`, `fixed`, `sticky` 중 하나와 함께 써야 합니다.

2. **쌓임 맥락(Stacking Context) 문제**

   - 부모 요소가 새로운 쌓임 맥락을 만들었을 때,  
     자식의 `z-index`가 다른 부모의 자식과 비교해 동작하지 않을 수 있습니다.
   - opacity, transform, filter, will-change, flex/grid 등도 새로운 stacking context를 만듦.

3. **z-index 값이 같거나 기본값(자동)일 때**
   - 명시적으로 z-index를 지정하지 않으면, HTML 소스 순서대로 쌓임.

---

### 3. 예시

```css
/* position이 없으면 z-index 적용 안 됨 */
.box1 {
  z-index: 10; /* X (동작하지 않음) */
}

/* position과 함께 써야 적용됨 */
.box2 {
  position: relative;
  z-index: 10; /* O (동작함) */
}
```

---

### 4. 체크해야할 부분

- 해당 요소(및 부모)가 position 속성을 가지고 있는지?
- 쌓임 맥락이 의도와 다르게 생성되어 있지 않은지?
- z-index 값이 의도대로 지정되어 있는지?

---

### 5. 요약

- z-index는 반드시 position 속성과 함께 써야 하며
- 쌓임 맥락(stacking context) 구조에 따라 예상과 다르게 동작할 수 있다.
- 여러 요소가 겹치는 경우, 쌓임 맥락을 명확히 이해하고 코드를 작성해야 한다.
