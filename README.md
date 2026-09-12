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

## 앱 코드와 동기화

`dimension-crew` 앱의 디자인 토큰이 바뀌면(`src/app/globals.css`) 이 저장소도 같이 갱신해주세요. 실제 값이 바뀌었는데 여기가 예전 값으로 남아있으면 레퍼런스로서 의미가 없습니다.
