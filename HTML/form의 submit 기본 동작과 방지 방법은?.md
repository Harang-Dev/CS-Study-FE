## form의 submit 기본 동작과 방지 방법

### 1. form의 submit 기본 동작

- `<form>` 태그는 **submit(제출) 이벤트**가 발생하면
1. **입력된 데이터를 action 속성에 지정한 URL로 전송**  
     (method 속성에 따라 GET/POST 등으로 전송)
2. **페이지가 새로고침(리로드)** 되거나,  
     **다른 페이지로 이동**하게 됩니다.

- 예시:
  ```html
  <form action="/submit" method="POST">
    <input type="text" name="username" />
    <button type="submit">제출</button>
  </form>
  ```

---

### 2. 기본 동장(새로고침/이동) 방지 방법

1. **JavaScript** 의 `preventDefault()` 사용
  - `submit` 이벤트에서 **e.preventDefault()** 를 호출하면 **폼의 기본 동작(페이지 이동/새로고침)** 을 막을 수 있습니다.
  - 예시
  ```jsx
  function handleSubmit(e) {
    e.preventDefault();
  }

return (
  <form onSubmit={handleSubmit}>
    <input type="text" />
    <button type="submit">제출</button>
  </form>
);
```
---

3. **요약**
- `<fomr>` 의 기본 동작 : 입력값 전송 + 페이지 이동/새로고침
- JS의 `e.preventDefault()` 로 이 **기본 동작을 막고** 원하는 방식으로 처리할 수 있다.