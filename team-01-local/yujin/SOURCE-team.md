# SOURCE-team · inputs-team/ 데이터 출처 목록

> `inputs-team/` 폴더에 팀이 모은 데이터의 출처를 적은 목록입니다. 강사가 준 `inputs/` 데이터의 출처는 `SOURCE.md`에 있습니다.
> 작성: 조유진 · 2026-11-17 (확인일도 모두 2026-11-17)
> 원본 파일은 받은 그대로 두었습니다. 숫자를 고치거나 반올림한 파일은 없습니다.
> 인증키는 어느 파일에도 적지 않았습니다. 아래 호출 주소의 `serviceKey`는 각자 발급받은 키를 넣습니다.

## 한눈에

| 번호 | 파일 | 행 수 | 기간 | 단위 | 출처 (직접 연 페이지) | 상태 |
|---|---|---:|---|---|---|---|
| 1 | `busan_dongsales_time_{동}_20261117.json` × 4 | 동마다 1080 | 2023-01 ~ 2026-09 (월) | 행정동 | https://www.data.go.kr/data/15164416/openapi.do | 확인 필요 |
| 2 | `busan_dongsales_age_{동}_20261117.json` × 4 | 동마다 270 | 2023-01 ~ 2026-09 (월) | 행정동 | https://www.data.go.kr/data/15164394/openapi.do | 확인 필요 |
| 3 | `busan_dongsales_gender_{동}_20261117.json` × 4 | 동마다 90 | 2023-01 ~ 2026-09 (월) | 행정동 | https://www.data.go.kr/data/15164384/openapi.do | 확인 필요 |
| 4 | `busan_dongsales_biz_{동}_20261117.json` × 4 | 동마다 495 | 2023-01 ~ 2026-09 (월) | 행정동 | https://www.data.go.kr/data/15164434/openapi.do | 확인 필요 |
| 5 | `busan_dongpop_age_{동}_20261117.json` × 4 | 동마다 282 | 2023-01 ~ 2026-09 (월) | 행정동 | https://www.data.go.kr/data/15164376/openapi.do | 확인 필요 |
| 6 | `부산_서면전포_부전시장_상업용부동산_임대동향_2020-2026.xlsx` | 원자료 시트 503 | 2020Q1 ~ 2026Q3 (분기) | R-ONE 상권 | https://www.reb.or.kr/r-one/portal/stat/easyStatPage.do (파일에 적힌 출처) | 확인 필요 |
| 7 | `busan_commercial_history_20261117/page_0001~0337.json` | 336235 | 인허가·폐업일 ~ 2023-06-01 | 주소(법정동) | 호출 주소만 확인, 상세 페이지 못 찾음 | 확인 필요 |
| 8 | `busan_commercial_change_20261117.json` | 477 | 기준 시점 없음 | 상권 477곳 | https://www.data.go.kr/data/15095252/openapi.do | 확인 필요 |
| 9 | `소상공인시장진흥공단_상가(상권)정보_20260930.zip` | 부산 CSV 157,296 | 2026-09 판 | 점포(행정동 칸 있음) | https://www.data.go.kr/data/15083033/fileData.do (SOURCE.md에 적힌 주소, 직접 열지 않음) | 확인함 |

- `{동}`은 `bujeon1`(부전1동), `bujeon2`(부전2동), `jeonpo1`(전포1동), `jeonpo2`(전포2동)입니다.
- 행정동 코드: 부전1동 2623051000, 부전2동 2623052000, 전포1동 2623060000, 전포2동 2623061000
- 상태가 `확인 필요`인 이유는 파일마다 아래 '조심할 점'에 적었습니다.

## 1~4. 카드 이용금액·건수 (부산광역시, 행정동별 월별 일평균)

공통 사항

- 제공기관: 부산광역시 (담당부서 빅데이터담당관)
- 공통 요청변수: serviceKey, pageNo, numOfRows, resultType (필수) / stdYm, hname (선택)
- `hname`에는 "부산진구 부전1동"처럼 구 이름까지 넣어야 결과가 나옵니다. "부전1동"만 넣으면 NODATA_ERROR가 납니다.
- 공통 응답 칸: `stdYm`(기준년월), `hcode`, `hname`, `avgAmt`(이용금액), `avgCnt`(이용건수) + 데이터마다 구분 칸 1개
- 파일데이터 설명에 따르면 네 데이터 모두 "카드사 가맹점 행정동별 승인된 결제 건"의 전월 일평균입니다. 개인정보 비식별화를 위해 월 단위로 집계했습니다.

