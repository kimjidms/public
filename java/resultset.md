# ResultSet

ResultSet? 

1. 결과를 저장하는 하나의 집합 2. DB에서 처리된 결과 3. DB로부터 실행된 결과 값을 임시로 저장하는 객체

ResultSet rs = ps..exeuteQuery\(\); rs.next\(\)

* rs에는 4 or 8 바이트 heap 메모리의 주소값이 들어가있다. + a
* FetchSize 설정이 중요하다. \(Out Of Memory의 주요 원인\)
* 해당 블로그 내용 참고 : http://dudaji.tistory.com/m/entry/ResultSet-의-동작-구조  

