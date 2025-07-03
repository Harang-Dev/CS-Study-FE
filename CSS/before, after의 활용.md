## ::before, ::after의 활용

### 1. 정의

- `::before`와 `::after`는 **CSS 가상 요소(Pseudo-elements)** 입니다.
- 실제 HTML에 없는 **가상의 콘텐츠를 요소 앞/뒤에 추가** 할 수 있게 해줍니다.
- 주로 **장식, 아이콘, 레이아웃 효과, 애니메이션 등** 에 활용됩니다.

---

### 2. 문법

```css
.selector::before {
  content: "앞에 추가될 텍스트 또는 요소";
}

.selector::after {
  content: "뒤에 추가될 텍스트 또는 요소";
}
```

- content 속성은 필수입니다 (없으면 아무것도 표시되지 않음)
- 일반적으로 display: block 또는 inline-block으로 스타일을 조정합니다.

---

### 3. 활용 예시

(1) 시각적 장식 요소

```css
.title::before {
  content: "★ ";
  color: gold;
}
```

(2) 작은 구분선

```css
.divider::after {
  content: "";
  display: block;
  height: 1px;
  background: #ccc;
  margin-top: 10px;
}
```

(3) 말풍선 꼬리 만들기

```css
.tooltip::after {
  content: "";
  position: absolute;
  border: 10px solid transparent;
  border-top-color: black;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
}
```

---

### 4. 주의사항

::before, ::after는 **인라인 요소(span 등)** 에서는
display를 inline-block 또는 block으로 바꿔야 보이기도 함

content에 이미지를 넣으려면 url() 사용 가능

```css
.icon::before {
  content: url("/icons/check.svg");
}
```

---

### 5. 요약

::before와 ::after는 가상 요소로,
HTML을 수정하지 않고 시각적 콘텐츠를 앞/뒤에 추가할 수 있습니다.

레이아웃, 장식, 애니메이션, 아이콘 등에 폭넓게 활용됩니다.
