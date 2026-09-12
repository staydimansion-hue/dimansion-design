# dimansion-design

STAY DIMANSION crew 앱(`dimension-crew`)의 디자인 시스템 레퍼런스입니다. 실제 앱 코드(`src/app/globals.css`, 각 화면 컴포넌트)에서 쓰이는 색상·타이포·아이콘·컴포넌트·화면 패턴 값을 그대로 정리했습니다.

## 보기

라이브 캔버스(클릭해서 색상/텍스트 바로 수정 가능): https://claude.ai/code/artifact/463e92e3-4a90-43a1-8ce6-ee3ea6f4697d

- **Foundations** — 색상 12개, 타이포(Bricolage Grotesque + Pretendard), 아이콘 3종 + 앱 아이콘, 모서리 반경
- **Components** — 버튼, 입력창, 상태 배지, 카드
- **Patterns** — 직원 하단 탭, 관리자 상단 내비, 표, 캘린더 날짜칸

## 파일 구조

```
design-system/
  Main.dc.html        # Foundations (색상·타이포·아이콘)
  Components.dc.html  # 버튼·입력·배지·카드
  Patterns.dc.html     # 내비·표·캘린더
  canvas.json          # 캔버스 배치 정보
```

각 `.dc.html`은 [Claude Design Components](https://claude.ai/design) 형식의 아트보드 소스입니다.

## Stay Dimansion House Rules

숙소 안내문(하우스룰) 캔버스. 라이브: https://claude.ai/code/artifact/fc099819-7cf7-482a-ae02-02a5b758190c

- **영문 워드마크(STAY DIMANSION)**: Cormorant Garamond (Google Fonts)
- **국문 헤드라인**: Maru Buri(마루 부리, 네이버) — `house-rules/Main.dc.html`에 `@font-face`로 폰트 파일 자체가 base64로 내장되어 있음(구글 폰트에 없는 폰트라서)
- 본문/안내 텍스트는 기존대로 Noto Sans KR 유지

```
house-rules/
  Main.dc.html   # 하우스룰 1페이지 (1123x794, 인쇄용 fixed)
  canvas.json
```

## Stay Dimansion Welcome Card

객실용 웰컴카드 캔버스. 라이브: https://claude.ai/code/artifact/d7666607-801c-4813-a45c-63af6747aae9

```
welcome-card/
  Main.dc.html   # 480x680 카드, 손님이름/객실번호/와이파이/체크아웃 시간 편집 가능
```

## Typography

서체 전체 목록(확정된 것 + 필요할 때 쓸 후보들)은 [typography.md](./typography.md) 참고.

## 디자인 규칙

브랜드 표기 규칙(이탤릭 금지, 강조는 제목에만, 자간, 줄바꿈 등)과 정렬·여백 규칙은 [CLAUDE.md](./CLAUDE.md) 참고. 브랜드에 국한되지 않는 일반 원칙은 [.claude/skills/editorial-design/SKILL.md](./.claude/skills/editorial-design/SKILL.md)에 따로 정리했습니다.

## 앱 코드와 동기화

`dimension-crew` 앱의 디자인 토큰이 바뀌면(`src/app/globals.css`) 이 저장소도 같이 갱신해주세요. 실제 값이 바뀌었는데 여기가 예전 값으로 남아있으면 레퍼런스로서 의미가 없습니다.
