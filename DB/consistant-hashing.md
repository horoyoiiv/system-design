
# consistent hashing  
### [Consistent hasing이란?](https://www.youtube.com/watch?v=tHEyzVbl4bg)  

## 1. Consistent hashing이란  
* 가상의 **hash ring**을 구성한 후, **request id**를 해쉬한 값으로부터 clock-wise 방향으로  
돌면서 처음 만난 서버로 해당 request를 전달하는 것.  

## 2. 이를 통해  
* 이를 통해 '단지 모듈러 기반으로 load balancing을 했다면 노드 추가 삭제 시 상당 부분을 '마이그레이션''해야 했는데  
consistent hashing을 통해 노드의 추가 삭제 시 **영향을 받게 되는 노드의 수를 이에 인접한 노드 하나로 제한**할 수 있다.  
