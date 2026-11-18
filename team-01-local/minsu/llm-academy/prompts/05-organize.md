# 05 · 모은 것을 archive/로 한꺼번에 정리하기 (5일차 4교시)

먼저 **Shift + Tab**을 눌러 화면 아래에 `⏸ plan mode on`이 보이게 합니다. 노란 칸 둘(우리 팀 4일차 태그 파일 이름 · 팀 태그 두세 개)만 바꿔 붙여 넣습니다. 1 · 2번 줄은 그대로 써도 됩니다.

```text
[1. 나의 정리 목적] 6개월 뒤 팀원이 파일 이름과 표 한 줄만 보고 자료를 찾고, 원문을 다시 열 수 있게
[2. 최우선 판단 기준] 원본은 그대로 둔다. 모르는 칸은 짐작하지 않고 비운다
[3. 태그로 쓸 말] 4일차 태그: [우리 팀 4일차 태그 파일 이름] 첫 줄의 태그 + 오늘 팀 태그 [팀 태그 두세 개]

위 세 칸을 기준으로 내 이름 폴더의 raw/ 안 파일을 모두 읽고 정리해 줘.
1. raw/의 파일을 archive/files/에 새 이름으로 복사해. raw/의 원본은 지우거나 고치지 마.
   이름: 모은날짜_소스_장소_내용_v01.확장자 (예: 2026-11-16_googlemap_nocheon-foot-spa_review-en_v01.md)
   영어 소문자·숫자·하이픈(-)만, 칸은 밑줄(_)로. 'final'은 쓰지 마.
2. archive/metadata.csv를 UTF-8 BOM으로 만들어. 한 파일 = 한 줄. 칸 14개:
   item_id,file,media,place,tags,source,url,created,collected,collector,plan_row,summary,rights,public_ok
   - item_id: 내 이름 폴더 이름-001처럼 / media: text · video · image 중 하나
   - source·url·created·collected: 파일 맨 위 출처 한 줄에 있는 것만 옮겨. 없으면 비워
   - plan_row: 맨 위 fieldwork-plan.md의 몇 번째 줄 자료인지
3. summary는 한 줄. 사진은 직접 보고 무엇이 보이는지와 보이는 글자, 자막은 요약 노트에서, 글은 몇 건이 무엇에 대한 것인지.
4. tags는 [3]의 말에서만 골라 ; 로 이어.
5. rights는 출처 한 줄에 적힌 권리 표시(공공누리 유형 등)만 그대로 옮기고, 없으면 비워. public_ok는 비워. 사람이 채운다.
6. 끝나면 복사한 파일 수와 metadata.csv 줄 수가 같은지, 옮기지 않은 파일은 무엇인지 알려 줘.
```

계획에서 볼 것 셋: 바꿀 이름 표 · 옮기지 않을 파일 · Claude가 되묻는 질문. 고칠 것이 있으면 **No, keep planning**을 고르고 한 줄로 말합니다. 맞으면 **Yes**.

이렇게 되면 성공: `archive/files/`와 `archive/metadata.csv`가 생기고, 마지막 보고에 "복사한 파일 수 = metadata.csv 줄 수", `raw/`는 그대로입니다.

## 막히면

- 계획이 길어 끝이 안 보이면: "갈래별로 나눠서 text부터 해 줘"
- 사진이 많아 사용 한도에 걸리면: "사진은 10장씩 나눠서 해 줘"
