## button과 input[type="submit"]의 차이

### 1. 공통점

- 둘 다 **폼(form)** 안에서 사용될 수 있으며,  
  **폼을 제출(submit)** 하거나, **클릭 이벤트** 를 처리할 수 있음

---

### 2. 차이점

| 구분               | `<button>`                                 | `<input type="submit">`              |
| ------------------ | ------------------------------------------ | ------------------------------------ |
| 태그 형태          | 쌍태그(열고 닫음)                          | 단일 태그(닫힘 태그 없음)            |
| 버튼 내부 컨텐츠   | 텍스트, 아이콘, 이미지 등 다양한 내용 가능 | value 속성에만 텍스트 가능           |
| 기본 역할          | type="submit"이면 폼 제출                  | 기본적으로 폼 제출용                 |
| type 속성          | submit, reset, button 등 지정 가능         | 무조건 submit (type="submit"만 지원) |
| 스타일링/확장성    | 내부에 span, img 등 다양한 커스텀 가능     | 텍스트 외엔 커스텀 어려움            |
| 접근성(스크린리더) | 버튼 역할로 명확하게 인식                  | submit 버튼으로 인식                 |

---

### 3. 사용 예시

```html
<!-- input[type="submit"] -->
<form>
  <input type="submit" value="제출" />
</form>

<!-- button -->
<form>
  <button type="submit">제출</button>
  <button type="button" onclick="alert('클릭!')">클릭</button>
  <button type="reset">초기화</button>
</form>
```
