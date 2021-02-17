# Release Notes


## 2020-2-17

### 업데이트 내용

- Shared SQL에서 특정 사용자 및 조직에게만 공유하도록 하는 기능 개선
- SQL 실행 오류 시 이력에 안남던 오류 수정
- 결과 export 기능이 접속된 db에서 수행되지 않던 오류 수정
- [mysql] 서브 쿼리 수행에서 결과가 다중일 경우 행걸리는 현상 수정
- 툴팁 미적용 기능 아이콘들에 대하여 툴팁 일괄 적용
- SQL History > Shared SQL 등록 기능 미작동 오류 수정
- [mysql] curtime() 함수가 빈값으로 나오던 오류 수정
- 결과창 정렬 인터페이스 개선
- 날짜형 데이터 정렬이 안되던 오류 수정
- View column 보기에서 긴 문자열이 다음노드로 넘어가 보이는 현상 수정
- Value cell 판넬이 해상도 조절에 따라 높이가 조절되도록 변경
- 결과창 필터 기능에서 데이터가 null인 경우도 컬럼 타입에 따라서 필터링 가능하도록 개선
- 다중 필터링 기능 알고리즘 개선
- 필터 팝업에서 선택한 컬럼의 목록의 정렬이 숫자, 문자일 경우 구분되어 오름 차순 정렬 되도록 개선
- 새로고침시 '새로고침 완료' 토스트 메시지 표시하도록 개선
- 환경 설정 > 세션 타임 아웃이 설정 안되던 오류 수정
- 자동완성 기능 개선(알파벳 순, view, db, schema 카테고리 추가, Templete 카테고리 삭제)
- 편집기에 Schema, db 선택 가능하도록 기능 추가
- 전체 필터링 -> 카테고리별 필터링 선택 가능하도록 기능 추가(sql history에만 추가됨)
- 사용자 신청 과 이메일 인증 통합화
- 로그인 후 첫 메인페이지 로딩시 시간이 너무많이 소요되는 현상 개선
- 비밀번호 찾기 시 잘못된 사용자 정보를 입력할 경우 아무런 결과나 나오지 않던 오류 수정
- 지원 db 오브젝트 트리에서 특정 오브젝트의 숫자가 잘못 표기되거나, 하위 오브젝트를 볼 수 없던 오류 수정
- [mongodb] aggregate method가 특정 상황에서 동작하지 않는 오류 수정
- [mongodb] 지원 method 추가 -> creatUser, createCollection, insertMany, bulkWrite
- 동일 컬럼명 조회 시 출력 오류 수정
- [soha db] auto script 기능이 동작하지 않던 오류 수정
- SQL Editor 최근 작업 내용 저장 기능을 일관성 있도록 개선


## 2020-12-18

### 기능 추가

#### DBMS 접근 관리
<img src="/images/20201218_1.gif" width="100%"/>

- 사용자, 조직별 접근 가능한 DBMS를 한눈에 파악 할 수 있습니다.
- N개의 DBMS를 선택하고 N개의 사용자 및 조직을 추가 가능합니다.
- 관리자 로그인 시 좌측 네비게이션바에 DBMS 접근 관리 항목이 보여집니다.
- 알파 테스트를 위해 해당 기능은 미활성화 상태로 업데이트 됩니다.

### 오류 수정 및 기능 개선

- MongoDB java Driver 상위 버전에 맞도록 소스 코드 개선(version 3.12 -> 4.1)
- 편집기 창에서 MongoDB 접속일 경우 Database 선택하여 구문 수행하도록 변경
- MongoDB 등록 모달에서 인증 db와 사용자, 비밀번호 미입력시에도 등록 되도록 개선
- MongoDB의 오브젝트 트리에서 사용자 우클릭시 메뉴 사용자 생성, 비밀번호 변경, 권한 변경 안되던 오류 수정

### 이슈 처리

- [연구소_박종한]mongodb 쿼리 실행 결과값 안보이는 현상 [#38](https://github.com/sinsiway/data-studio-alpha/issues/38)
- [연구소_박종한]mongodb 객체검색기 안보이는 현상 [#37](https://github.com/sinsiway/data-studio-alpha/issues/37)
- [연구소_김동훈] 결과창 아이콘 구분바 추가 요청 [#33](https://github.com/sinsiway/data-studio-alpha/issues/33)
- [R&D_류대석] 화면 DB접속 탭이 하나로 연결되어 보이는 현상 [#32](https://github.com/sinsiway/data-studio-alpha/issues/32)



## 2020-11-20

### 기능 추가

#### multiple sort 기능
<img src="/images/20201120_1.gif" width="100%"/>

#### 컬럼 사이즈 조절 기능
<img src="/images/20201120_2.gif" width="100%"/>

### 이슈 처리

- 편집기창과 그리드 사이의 높이 유동적으로 조절 가능하도록 개선 [#12](https://github.com/sinsiway/data-studio-alpha/issues/12)
- 로그인된 상태에서 URL 복사 후 이기종 브라우저에서 해당 URL로 접속 시 로그인 화면으로 돌아가도록 변경 [#16](https://github.com/sinsiway/data-studio-alpha/issues/16)
- 처리 불가 세션 닫을 때 트랜젝션 롤백 여부 알림 오류 수정 [#24](https://github.com/sinsiway/data-studio-alpha/issues/24)
- 접근 가능한 DB 추가 시 Alias 글자 수 제한에 공백이 포함되던 오류 수정 [#23](https://github.com/sinsiway/data-studio-alpha/issues/23)
- soha DB세션에서 실행 계획 선택시 UI가 멈추는 현상 수정 [#22](https://github.com/sinsiway/data-studio-alpha/issues/22)



## 2020-11-10

### 이슈 처리

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



## 2020-10-23

### 기능 추가
#### 대용량 처리 기반 테이블 플러그인 개발 및 적용(petra-grid)
<img src="/images/20201023_3.png" width="100%"/>

- 다중 필터링
- 50만건 이상의 데이터도 20건과 같은 렌더링 속도 보장
- 페이지 기반의 그리드에서 스크롤 기반으로
- table data 변경 기능
- 셀 범위 선택 및 복사, 붙여넣기 등(엑셀 호환)
- 데이터 파일로 내보내기(type : json, csv, excel, xml, txt)

#### 업데이트 알림 기능 추가
<img src="/images/20201023_4.png" width="100%"/>

- 현재 업데이트 내용을 볼수 있는 바로가기 제공
- 환경설정 > 기타 > 업데이트 관리 > 내역 바로가기(관리자 접속시 해당 환경 설정에서 사용자 다시 보지않기를 초기화 가능)


#### 자동 로그아웃 및 세션 연장 기능 추가
<img src="/images/20201023_1.png" width="400px"/>

- 설정된 세션 시간 만료시 로그인 페이지로 이동

### 이슈 처리

- where 절 조건에 맞지 않는경우 레코드가 0 이어야 하는데 전에 조회한 값이 보이는 현상 수정


## 2020-09-25

> 알파 테스트 페이지 오픈. [사용해보기](http://ds.sinsiway.com/petra/init.do)
