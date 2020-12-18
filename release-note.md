# Release Notes

## 2020-11-20

### 기능 추가

- multiple sort 기능
- 컬럼 사이즈 조절 기능

## 이슈 처리

- 편집기창과 그리드 사이의 높이 유동적으로 조절 가능하도록 개선 [#12](https://github.com/sinsiway/data-studio-alpha/issues/12)
- 로그인된 상태에서 URL 복사 후 이기종 브라우저에서 해당 URL로 접속 시 로그인 화면으로 돌아가도록 변경 [#16](https://github.com/sinsiway/data-studio-alpha/issues/16)
- 처리 불가 세션 닫을 때 트랜젝션 롤백 여부 알림 오류 수정 [#24](https://github.com/sinsiway/data-studio-alpha/issues/24)
- 접근 가능한 DB 추가 시 Alias 글자 수 제한에 공백이 포함되던 오류 수정 [#23](https://github.com/sinsiway/data-studio-alpha/issues/23)
- soha DB세션에서 실행 계획 선택시 UI가 멈추는 현상 수정 [#22](https://github.com/sinsiway/data-studio-alpha/issues/22)


## 2020-11-10

- #### 이슈 처리

```
  - 업데이트 내역 "다시 보지 않기" 동작하지 않는 현상
  - 에디터 닫을 때 "auto commit" 옵션이지만 트랜젝션이 있다고 나오는 현상
  - 검색 후 재검색이 되지 않는 현상
  - 필터 적용 후 전체 필터 해제 시 필터 마크가 남아있는 현상
  - SQL Editor 결과 메뉴 중 실행계획 선택 시 행 걸리는 현상
  - SQL 실행 오류 : SQL 실행 실패 및 행 걸리는 현상
  - DB 접속 결과 확인 불가
  - SOHA DB 데이터 boolean 타입 출력 오류
  - SQL 실행 오류 : 다중 쿼리 SELECT 실행시 실행 결과 미출력
  - 2개 이상의 동일한 DB 탭 접속 후, DB탭 일부 닫기 시, 나머지 탭에서도 연결이 종료되는 현상
  - Data Edit 기능 사용시 soha에서 insert, update, delete 문장이 수행 가능하도록 완성되도록 개선
  - row 추가시 숫자형 컬럼에 문자로 인식되어 나던 오류 수정
  - row 추가시 date 컬럼의 날짜가 일반 포맷(yyyy-mm-dd hh:mm:ss) 및 현재시간으로 셋팅 되도록 개선
```

## 2020-10-23

- #### 대용량 처리 기반 테이블 플러그인 개발 및 적용(petra-grid)
  <img src="/images/20201023_3.png" width="100%"/>

```
  - 다중 필터링
  - 50만건 이상의 데이터도 20건과 같은 렌더링 속도 보장
  - 페이지 기반의 그리드에서 스크롤 기반으로
  - table data 변경 기능
  - 셀 범위 선택 및 복사, 붙여넣기 등(엑셀 호환)
  - 데이터 파일로 내보내기(type : json, csv, excel, xml, txt)
```

- #### 업데이트 알림 기능 추가
  <img src="/images/20201023_4.png" width="100%"/>

```
  - 현재 업데이트 내용을 볼수 있는 바로가기 제공
  - 환경설정 > 기타 > 업데이트 관리 > 내역 바로가기(관리자 접속시 해당 환경 설정에서 사용자 다시 보지않기를 초기화 가능)
```

- #### 자동 로그아웃 및 세션 연장 기능 추가
  <img src="/images/20201023_1.png" width="400px"/>

```
  - 설정된 세션 시간 만료시 로그인 페이지로 이동
```

- #### 이슈 처리

```
  - where 절 조건에 맞지 않는경우 레코드가 0 이어야 하는데 전에 조회한 값이 보이는 현상 수정
```

## 2020-09-25

> 알파 테스트 페이지 오픈. [사용해보기](http://ds.sinsiway.com/petra/init.do)
