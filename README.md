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

 
 ## GSLB(Global Server Load Balancer)  
 **healthcheck 와 Latency를 고려할 수 있는 스마트한 DNS**  

 #### GSLB는 Authoritative Domain Server로서 동작  
 [1. What is authoritative server?](https://www.cloudns.net/blog/authoritative-dns-server/)  
 [2. *GSLB is what?](https://www.a10networks.com/blog/global-server-load-balancing/)  
  Local DNS 서버가 Root 서버, TLD 서버로부터 가져온 Authoritative 서버가 종래의 DNS 서버가 아닌, GSLB DNS 서버 주소를 가져옴.  
  Local DNS 서버는 GSLB DNS서버에 질의하여, 최적의 서버 IP를 가져온다.  
  
  [3. How it works](https://cloud.kt.com/portal/ktcloudportal.epc.productintro.gslb.html)  
 ㅈ
 

 # CDN
 
 [what is cdn by akamai](https://cdn.hosting.kr/cdn%EC%9D%B4%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80%EC%9A%94/)  
 

 # LB  
 
 [L4 vs L7 Load Balancer](https://freeloadbalancer.com/load-balancing-layer-4-and-layer-7/)  
 
 #### 1. 이점  
 
 1. ssl에 대한 복호화 및 암호화를 LB에서 수행하여, upstream server의 암호화 부하를 줄일 수 있다.  
 2. Scale-out을 통한 throughput 증가  
 
 #### 2. 단점  
 
 1. cluster 구성의 복잡도 증가  
 2. LB의 리소스가 부족할 경우 LB 자체가 bottleneck이 될 수 있다.  
 
 #### 3. Consistent Hashing  
 * [consistent hasing이란?](/DB/consistant-hashing.md)  
 * 가상의 **hash ring**을 구성한 후 **request id**의 hash값을 **clock-wise**하게 탐색하며 처음 만난 서버로 요청을 전송.  
 * 이를 통해, 노드의 추가 삭제 시 **인접한 노드에만 영향**이 가기에, 변화를 최소화할 수 있다.  
 
 # Forward Proxy vs Reverse Proxy  
 #### [설명](https://www.lesstif.com/system-admin/forward-proxy-reverse-proxy-21430345.html)  
 
 ## 1. Forward Proxy  
 * Client와 인접한 곳에 위치하여, **클라이언트의 요청**을 대신 수행하는 서버.  
 * 또한, 요청에 대한 결과를 **Caching**하여, 다음의 동일한 요청에 대해서 그 cache된 응답을 돌려줄 수 있다.  
 
 ## 2. Reverse Proxy  
 * backend 서버 앞단에 배치된다.  
 #### 2.1. 들어오는 요청을 [upstream server](https://stackoverflow.com/questions/5877929/what-does-upstream-mean-in-nginx)로 포워딩해준다. 
 #### 2.2. ssl 암,복호화 수행 뿐만 아니라 static contents나 response를 caching하는 기능수행.  
 
 
 ## LB vs Reverse Proxy  
 
 1. LB는 여러 서버에 부하를 분산한다는 개념이 강하다.  
 2. Rerver Proxy는 서버가 하나라도 사용할 수 있다.  
 3. blacklist ip, ssl, caching 기능 등을 위하여  
 
 
 
 ## Performance in Database  

#### Keys  
[keys](https://www.studytonight.com/dbms/database-key.php)  

#### 정규화  
[link](https://yaboong.github.io/database/2018/03/09/database-normalization-1/)  
[link](https://3months.tistory.com/193)  

[Why 1NF is needed](https://dba.stackexchange.com/questions/26933/first-normal-form-why-is-it-good-and-how-does-it-reduce-redundancy)  

[Join의 방식과 비싼 비용](https://www.sqlshack.com/introduction-to-nested-loop-joins-in-sql-server/)  

#### Join method  
 * **It is always good to know what's happening behind**  
 [What kind of join method ](/DB/join.md)  
 
 
#### 1. Denormalization  
 * 이 역시 trade-off 다. 성능 vs redundacny 증가로 인해 ananomaly 발생 확률  
 
[geeks](https://www.geeksforgeeks.org/denormalization-in-databases/)  

#### 2. Indexing  
[SELECT query 향상을 위한 index라는 추가 자료구조 사용](/DB/indexing.md)  


#### 3. SQL Tuning  

#### 4. Query-off  

#### 5. Sharding  


 
 
 
 
