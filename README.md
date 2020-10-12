# ToadForOracle
- [Toad(wiki)](https://ko.wikipedia.org/wiki/TOAD)

## Toad사용법

1. 로그인(Connection)
   - DB Server 에 로그인할 수 있음

2. Object Palette 활용법

3. Schema Browser 사용법
   - ERD 확인 가능
   - 테이블 속성 확인 가능
   - SQL Builder 사용법
     - 테이블이 이미 생성이 되어 있으면 원하는대로 Diagram을 움직여 쿼리를 제작할 수 있음

4. SQL Editor 사용법
   - 직접 SQL 을 코딩할 수 있음.

## DBLink

- 현재 접속해있는 스키마에서 다른 스키마로의 연결을 제공해주는 link
- 알아두기!
  - ``BLOB``, ``CLOB`` 는 DBLink 로 다룰 수 없다.

## 내장 함수

- ROW_NUMBER() OVER()
  - PARTITION BY : 내부 파라미터를 그룹핑해서 NUMBERING을 실시한다.
    - **주의) 꼭 ORDER BY 와 함께 사용해야 한다.**
    - ex) ROW_NUMBER() OVER(PARTITION BY USR_ID ORDER BY USR_ID)
  - ORDER BY : 내부 파라미터를 기준으로 SORTING을 실시한 후에 NUMBERING을 한다.
    - ex) ROW_NUMBER() OVER(ORDER BY USR_ID)

- ROWNUM
  - 단순하게 NUMBERING을 한다.
    - **주의) SELECT의 실행순서보다 ORDER BY 가 늦기 때문에 ROWNUM을 사용한 후 ORDER BY 를 실시하게 되면 순서가 뒤엉키게 된다.
  
