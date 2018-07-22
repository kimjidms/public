# 알아두면 쓸모있는 SQL 기능,명령어

SQL 기능, 명령어 \(계속 추가중\)

\(참고 : https://www.w3schools.com/sql/default.asp

**EXPLAIN 명령어**

SELECT 쿼리의 performance를 확인하는 명령어

쿼리를 수행하기 전에 데이터를 어떻게 가져올 것인지 그 '실행계획'을 분석해서 보여주는 명령어.

원하는 쿼리를 SELECT로 바꾼 후, 앞에 EXPLAIN 을 붙여서 실행

\(컬럼별 내용 상세 : https://in1n4.blog.me/10035411273



**컬럼 값에 콤마\(,\)로 합치거나 나누기 명령어**

CONCAT : 컬럼값 합치기

SUBSTR : 컬럼값 나누기 \(http://naver.me/59EAYK0Q\)



**DSITINCT 명령어**

SELECT 쿼리에서 중복값을 제거하기 원하는 컬럼의 이름을 써준다. 정렬된 값을 얻으려면 ORDER BY를 사용해야한다.



**BEGIN COMMIT, ROLLBACK 명령어**

BEGIN : 트랜잭션을 시작한다는 뜻으로 begin 이후의 모든 명령들은 취소할 수 있다.

COMMIT : 트랜잭션을 종료한다는 명령어로 실제 쿼리문이 반영이되며 취소할 수 없다.

이 명령어를 사용하면 begin 이전으로 복구된다.



**FIND\_IN\_SET\('\[찾을값\]',\[컬럼명\]\)**

컬럼 안에 데이터가 콤마로 구분되어 저장된 경우, 'c'만 찾고싶지만 다른 속성값에 'cc'도 있다면 '%c%'로 찾을 수 없다. 따라서 이때 사용하는 명령어이다.



**SQL\_NO\_CACHE**

대부분의 DB가 그렇듯이 한번 select하면 메모리에 올려져 있으므로 같은 퀴리로 계속 호출하면 메모리에 올라와 있는것을 읽으므로 속도가 개선된것처럼 착각을 할 수 있다. 이럴 땐 퀴리에 sql\_no\_cache 를 붙여서 캐쉬를 사용하지 않으면 된다.

ex\) SELECT **SQL\_NO\_CACHE** A.\* FORM A;

