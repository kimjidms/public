---
description: 정규화
---

# Normalization

데이터 베이스에서 정규화?

관계형 데이터베이스에서 중복 작업을 최소화하기 위해 정보를 나누는 작업. 프로그램 처리속도를 개선이 목표. 특히 데이터의 수정 시 반복된 작업을 제거하기 위해 필수적이다.

정규화의 종류?

1NF, 2NF, 3NF, 4NF, 5NF 등이 있다. 하지만 일반적으로 사용하는 단계에서는 3NF만 만족해도 충분하다.

1NF

각 속성은 반드시 원자값을 가져야한다. 하나의 컬럼에 나누어 질 수 없는 값을 넣어선 안된다.

| 이름 | 이메일 |
| --- | --- | --- |
| 김에이 | a@abc.com |
| 김삐이 | b@abc.com |

다음과 같이 테이블을 구성한다.

| 이름 | 연락처 |
| --- | --- | --- |
| 김에이 | 010-1234-6789 |
| 김삐이 | 010-9876-5432, 010-1212-1212 |

위에 표는 1NF의 위배되는 테이블이다.

2NF

완전 함수 종속을 만족해야한다. \(부분함수 종속 제거\) KEY가 아닌 모든 칼럼은 KEY에 의존적이여야 한다.

| 상품명 | 주문자명 | 주소 | 연락처 |
| --- | --- | --- |
| 한글책 | 김에이 | 서울시 | 010-1234-6789 |
| 영어책 | 김삐이 | 경기도 | 010-9876-5432 |

주문 정보가 들어있는 테이블에서 상품명과 주문자 명이 기본키가 된다. 하지만 부분적으로 함수가 종속되어 있고 이를 제거하지 않으면 수정시 불필요하게 많은 데이터를 반복적으로 수정해야하는 경우가 발생 할 수도 있다.

| 주문자 명 | 주소 | 연락처 |
| --- | --- | --- |
| 김에이 | 서울시 | 010-1234-6789 |
| 김삐이 | 경기도 | 010-9876-5432 |

| 상품명 | 주문자명 |
| --- | --- | --- |
| 한글책 | 김에이 |
| 영어책 | 김삐이 |

다음과 같이 테이블을 나누어 부분함수 종속을 제거한다.

3NF

이행적 종속 관계 제거. 기본 키에 의존하지 않고 일반 칼럼에 의존하는 경우를 제거해야한다.

A -&gt; B, B-&gt;C 그러면 A-&gt;C인 관계를 제거해야한다.

