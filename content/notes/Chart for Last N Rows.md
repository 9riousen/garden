---
title: "최근 N개의 row로 차트 생성하기"
date: '2023-06-25'
images: ['https://exceljet.net/sites/default/files/styles/original_with_watermark/public/images/formulas/last%20n%20rows%20in%20a%20range_0.png']
---
![last n rows](https://exceljet.net/sites/default/files/styles/original_with_watermark/public/images/formulas/last%20n%20rows%20in%20a%20range_0.png)
- Google Sheets 기준으로 (Excel은 `OFFSET`이 뭔가 잘 안됨)
- 매일 row가 하나씩 추가되는 데이터가 있을 때 최근 1주일 chart자동으로 업데이트 하기
- [예제](https://docs.google.com/spreadsheets/d/1ophinHLHNahxgOWKxr_P0gYPxvSFSSa4pil4_rZ0oIM/edit?usp=sharing)

## `OFFSET()`
![[notes/images/offset.png]]
- `=offset(A3,2,0,10,1)` 을 입력하면 3번 그림 처럼 셀들의 내용이 자동 입력된다
	- 해석: `A3`을 기준으로 `2` row 아래, `0` column 오른쪽의 내용을 현재 `10 rows x 1 column` 만큼 cell에(부터) 입력하라
	- 특이하게도 `C6`  이나 `C7` 등에서 backspace등을 눌러도 내용이 지워지지 않는다
	- 지우려면 `C5`의 내용을 지우면 한꺼번에 제거됨
- 현재 입력하는 셀의 위치는 상관없다

## `COUNT()`
- 내용이 있는 row의 수를 반환한다
- `=COUNT(A:A)`
	- 전체 row의 수(빈 row 빼고)

## Chart data source
둘을 조합한 영역을 data source로 설정하면 원하는 차트를 만들 수 있다

---
- [[tags/Spreadsheet|Spreadsheet]]
- [OFFSET 함수 - Microsoft 지원](https://support.microsoft.com/ko-kr/office/offset-%ED%95%A8%EC%88%98-c8de19ae-dd79-4b9b-a14e-b4d906d11b66)
