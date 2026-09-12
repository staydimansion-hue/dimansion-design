# Typography

STAY DIMANSION 브랜드 소재(하우스룰, 안내문, 홍보물 등)에 쓸 서체 모음입니다. 필요할 때 아래 링크 태그와 `font-family`를 그대로 복사해서 쓰면 됩니다.

## Serif (헤드라인/워드마크) — 확정

House Rules에 적용된 조합입니다.

| 용도 | 서체 | 방식 |
|---|---|---|
| 영문 워드마크 (STAY DIMANSION) | **Cormorant Garamond** | Google Fonts |
| 국문 헤드라인 | **Maru Buri (마루 부리)** | 폰트 파일 직접 내장(구글 폰트에 없음) |

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@600;700&display=swap">
```

```css
.serif-en { font-family: "Cormorant Garamond", "Georgia", serif; }
.serif-kr { font-family: "Maru Buri", "Noto Serif KR", "Georgia", serif; } /* 폰트 파일은 house-rules/Main.dc.html 안에 base64로 내장되어 있음 */
```

## Sans-serif (본문) — 후보

지금 하우스룰/앱 본문은 Pretendard를 쓰고 있습니다. 다른 톤이 필요할 때 쓸 수 있게 3개를 정리해뒀습니다.

### 1. SUIT — 요즘 제일 핫한 픽

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/sun-typeface/SUIT@2/fonts/variable/woff2/SUIT-Variable.css">
```
```css
font-family: "SUIT Variable", "SUIT", sans-serif;
```
Pretendard와 결이 비슷하면서 조금 더 또렷하고 개성 있는 인상. 요즘 "헤더는 SUIT, 본문은 Pretendard" 조합이 트렌드.

### 2. Spoqa Han Sans Neo — 오래 검증된 스탠다드

```html
<link rel="stylesheet" href="https://spoqa.github.io/spoqa-han-sans/css/SpoqaHanSansNeo.css">
```
```css
font-family: "Spoqa Han Sans Neo", sans-serif;
```
Pretendard가 이 계열을 다듬어 만들어진 만큼 톤이 거의 같으면서, 더 오래 검증된 안정적인 선택.

### 3. Wanted Sans — 숫자·기호 디테일이 좋은 대안

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/wanteddev/wanted-sans@v1.0.1/packages/wanted-sans/fonts/webfonts/variable/split/WantedSansVariable.min.css">
```
```css
font-family: "Wanted Sans Variable", "Wanted Sans", sans-serif;
```
Noto Sans 기반 정제 폰트로 Pretendard/SUIT과 섞어 써도 이질감 없음. 숫자·특수문자 디테일이 좋아 표·가격 안내 같은 UI 본문에 적합.

## 참고 — 후보에서 제외한 것들

- Nanum Myeongjo, Gowun Batang, Hahmlet: 검토했으나 톤이 안 맞아 제외
- ZEN SERIF(젠 세리프): 2025년 한글날 공개된 화제작이지만 라이선스상 폰트 파일 재배포·수정이 금지되어 있어 여기 내장하지 않음. 쓰고 싶으면 [Odd Atelier 공식 배포처](https://noonnu.cc/en/font_page/1686)에서 직접 받아 각자 서버에 올려야 함
