## @Transactional

#### 1. 트래잭션 성질

##### 원자성

- 한 트랜잭션 내에서 실행한 작업들은 하나로 간주한다. 즉, 모두 성공 또는 모두 실패.

  

##### 일관성

- 트랜잭션은 일관성 있는 데이타베이스 상태를 유지한다.

  

##### 격리성

- 동시에 실행되는 트랜잭션들이 서로 영향을 미치지 않도록 격리해야한다.



##### 지속성

- 트랜잭션을 성공적으로 마치면 결과가 항상 저장되어야 한다.



#### 2. 스프링에서 트랜잭션 처리 방법



##### 스프링에서는 트랜잭션 처리를 지원하는데 그중 어노테이션 방식으로 @Transactional을 선언하여 사용하는 방법이 일반적이며, 선언적 트랜잭션이라 부른다.

##### 클래스, 메서드 위에 @Transactional 이 추가되면, 이 클래스에 트랜잭션 기능이 적용된 프록시 객체가 생성된다.

##### 이 프록시 객체는 @Transactional 이 포함된 메소드가 호출 될 경우, PlatformTransactionManger를 사용하여 트랜잭션을 시작하고, 정상 여부에 따라 Commit 또는 Rollback한다.





#### EX)

**@Transactional**

**public** boolean insertUser(**User** user){

 ...

}



