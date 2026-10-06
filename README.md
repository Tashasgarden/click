# 행복대화 · 나의 복주머니 뽑기

한국SGI 좌담회 '행복대화'에서 쓰는 복주머니 뽑기 웹페이지입니다.
복주머니를 누르면 어서(또는 이케다 선생님 스피치)와 해설, 나눔 질문이 팝업으로 나옵니다.

- 주제: 공양 · 청년육성 · 체험담 · 이달의 법련 · 화합
- 🎁 랜덤으로 뽑기 / 주제별 보기 / 열어본 주머니 표시(↺ 처음부터로 초기화)
- 빌드 없는 단일 파일 `index.html` (HTML / CSS / JavaScript)

## 복주머니 추가·수정

`index.html` 아래쪽 `<script>`의 `POUCHES` 배열에 항목을 추가하면 됩니다.

```js
{ topic:"체험담", type:"어서",          // type: "어서" 또는 "스피치"
  quote:"어서 또는 스피치 본문",
  source:"어서명 · 어서 ○○쪽",          // 스피치는 저서·권·장 등
  text:"해설",
  q:"나눔 질문" },
```

새 주제를 만들려면 `TOPICS` 배열에도 이름을 추가하세요.
어서 쪽수는 『니치렌대성인 어서전집』 한국어판 기준이며, 번역 문구는 좌담회 전에 어서·『법련』 원문과 대조해 주세요.

## 배포

**Netlify (가장 간단)** – https://app.netlify.com/drop 에 이 폴더를 끌어다 놓거나,
Netlify에서 이 저장소를 연결하면 됩니다(`netlify.toml` 포함, 빌드 명령 없음).

**GitHub Pages** – `main` 브랜치에 병합한 뒤 저장소 Settings → Pages → Source를
"GitHub Actions"로 선택하면 `.github/workflows/pages.yml`이 자동 배포합니다.

**Vercel** – 저장소를 Import 하고 Framework Preset을 "Other"로 두면 그대로 배포됩니다.
