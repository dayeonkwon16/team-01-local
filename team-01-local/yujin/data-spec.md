# 데이터 명세 · 조유진 · AX 데이터·서비스 트랙

> 정리한 CSV 하나마다 이 표를 하나씩 씁니다. 원본 파일은 고치지 않습니다.
> 작성 2026-11-17. 정리본은 모두 `inputs-team/`에 UTF-8 BOM으로 새로 저장했습니다. 정리는 세 가지만 했습니다: 모든 행이 빈 칸인 열 빼기, 완전히 같은 행은 하나만 남기기, 뺀 것 기록. 값은 원본 글자 그대로 옮겼습니다.
> 제공기관·갱신주기는 SOURCE-day03.md·SOURCE.md를 먼저 봤습니다. 거기에 없는 데이터는 "SOURCE-day03.md·SOURCE.md에 없음"이라고 적고, 확인한 다른 곳(SOURCE-team.md, 공공데이터포털 페이지)을 함께 적었습니다.

## busan_dongsales_time_{동}_20261117.json × 4 → busan_dongsales_time_20261117_clean.csv

| 명세 칸 | 내용 |
|---|---|
| 제공기관 | SOURCE-day03.md·SOURCE.md에 없음 → 부산광역시(빅데이터담당관) (SOURCE-team.md 1번) |
| 갱신주기 | SOURCE-day03.md·SOURCE.md에 없음 → 못 찾음 (이 API 페이지의 갱신주기는 확인 안 함) |
| 기준 시점 | `stdYm` 기준 2023-01 ~ 2026-09 |
| 행 수 | 원본 4320행(동 4개 × 1080) → 정리 후 4320행. 뺀 열 0, 뺀 행 0 |
| 컬럼 뜻 | stdYm: 기준년월 / hcode: 행정동코드 / hname: 행정동명 / times: 시간대(00시~23시) / avgAmt: 월별 일평균 이용금액 / avgCnt: 월별 일평균 이용건수 |
| 단위 | avgAmt: 못 찾음(원인지 적힌 곳 없음) / avgCnt: 못 찾음(설명에 '이용건수'만 있음) |
| 결측·주의 | 빈 칸 없음. 동 4개 JSON을 한 표로 합쳤음(형식만 바꿈). 시간·연령·성별 표끼리 동별 합계가 금액 0~2, 건수 0~4 다름(SOURCE-team.md) |

## busan_dongsales_age_{동}_20261117.json × 4 → busan_dongsales_age_20261117_clean.csv

| 명세 칸 | 내용 |
|---|---|
| 제공기관 | SOURCE-day03.md·SOURCE.md에 없음 → 부산광역시(빅데이터담당관) (SOURCE-team.md 2번) |
| 갱신주기 | SOURCE-day03.md·SOURCE.md에 없음 → 못 찾음 |
| 기준 시점 | `stdYm` 기준 2023-01 ~ 2026-09 |
| 행 수 | 원본 1080행 → 정리 후 1080행. 뺀 열 0, 뺀 행 0 |
| 컬럼 뜻 | stdYm, hcode, hname: 위와 같음 / ages: 연령대(20대미만~60대이상) / avgAmt, avgCnt: 위와 같음 |
| 단위 | avgAmt, avgCnt: 못 찾음 |
| 결측·주의 | 빈 칸 없음. 연령이 카드 소유자 기준인지 적힌 곳 없음 |

## busan_dongsales_gender_{동}_20261117.json × 4 → busan_dongsales_gender_20261117_clean.csv

| 명세 칸 | 내용 |
|---|---|
| 제공기관 | SOURCE-day03.md·SOURCE.md에 없음 → 부산광역시(빅데이터담당관) (SOURCE-team.md 3번) |
| 갱신주기 | SOURCE-day03.md·SOURCE.md에 없음 → 못 찾음 |
| 기준 시점 | `stdYm` 기준 2023-01 ~ 2026-09 |
| 행 수 | 원본 360행 → 정리 후 360행. 뺀 열 0, 뺀 행 0 |
| 컬럼 뜻 | stdYm, hcode, hname: 위와 같음 / gender: 남성·여성 / avgAmt, avgCnt: 위와 같음 |
| 단위 | avgAmt, avgCnt: 못 찾음 |
| 결측·주의 | 빈 칸 없음. 파일데이터 설명(15147846)에 '업종(중)별'이라는 잘못된 문장이 있음(SOURCE-team.md) |