| 번호 | 데이터셋 이름 | 호출 주소 | 구분 칸 | 파일데이터 설명 |
|---|---|---|---|---|
| 1 | 부산광역시_일평균 카드 이용금액 및 건수(행정동·시간) | `https://apis.data.go.kr/6260000/DongSalesTimeService/getDongSalesTime` | `times` 00시~23시 (24개) | https://www.data.go.kr/biz/dcat/metadata/15147852.do |
| 2 | 부산광역시_일평균 카드 이용금액 및 건수(행정동·연령) | `https://apis.data.go.kr/6260000/DongSalesAgeService/getDongSalesAge` | `ages` 20대미만~60대이상 (6개) | https://www.data.go.kr/biz/dcat/metadata/15147849.do |
| 3 | 부산광역시_일평균 카드 이용금액 및 건수(행정동·성별) | `https://apis.data.go.kr/6260000/DongSalesGenderService/getDongSalesGender` | `gender` 남성·여성 | https://www.data.go.kr/biz/dcat/metadata/15147846.do |
| 4 | 부산광역시_일평균 카드 이용금액 및 건수(행정동·업종) | `https://apis.data.go.kr/6260000/DongSalesBizService/getDongSalesBiz` | `ryLNm` 업종 대분류 11개 | https://www.data.go.kr/biz/dcat/metadata/15147853.do |

- API 페이지 수정일: 네 개 모두 2026-11-06
- API 전체 행 수(totalCount): 시간 221,599 / 연령 55467 / 성별 18490 / 업종 101695

조심할 점

- 금액 단위가 원인지, 몇 개 카드사 자료인지 적혀 있지 않습니다. [확인 필요]
- 시간·연령·성별 API의 동별 합계는 서로 금액 0~2, 건수 0~4만큼 다릅니다.
- **업종 API 합계는 다른 세 API와 크게 다릅니다.** 예: 2026-09 부전1동 업종 합계 569328966, 시간 합계 1960731092. 공개 설명으로는 이유를 알 수 없습니다. 확인 전까지는 같은 동 안에서 업종끼리 비율로만 씁니다.
- 업종 이름 `음식료품`이 2026-01부터 `음식료픔`으로 바뀝니다. 원본은 그대로 두고, 정리본에서만 합칩니다.
- 성별 파일데이터 설명(15147846)에 '업종(중)별'이라는 문장이 들어 있습니다(설명 오류로 보임).
- 관련 노트: `research/2026-11-12-seomyeon-card-sales.md`

## 5. 생활인구 (부산광역시, 행정동·연령, 통신사)

- 데이터셋: 부산광역시_일평균 생활인구수(행정동·연령, 통신사)
- 호출 주소: `https://apis.data.go.kr/6260000/DongPopAgeService/getDongPopAge`
- API 페이지 수정일 2026-11-06, API 전체 행 수 57,936
- 응답 칸: `stdYm`, `hcode`, `hname`, `ages`, `hpopAvg`·`wpopAvg`·`vpopAvg` (주거·직장·방문 인구로 추정)

조심할 점

