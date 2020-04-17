
# Join  

  * DBMS의 컴포넌트 중 **Query Optimizer**는 사용자가 요청한 **SQL query**를 분석하여, 최적의 **Execution Plan**을 선택한다.  
  * join 연산 시 **nested loop join**, **merge join**, **hash join** 을 선택.  
  

## 1. Nested loop join  

[What is nested loop join?](https://www.sqlshack.com/introduction-to-nested-loop-joins-in-sql-server/)  

[*그루비](http://www.gurubee.net/lecture/2388)  

## 2. Sort merge join  
 * join할 행을 찾은 후 정렬을 수행하고, 정렬된 두 결과를 바탕으로 join을 수행  
 
## 3. Hash join  
 * Outer table의 행의 값을 hashing하여, hash table에 저장하고, Inner table의 행의 값을 hashing하여 그 key값의 bucket에 저장된 Outer 행들과 join함.  
 