## busan_dongsales_biz_{동}_20261117.json × 4 → busan_dongsales_biz_20261117_clean.csv

| 명세 칸 | 내용 |
|---|---|
| 제공기관 | SOURCE-day03.md·SOURCE.md에 없음 → 부산광역시(빅데이터담당관) (SOURCE-team.md 4번) |
| 갱신주기 | SOURCE-day03.md·SOURCE.md에 없음 → API 페이지 "실시간", 파일데이터 판 "연간" (research/2026-11-17-부산-카드매출-생활인구-데이터.md) |
| 기준 시점 | `stdYm` 기준 2023-01 ~ 2026-09 |
| 행 수 | 원본 1980행 → 정리 후 1980행. 뺀 열 0, 뺀 행 0 |
| 컬럼 뜻 | stdYm, hcode, hname: 위와 같음 / ryLNm: 업종 대분류명(11개) / avgAmt, avgCnt: 위와 같음 |
| 단위 | avgAmt, avgCnt: 못 찾음 |
| 결측·주의 | 빈 칸 없음. `음식료품`이 2026-01부터 `음식료픔`으로 바뀜(값 그대로 둠). 동별 합계가 시간 API와 크게 다름(SOURCE-team.md) |

## busan_dongpop_age_{동}_20261117.json × 4 → busan_dongpop_age_20261117_clean.csv

| 명세 칸 | 내용 |
|---|---|
| 제공기관 | SOURCE-day03.md·SOURCE.md에 없음 → 부산광역시 (SOURCE-team.md 5번) |
| 갱신주기 | SOURCE-day03.md·SOURCE.md에 없음 → API 페이지 "실시간" (research/2026-11-17-부산-카드매출-생활인구-데이터.md) |
| 기준 시점 | `stdYm` 기준 2023-01 ~ 2026-09 |
| 행 수 | 원본 1128행 → 정리 후 1080행. 뺀 열 0, **뺀 행 48**(2026-08·09에 같은 행이 두 번씩 있던 것, 동마다 12행) |
| 컬럼 뜻 | stdYm, hcode, hname: 위와 같음 / ages: 연령대 / hpopAvg·wpopAvg·vpopAvg: 주거·직장·방문 인구 월별 일평균(칸 이름으로 추정) |
| 단위 | 못 찾음 (명인지 적힌 곳 없음) |
| 결측·주의 | 빈 칸 없음. ages 값에 `20대미만`과 `20세미만`이 함께 있음(2026-08부터 바뀜) |

## busan_commercial_change_20261117.json → busan_commercial_change_20261117_clean.csv

| 명세 칸 | 내용 |
|---|---|
| 제공기관 | SOURCE-day03.md·SOURCE.md에 없음 → 부산광역시(빅데이터담당관) (SOURCE-team.md 8번) |
| 갱신주기 | SOURCE-day03.md·SOURCE.md에 없음 → API 페이지 "실시간" (SOURCE-team.md 8번) |
| 기준 시점 | 파일 안에 날짜 칸 없음 → 못 찾음 |
| 행 수 | 원본 477행 → 정리 후 477행. 뺀 열 0, 뺀 행 0 |
| 컬럼 뜻 | type_nm: 상권구분명 / comm_nm: 상권명 / change_indicator_nm: 변화지표값 / average_open_months: 평균생존개월수 / average_close_months: 평균폐업개월수 / busan_average_open_months·busan_average_close_months: 부산 평균 |
| 단위 | 개월 (API 페이지 항목명 '평균생존개월수'에서) |
| 결측·주의 | 빈 칸 없음. 변화지표 네 분류의 정의가 없음. 생존·폐업 0개월인 상권이 있음 |

## busan_commercial_history_20261117/page_0001~0337.json → busan_commercial_history_20261117_clean.csv

