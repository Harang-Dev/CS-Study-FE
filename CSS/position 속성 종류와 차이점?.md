## position 속성 종류와 차이점

### 1. 정의

- CSS의 `position` 속성은 **요소를 어디에, 어떻게 배치할지** 를 결정하는 속성입니다.
- 주요 값: `static`, `relative`, `absolute`, `fixed`, `sticky`

---

### 2. 각 position 값의 특징과 차이점

| 값       | 의미/특징                                                               | 기준(기준점)                                       |
| -------- | ----------------------------------------------------------------------- | -------------------------------------------------- |
| static   | 기본값. 일반적인 흐름(문서 순서)에 따라 배치                            | 없음                                               |
| relative | static과 비슷하나, top/right/bottom/left로 **자기 위치 기준 이동** 가능 | 자기 자신(원래 위치)                               |
| absolute | **가장 가까운 position이 지정된 조상** 기준으로 위치를 절대 지정        | position:relative/absolute/fixed 조상, 없으면 body |
| fixed    | **브라우저(뷰포트) 기준** 으로 고정. 스크롤해도 위치 변하지 않음        | 브라우저(뷰포트)                                   |
| sticky   | 스크롤 위치에 따라 static/ fixed처럼 동작(임계점 지나면 고정)           | 가장 가까운 스크롤 조상                            |

---

### 3. 예시

```css
/* static (기본값) */
.box1 {
  position: static;
}

/* relative */
.box2 {
  position: relative;
  top: 10px; /* 원래 위치에서 아래로 10px 이동 */
  left: 20px; /* 원래 위치에서 오른쪽으로 20px 이동 */
}

/* absolute */
.box3 {
  position: absolute;
  top: 0;
  right: 0;
  /* 조상 중 position: relative 등으로 지정된 요소를 기준으로 위치 */
}

/* fixed */
.box4 {
  position: fixed;
  bottom: 10px;
  right: 10px;
  /* 항상 화면(브라우저) 우하단에 고정 */
}

/* sticky */
.box5 {
  position: sticky;
  top: 0;
  /* 부모의 영역을 스크롤할 때만 고정 */
}
```

---

### 4. 요약

- **static** : 기본 배치 (포지션 지정 안함)
- **relative** : 자기 위치 기준으로 이동 (공간 차지 O)
- **absolute** : 기준이 되는 조상(없으면 body) 기준, 레이어처럼 떠 있음 (공간 차지 X)
- **fixed** : 브라우저 화면에 고정, 스크롤에도 위치 변하지 않음
- **sticky** : 스크롤 위치에 따라 static/fixed처럼 동작
