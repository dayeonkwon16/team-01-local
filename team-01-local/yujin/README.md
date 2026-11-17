# 2일차 시작 폴더 (L.L.M Academy · Local ①)

이 폴더를 통째로 복사해서 **내 학습 폴더**로 씁니다. 6주 동안 리서치 결과는 채팅창이 아니라 이 폴더의 파일로 쌓습니다.

## 들어 있는 것

| 파일·폴더 | 하는 일 | 오늘 할 일 |
|---|---|---|
| `CLAUDE.template.md` | 내 CLAUDE.md의 틀. Claude Code가 이 폴더에서 일할 때마다 먼저 읽는 '나 소개서' | 복사해서 이름을 `CLAUDE.md`로 바꾸고 네 칸을 채웁니다 |
| `keyword-map.md` | 부산 지역 키워드 맵 틀 | 내 트랙 칸에 키워드 12개 이상 |
| `research/` | 주제별 리서치 노트를 모으는 폴더 | 노트 2개 이상(출처 URL·확인일 포함) |
| `research/_note-template.md` | 리서치 노트 한 장의 틀 | 복사해서 `2026-11-12-주제.md`로 저장 |
| `SOURCE.md` | `inputs/` 표들의 공식 출처·기준 시점·컬럼 뜻·전처리 기준, 지역 사진(TourAPI) 받는 법 | 표를 열기 전에 먼저 읽습니다 |
| `inputs/` | 공공데이터에서 부산 행만 뽑은 실데이터 CSV 9개(축제·전통시장·상가·데이터랩) | 실습 1단계에서 Claude Code와 함께 읽습니다 |
| `prompts/` | 세 칸([1. 나의 기획 목적] · [2. 최우선 판단 기준(우선순위)] · [3. 타깃 대상 및 제외할 노이즈])을 채우는 조립형 프롬프트 | 실습 2단계에서 내 말로 칸을 채웁니다 |
| `examples/` | 칸을 비우고 물었을 때(Before)와 목표 수준(After) 비교, CLAUDE.md 완성 예시 | 실습 3단계에서 내 결과와 대조합니다 |

## 오늘 실습의 세 단계

1. **[Input 함께 읽기 & 한계 점검 소통]** `inputs/`의 표를 Claude Code에 읽히고, 무엇이 없고 무엇이 중복인지 짝·강사와 이야기합니다.
2. **[내 목적·우선순위 주입해 Input 가다듬기]** `prompts/`의 세 칸을 내 말로 채워 필요한 행만 남깁니다.
3. **[산출물 생성 & 골든 샘플 대조 개선]** `keyword-map.md`와 `research/2026-11-12-주제.md`를 만들고 `examples/`의 After와 비교해 고칩니다.

## 시작 순서

1. VS Code에서 내 학습 폴더 `LLM-team-project`(Windows `C:\Users\내이름\LLM-team-project`, macOS `~/LLM-team-project`)를 엽니다. 폴더 만드는 명령은 2일차 1교시 교안에 있습니다.
2. 파일은 교안 슬라이드의 ⬇ 단추로 그때그때 받아, 단추에 적힌 폴더(`LLM-team-project/`, `inputs/`, `prompts/`, `examples/`, `research/`)에 끌어다 놓습니다. 놓친 파일은 2일차 자료실에서 다시 받습니다.
3. Claude Code는 항상 `LLM-team-project` 폴더에서 켭니다(VS Code 터미널에서 `claude`, 데스크톱 앱 **Code** 탭이면 **Open folder** → `LLM-team-project`).
4. `CLAUDE.template.md`로 내 `CLAUDE.md`의 네 칸을 채우고, `keyword-map.md`를 채운 뒤, 키워드마다 `research/` 안에 노트를 만듭니다.

## 지킬 것

- 비밀번호, 전화번호, 접속 코드는 어떤 파일에도 적지 않습니다.
- 출처 URL을 직접 열어 보지 않은 내용은 노트에 `[확인 필요: 무엇]`으로 남깁니다.
- 노트 이름은 `날짜-주제.md`, 영어 소문자와 하이픈만 씁니다. 예: `research/2026-11-12-yeongdo-halmae.md`