| 명세 칸 | 내용 |
|---|---|
| 제공기관 | SOURCE-day03.md·SOURCE.md에 없음 → 부산광역시 (SOURCE-team.md 7번) |
| 갱신주기 | SOURCE-day03.md·SOURCE.md에 없음 → 못 찾음 (상세 페이지를 못 찾음) |
| 기준 시점 | `apvpermymd` 1900-01-01 ~ 2023-06-01, `dcbymd` 1969-11-12 ~ 2023-06-01 |
| 행 수 | 원본 336235행 → 정리 후 336033행. 뺀 열 0, **뺀 행 202**(완전히 같은 행) |
| 컬럼 뜻 | trdstatenm: 영업상태 / bplcnm: 상호 / majornm·minornm: 업종 대·소분류 / upjongnm: 업태 / rdnwhladdr: 도로명주소 / apvpermymd: 인허가일(추정) / dcbymd: 폐업일(추정) / geom: 좌표 |
| 단위 | 날짜 칸은 YYYY-MM-DD. geom 좌표계는 못 찾음 |
| 결측·주의 | 빈 문자열 대신 공백 한 칸(" ")이 들어간 칸이 많아 '빈 열'로 빠진 열은 없음. 공백 칸 수: majornm 23165, minornm 35035, upjongnm 23165, rdnwhladdr 59020, apvpermymd 12706, dcbymd 186769. 행정동 칸 없음. 인허가일 1900-01-01은 실제 날짜가 아닐 수 있음 |

## 부산_서면전포_부전시장_상업용부동산_임대동향_2020-2026.xlsx '원자료' 시트 → busan_seomyeon_rone_rent_vacancy_2020-2026_clean.csv

| 명세 칸 | 내용 |
|---|---|
| 제공기관 | SOURCE-day03.md·SOURCE.md에 없음 → 한국부동산원 R-ONE (xlsx '안내' 시트 B3, SOURCE-team.md 6번) |
| 갱신주기 | SOURCE-day03.md·SOURCE.md에 없음 → 분기 (xlsx '안내' 시트 B7) |
| 기준 시점 | `분기` 칸 기준 2020Q1 ~ 2026Q3 |
| 행 수 | 원본 503행 → 정리 후 503행. 뺀 열 0, 뺀 행 0 |
| 컬럼 뜻 | 지표: 공실률·임대료 / 유형: 상가 유형 / 상권: 부산·서면/전포·부전시장 / 분기 / 값 / 단위 / R-ONE 통계표ID / 비고 |
| 단위 | 파일 `단위` 칸: 공실률 %, 임대료 천원/㎡ |
| 결측·주의 | 비고 칸은 483행이 빈칸(20행만 상권명 메모). 값 칸 9행은 셀 저장값 끝자리 오차가 그대로 있음(예: 8.300000000000001). 2024Q3·2026Q3 표본 개편. R-ONE 원문과 대조 못 함 |

## 소상공인시장진흥공단_상가(상권)정보_20260930.zip 안 부산 CSV → sbiz_store_busan_202609_clean.csv

| 명세 칸 | 내용 |
|---|---|
| 제공기관 | 소상공인시장진흥공단 (SOURCE-day03.md 2번, SOURCE.md 4번) |
| 갱신주기 | 분기 (SOURCE-day03.md 2번, SOURCE.md 4번) |
| 기준 시점 | 파일 안 날짜 칸 없음 → 파일 이름 기준 2026-09 판 (SOURCE-day03.md 2번) |
| 행 수 | 원본 157296행 × 39칸 → 정리 후 157296행 × 37칸. **뺀 열 2개: 동정보, 호정보**(모든 행 빈칸). 뺀 행 0 |
| 컬럼 뜻 | 상가업소번호, 상호명, 지점명, 상권업종 대·중·소분류 코드·이름, 표준산업분류 코드·이름, 시도·시군구·행정동·법정동 코드·이름, 지번 관련 칸, 도로명 관련 칸, 건물명, 도로명주소, 구·신우편번호, 층정보, 경도, 위도 (칸 목록은 SOURCE-day03.md 2번과 같음) |
| 단위 | 경도·위도: 못 찾음 |
| 결측·주의 | 빈 칸 수: 지점명 140409, 건물부번지 132794, 건물명 102993, 층정보 73100, 지번부번지 19874, 표준산업분류코드·명 14, 지번본번지 5. 등록 점포 목록이지 영업 여부·매출은 없음(SOURCE-day03.md). 원본 인코딩 UTF-8 BOM. 원본 ZIP은 그대로 둠 |

## 끝 기준

- [ ] 정리한 CSV를 엑셀로 열어 한글이 깨지지 않음(보기만, 저장하지 말고 닫기) → **아직 안 함** (파일 앞에 BOM이 들어간 것만 확인)
- [x] 원본 행 수를 적음
- [x] 명세 7칸을 모두 채움
- [x] 단위 칸에 찾은 곳 또는 '못 찾음'을 적음
