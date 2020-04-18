

# NoSQL  


## Why NoSQL is better?  

## 1. NoSQL은 scale-out에 강하다.  

1. **ACID** 관점 : master노드와 slave사이 데이터 동기화를 통한 Consistency 보장이 어렵다.  
[why?](https://softwareengineering.stackexchange.com/questions/194340/why-are-nosql-databases-more-scalable-than-sql)  

2. **join의 관점** : join할 두 테이블이 다른 서버에 저장되어 있다면, 
[why?](https://www.quora.com/Why-is-it-said-that-relational-SQL-databases-do-not-scale)  


## 2. 고정된 강한 제약조건인 스키마가 없기에, 데이터 유형 변화에 기민하게 반응할 수 있다.  

정형 데이터, 반정형 데이터, 비정형 데이터  

현재 인류에 맞게끔 스키마를 설계해서  
[몸 | 머리 | 팔 | 다리] 라는 테이블을 설계했다.  
그러다 100년 후 꼬리 달린 인류가 나오게 되면  
[몸 | 머리 | 팔 | 다리 | 꼬리] 로 스키마 재설계해야 한다.  
100년 간 누적된 record에 전부 꼬리 field를 null로 넣어야 한다?  



## 3. 속도의 측면  

NoSQL이 더 빠르다.  

RDB가 성능 향상을 위하여 할 수 있는 방법은  
1) Query-off  
2) Sharding  
3) SQL tuning  
4) 그러다가 Denormalization이 된다.  

정규화는 데이터 간 redundancy를 최소화하여 anomaly를 없애는 목적이었으나,  
그 결과 여러 테이블로 쪼개지고 이는 high cost한 JOIN 연산의 필요로 이어진다.  

JOIN이 비싸다보니, 아차 정규화 괜히했구나 싶어 호다닥 테이블을 다시 붙인다. 
즉, 데이터의 중복을 허용한다.  

이렇게 할 거였으면
애초에 중복되게 저장하면 되고,  
그것이 NoSQL에서의 데이터 저장방식  

[why nosql is needed?](https://www.dezyre.com/article/nosql-vs-sql-4-reasons-why-nosql-is-better-for-big-data-applications/86)  


## ACID vs BASE  
[BA/S/E 가 뭔데?](https://ssup2.github.io/theory_analysis/CAP_ACID_BASE/)  



