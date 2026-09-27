# hyeseong-ppt

발표 자료를 **질문으로 시작해서 설득 구조로 끝내는** AI 에이전트 스킬입니다.
결과물은 외부 요청이 없는 **자립형 단일 HTML 파일** 하나입니다.

[maro-ppt](https://github.com/RDDcat/maro-ppt)(MIT, 육마로)를 바탕으로 아래를 바꿨습니다.

- **기본 스타일 `airbnb`(소프트 덱)** — 흰 캔버스 · 14px 둥근 카드 · Rausch 핑크 한 점. 스타일을 묻지 않고 airbnb 로 만듭니다.
- **모바일 지원** — 좌우로 밀어 장 넘기기, 긴 장은 슬라이드 안에서 세로 스크롤.
- 원본의 `minimal`(최소 덱) 스타일도 그대로 들어 있습니다. "minimal 스타일로"라고 하면 그걸로 만듭니다.

## 설치

```bash
# 전역 설치 (모든 프로젝트에서 사용)
npx skills add songbly-dev/hyeseong-ppt -g

# 지금 프로젝트에만
npx skills add songbly-dev/hyeseong-ppt
```

Claude Code 플러그인으로 설치해도 됩니다.

```
/plugin marketplace add songbly-dev/hyeseong-ppt
/plugin install hyeseong-ppt@hyeseong-ppt
```

비공개 저장소라면 GitHub 에 로그인된 환경(`gh auth login`)에서 설치하세요.

## 쓰는 법

```
발표 자료 만들어줘
{자료 경로} 이 자료로 PPT 만들어줘
/hyeseong-ppt
```

핵심 메시지 → 후킹 제목 → 슬라이드 구성 → 나머지(청중·저장 위치) 순서로 하나씩 묻고, 덱을 만든 뒤 장별 요약표를 보여 줍니다.
고칠 장 번호만 말하면 그 장만 고칩니다.

## 만든 덱에서 할 수 있는 것

| 기능 | 조작 |
|---|---|
| 장 넘기기 | `←` `→` · 모바일은 좌우로 밀기 |
| 글자 고치고 파일에 덮어쓰기 | `E` 로 편집 켜고 `⌘S` 로 저장 |
| 강의 중 화면 배율 | `]` 확대 · `[` 축소 · `\` 원래대로 |

## 구성

```
skills/hyeseong-ppt/
├── SKILL.md                 인터뷰 → 확장 → 생성 → 수정 규칙
├── styles/
│   ├── airbnb/  (기본)       style.md · template.html · design-spec.md · design-spec.html
│   └── minimal/             style.md · template.html · design-spec.md · design-spec.html
└── utils/kakao-chat/        카카오톡 채팅 화면 재현 유틸
```

스타일 규격은 `styles/airbnb/design-spec.html` 을 브라우저로 열면 볼 수 있습니다.

## 크레딧

- 원작: [RDDcat/maro-ppt](https://github.com/RDDcat/maro-ppt) — MIT, © 2026 육마로
- airbnb 스타일의 토큰 원본: `npx getdesign@latest add airbnb` 가 만든 DESIGN.md ("inspired by airbnb")

MIT. [`LICENSE`](LICENSE)
