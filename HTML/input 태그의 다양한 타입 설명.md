## input 태그의 다양한 타입 설명

### 1. input 태그란?

- `<input>`은 사용자로부터 데이터를 입력받을 수 있는 HTML 폼 요소입니다.
- `type` 속성에 따라 다양한 입력 방식(텍스트, 비밀번호, 이메일 등)을 지원합니다.

---

### 2. 주요 input 타입과 설명

| 타입           | 설명                               | 예시 코드                              |
| -------------- | ---------------------------------- | -------------------------------------- |
| text           | 한 줄 텍스트 입력                  | `<input type="text" />`                |
| password       | 비밀번호 입력(문자 숨김)           | `<input type="password" />`            |
| email          | 이메일 주소 입력                   | `<input type="email" />`               |
| number         | 숫자만 입력, 화살표로 증감         | `<input type="number" />`              |
| tel            | 전화번호 입력                      | `<input type="tel" />`                 |
| url            | 웹사이트 주소 입력                 | `<input type="url" />`                 |
| search         | 검색어 입력, clear 버튼 등 UI 지원 | `<input type="search" />`              |
| date           | 날짜 선택(달력 UI)                 | `<input type="date" />`                |
| time           | 시간 선택                          | `<input type="time" />`                |
| datetime-local | 날짜+시간 선택                     | `<input type="datetime-local" />`      |
| month          | 연/월 선택                         | `<input type="month" />`               |
| week           | 연/주 선택                         | `<input type="week" />`                |
| checkbox       | 체크박스(복수 선택)                | `<input type="checkbox" />`            |
| radio          | 라디오버튼(단일 선택)              | `<input type="radio" />`               |
| range          | 슬라이더(범위 값 입력)             | `<input type="range" />`               |
| color          | 색상 선택(컬러피커 UI)             | `<input type="color" />`               |
| file           | 파일 업로드                        | `<input type="file" />`                |
| hidden         | 사용자에게 보이지 않음(값 저장용)  | `<input type="hidden" />`              |
| submit         | 폼 제출 버튼                       | `<input type="submit" />`              |
| reset          | 폼 입력값 초기화                   | `<input type="reset" />`               |
| button         | 일반 버튼(별도 JS 처리 필요)       | `<input type="button" />`              |
| image          | 이미지를 submit 버튼으로 사용      | `<input type="image" src="img.png" />` |

---

### 3. 참고

- 최신 브라우저에서는 다양한 타입을 지원하지만,  
  구형 브라우저에서는 일부 타입이 지원되지 않을 수 있음
- 필요에 따라 **placeholder, required, maxlength, min/max, pattern** 등 속성과 함께 사용하면 유용함

---

### 4. 요약

- `<input>`의 `type` 속성을 변경함으로써  
  다양한 종류의 사용자 입력을 손쉽게 받을 수 있다.
