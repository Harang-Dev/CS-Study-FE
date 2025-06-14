## meta 태그의 종류와 역할

### 1. meta 태그란?

- `<meta>` 태그는 **HTML 문서의 정보(메타데이터)**를 담는 태그로,
  웹페이지 자체에는 직접 표시되지 않지만,  
  **브라우저, 검색엔진, 소셜미디어, 기타 서비스**에서 페이지를 이해하는 데 중요한 역할을 합니다.
- 보통 `<head>` 태그 내부에 위치합니다.

---

### 2. 주요 meta 태그 종류와 역할

| 종류           | 예시 코드                                                       | 역할/설명                                                    |
|----------------|-----------------------------------------------------------------|--------------------------------------------------------------|
| charset        | `<meta charset="UTF-8">`                                        | 문자 인코딩(한글 등 여러 언어 지원)                          |
| viewport       | `<meta name="viewport" content="width=device-width, initial-scale=1.0">` | 반응형 웹을 위한 화면 크기/배율 설정                         |
| description    | `<meta name="description" content="페이지 설명">`                | 검색엔진/소셜미디어에 표시되는 페이지 요약                   |
| keywords       | `<meta name="keywords" content="키워드1, 키워드2">`              | (예전 SEO용) 페이지 관련 키워드(요즘은 영향 거의 없음)        |
| author         | `<meta name="author" content="작성자명">`                        | 문서 작성자 정보                                              |
| robots         | `<meta name="robots" content="index, follow">`                   | 검색엔진의 페이지 수집/색인 정책                              |
| http-equiv     | `<meta http-equiv="refresh" content="5; url=https://example.com">`| 5초 후 해당 URL로 자동 이동(리다이렉트), 기타 HTTP 헤더 설정   |
| og(Open Graph) | `<meta property="og:title" content="페이지 제목">`               | 소셜미디어(페북, 카톡 등) 공유 시 제목/이미지/설명 표시       |
| twitter card   | `<meta name="twitter:card" content="summary_large_image">`       | 트위터 공유용 카드 스타일                                     |

---

### 3. 예시 코드

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="프론트엔드 CS 기술면접 정리 레포지토리">
  <meta name="author" content="홍길동">
  <meta property="og:title" content="Frontend Interview Notes" />
  <meta property="og:description" content="프론트엔드 면접 대비 Q&A 마크다운 모음" />
  <meta property="og:image" content="https://example.com/banner.png" />
</head>
```

---

### 4. 요약
- **meta 태그** 는 문서 정보를 제공해 **검색엔진 최적화** , **소셜미디어 미리보기** , **브라우저 동작** 등 다양한 곳에서 활용 된다.
- 기본적으로 `<head>` 내부에 작성하며, 주요한 정보(인코딩, 뷰포트, 설명, 오픈그래프, 트위터카드 등)을 꼭 포함시키는 것이 좋다.