- 2026-08·09는 같은 행이 두 번씩 들어 있습니다. 동마다 282행 중 12행이 중복이라, 중복을 빼면 270행입니다.
- 2026-08부터 `20대미만`이 `20세미만`으로 바뀝니다.
- hpop·wpop·vpop 칸 정의 문서는 찾지 못했습니다. [확인 필요]
- **같은 기관의 성별 API(https://www.data.go.kr/data/15164442/openapi.do)는 아직 못 받았습니다.** 인증키가 이 API에 등록되지 않아 "SERVICE_KEY_IS_NOT_REGISTERED_ERROR"가 납니다. 활용신청이 필요합니다.
- 관련 노트: `research/2026-11-12-seomyeon-living-population.md`

## 6. 상업용부동산 임대동향 (한국부동산원 R-ONE, xlsx)

- 파일에 적힌 출처: 한국부동산원 R-ONE, 상업용부동산 임대동향조사 > 임대정보 > 지역별 공실률 / 지역별 임대료 (파일 '안내' 시트 B3)
- 파일 안 조회일: 2026-11-17 / 팀에서 정리해 넣은 파일입니다. 작성자는 파일에 없습니다.
- 시트: 안내, 공실률, 임대료, 원자료(503행). '원자료' 503행과 표 시트 값은 모두 같습니다.
- 지역: 부산 전체, 서면/전포 상권, 부전시장 상권 / 단위: 공실률 %, 임대료 천원/㎡(월)
- R-ONE 통계표 ID: '안내' 시트 B21~B28

조심할 점

- 행정동이 아니라 R-ONE '상권' 단위입니다. 행정동 4곳과 경계가 어떻게 겹치는지 모릅니다. [확인 필요]
- 2024Q3·2026Q3에 표본이 바뀌었습니다. 이 분기 전후 값은 바로 비교하지 않습니다.
- 셀 안에는 `8.300000000000001`처럼 끝자리가 붙은 값이 있습니다. 노트에는 엑셀 화면 값(8.3)으로 적었습니다.
- **R-ONE 원문과 대조하지 못했습니다.** R-ONE Open API는 인증키 없이 부르면 표마다 맛보기 5행만 줍니다. R-ONE 인증키가 필요합니다.
- 관련 노트: `research/2026-11-17-seomyeon-vacancy-rent.md`

## 7. 상권 점포이력 (부산광역시)

- 서비스 이름: 부산광역시_상권 점포이력정보서비스 (팀에서 전달받은 이름)
- 호출 주소: `https://apis.data.go.kr/6260000/BusanCommercialHistoryService/getCommercialHistoryList`
- 저장: `inputs-team/busan_commercial_history_20261117/` 안에 1000행씩 337개 파일 (page_0001.json ~ page_0337.json), 합계 336235행, 약 97MB
- 응답 칸: `trdstatenm`(영업상태), `bplcnm`(상호), `majornm`·`minornm`(업종 대·소분류), `upjongnm`(업태), `rdnwhladdr`(도로명주소), `apvpermymd`, `dcbymd`, `geom`(좌표)

조심할 점

- **인허가일·폐업일이 2023-06-01에서 끝납니다.** 2024~2026년 개·폐업은 없습니다.
- 행정동 칸이 없습니다. 도로명주소 끝 괄호의 법정동(부전동·전포동)으로 골랐습니다.
- 도로명주소가 빈 행 59097, 인허가일이 빈 행 12758, 완전히 같은 행 202개가 있습니다.
- 공공데이터포털 상세 페이지를 찾지 못했습니다. `apvpermymd`=인허가일, `dcbymd`=폐업일은 칸 이름과 값으로 추정한 것입니다. [확인 필요]
- 소분류에 `카페`가 없고, `전자상거래업`(온라인 판매 신고로 보임)이 많습니다.
- 관련 노트: `research/2026-11-17-seomyeon-store-openclose.md`

## 8. 상권 변화지표 (부산광역시)

- 데이터셋: 부산광역시_상권 변화지표정보서비스 (담당부서 빅데이터담당관, 등록일 2021-11-29, 수정일 2025-07-29, 업데이트 주기 '실시간')
- 호출 주소: `https://apis.data.go.kr/6260000/BusanCommercialChangeService/getCommercialChangeList`
- 응답 칸: `type_nm`(상권구분명), `comm_nm`(상권명), `change_indicator_nm`(변화지표값), `average_open_months`(평균생존개월수), `average_close_months`(평균폐업개월수), `busan_average_open_months`·`busan_average_close_months`(부산 평균)

조심할 점

- 데이터 기준 시점이 없습니다. 페이지에도, 응답에도 날짜가 없습니다. [확인 필요]
- '다이나믹·상권확장·상권축소·정체'의 공식 정의가 페이지에 없습니다. [확인 필요]
- 시장 노트의 시장 9곳 가운데 5곳은 이 데이터에 이름이 없습니다.
- 관련 노트: `research/2026-11-17-seomyeon-store-openclose.md`

## 9. 상가(상권)정보 (소상공인시장진흥공단, ZIP)

- 공식 출처와 설명은 `SOURCE.md` 4번에 있습니다. 원본 ZIP을 `inputs-team/`에 둔 것입니다.
- 부산 CSV(`소상공인시장진흥공단_상가(상권)정보_부산_202609.csv`)는 157,296행, 39개 열입니다. 개업일·폐업일 칸은 없습니다.
- 부산진구 20,668곳, 대상 행정동 부전1동 2,759 / 부전2동 4,174 / 전포1동 2,078 / 전포2동 1,347곳
- 관련 노트: `research/2026-11-12-seomyeon-market.md`, `keyword-map.md`

## 아직 없는 데이터

| 필요한 것 | 왜 | 지금 상황 |
|---|---|---|
| 생활인구 성별 | 카드 성별과 짝 맞추기 | 활용신청 필요 (https://www.data.go.kr/data/15164442/openapi.do) |
| R-ONE 원문 값 | 6번 파일 대조 | R-ONE Open API 인증키 필요 |
| 2024~2026 개·폐업 | 판단 기준 ②의 최근 변화 | 출처를 아직 찾지 못함 |
| 리뷰 데이터 | 6주 목표의 리뷰 분석 | 팀에서 플랫폼을 정해야 함 |
| 상권·행정동 경계 | 행정동 데이터와 상권 데이터 맞추기 | 출처를 아직 찾지 못함 |

## 부산시 빅데이터담당관에 물어볼 것

1. 카드 업종 API 합계가 시간·연령·성별 API와 크게 다른 이유
2. 카드 `avgAmt` 단위(원인지)와 카드사 범위
3. 상권 변화지표의 기준 시점, 네 분류의 정의
4. 상권 점포이력 API가 2023-06-01에서 멈춘 이유와 갱신 계획, 칸 정의
