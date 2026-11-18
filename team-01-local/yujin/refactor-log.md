# 폴더 정리 기록 (refactor-log)

- 날짜: 2026-11-18
- 파일 내용은 고치지 않고 자리만 옮겼습니다. 지운 파일은 없습니다. 파일 이름도 그대로입니다.
- 파일 개수: 옮기기 전 413개 → 옮긴 뒤 413개 (같음). 이 기록 파일을 만든 뒤 414개입니다.
- 다른 파일 안에 적힌 옛 경로(예: "SOURCE-team.md 12줄", "research/_check.md")는 고치지 않았습니다. 파일 이름이 같으니 이름으로 찾으면 됩니다.

## 옮긴 것

- SOURCE.md → sources/SOURCE.md
- SOURCE-day03.md → sources/SOURCE-day03.md
- SOURCE-team.md → sources/SOURCE-team.md
- data-spec.md → sources/data-spec.md
- CLAUDE.template.md → templates/CLAUDE.template.md
- research/_note-template.md → templates/_note-template.md
- research/_check.md → checklists/_check.md
- research/2026-11-17-서면1번가-상권활성화사업-검증.md → research/archive/2026-11-17-서면1번가-상권활성화사업-검증.md

## 2026-11-18 추가로 옮긴 것

- 맨 위에 새로 들어온 강의 프롬프트 안내서 2개를 `prompts/`로 옮겼습니다(팀원 폴더도 같은 파일을 prompts/에 둠). 내용과 이름은 그대로입니다. 파일 개수 430개 → 430개(같음).
- 10-team-report.md → prompts/10-team-report.md
- 11-team-fieldwork-plan.md → prompts/11-team-fieldwork-plan.md

## 2026-11-18 자막 자리 옮김

- 영상 자막 자리를 `transcripts/`에서 `raw/video/`로 바꿨습니다(조유진 결정). `raw/`는 깃허브에 올라가지 않아 이 파일은 내 PC에만 남습니다. 빈 `transcripts/` 폴더는 지웠습니다.
- transcripts/seomyeon-Ens.txt → raw/video/seomyeon-Ens.txt

## 2026-11-18 안내서 3개와 영상 노트 옮김

- 맨 위에 새로 들어온 5일차 강의 프롬프트 안내서 3개를 `prompts/`로 옮겼습니다. 내용과 이름은 그대로입니다.
- 01-collect-plan.md → prompts/01-collect-plan.md
- 02-collect-text.md → prompts/02-collect-text.md
- 03-video-transcript.md → prompts/03-video-transcript.md
- 영상 요약 노트를 팀과 나누려고 깃허브에 올라가지 않는 `raw/`에서 `report/`로 옮겼습니다(조유진 결정). 닉네임 등 개인 정보는 없습니다. 자막 원본은 `raw/video/`에 그대로 둡니다.
- raw/video/Jeonpo-cafe-note.md → report/Jeonpo-cafe-note.md
