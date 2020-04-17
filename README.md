# systme-design

 **모든 것은 빠르고 정확하게 해내기 위한 과정이다.**  
 **모든 것은 Trade-off다**  

## Terminology  

#### fail over [장애 조치](http://www.terms.co.kr/failover.htm)  



## CAP Theorem  

[about](https://hamait.tistory.com/197)  


## Consistency Pattern  

 * 분산 시스템에서, replica 서버에 데이터를 어떻게 동기화할 것인가에 대한 level.  
 [eventual consistency](https://stackoverflow.com/questions/10078540/eventual-consistency-in-plain-english)  
 [Strong consistency vs ](https://www.nurinamu.com/trans/2016/04/03/balancing-strong-and-eventual-consistency-with-google-cloud-datastore/)   
 
## Availability Pattern  

 * 시스템이 얼마나 365일 무중단 서비스를 제공할 수 있는가에 대한 지표  
 
 * 두 가지 방법  
 1. Fail over  
 [Active-active](https://bae-juk.tistory.com/26)  
 [Active-passive]()  
 
 
 2. Replication  
 
 ## DNS  
 
 [DNS 등록 및 흐름](https://opentutorials.org/course/3276/20307)  
 [How it works](https://www.netmanias.com/ko/post/techdocs/5259/dns-network-protocol/dns-basic-operation)  
 [How it works 2](https://opentutorials.org/course/3276/20303)  
 [그외) 1. 무료 domain 할당](https://j-history.tistory.com/9)  
 [그외) 2. domain을 Route53으로 연결](https://tech.cloud.nongshim.co.kr/2018/10/16/%EC%B4%88%EB%B3%B4%EC%9E%90%EB%A5%BC-%EC%9C%84%ED%95%9C-aws-%EC%9B%B9%EA%B5%AC%EC%B6%95-8-%EB%AC%B4%EB%A3%8C-%EB%8F%84%EB%A9%94%EC%9D%B8%EC%9C%BC%EB%A1%9C-route-53-%EB%93%B1%EB%A1%9D-%EB%B0%8F-elb/)  
 
 ## CDN
 
 [what is cdn by akamai](https://cdn.hosting.kr/cdn%EC%9D%B4%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80%EC%9A%94/)  
 
 
 ## GSLB(Global Server Load Balancer)  
 **healthcheck 와 Latency를 고려할 수 있는 스마트한 DNS**  
 
 
 
 ## Performance in Database  

#### Keys  
[keys](https://www.studytonight.com/dbms/database-key.php)  

#### 정규화  
[link](https://yaboong.github.io/database/2018/03/09/database-normalization-1/)  
[link](https://3months.tistory.com/193)  

[Why 1NF is needed](https://dba.stackexchange.com/questions/26933/first-normal-form-why-is-it-good-and-how-does-it-reduce-redundancy)  

[Join의 방식과 비싼 비용](https://www.sqlshack.com/introduction-to-nested-loop-joins-in-sql-server/)  

#### 1. Denormalization  
 * 이 역시 trade-off 다. 성능 vs redundacny 증가로 인해 ananomaly 발생 확률  
 
[geeks](https://www.geeksforgeeks.org/denormalization-in-databases/)  

#### 2. Indexing  

#### 3. SQL Tuning  

#### 4. Query-off  

#### 5. Sharding  


 
 
 
 
