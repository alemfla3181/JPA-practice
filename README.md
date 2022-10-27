# JPA-practice

## JPA란 무엇인가?
- JPA (Java Persisitence API)는 자바 진영의 ORM 기술 표준

## JPA 소개
- EJB 3.0에서 하이버네이트를 기반으로 새로운 자바 ORM 기술 표준이 만들어졌는데 이것이 바로 JPA
- JPA는 자바 ORM 기술에 대한 API 표준 명세
- 인터페이스를 모아둔 것, 따라서 JPA를 구현한 ORM 프레임워크를 선택해야함

## 왜 JPA를 사용해야 하는가?
### 생산성
- JPA를 자바 컬렉션에 객체를 저장하듯 JPA에게 저장할 객체를 전달
- INSERT SQL을 작성하고 JDBC API 사용하는 지루하고 반복적인 일을 JPA가 대신 처리해줌
- CREATE TABLE같은 DDL문 자동 생성
- 데이터베이스 설계 중심의 패러다임을 객체 설계 중심으로 역전

### 유지보수
- 엔티티에 필드 추가시 등록, 수정, 조회 관련 코드 모두 변경
- JPA를 사용하면 이런 과정을 JPA가 대신 처리
- 개발자가 작성해야 할 SQL과 JDBC API 코드를 JPA가 대신 처리해줌으로 유지보수해야 하는 코드 수가 줄어듬

### 패러다임 불일치 해결
- 상속, 연관관계, 객체 그래프 탐색, 비교하기 같은 패러다임 불일치 해결
- 성능

JDBC API를 사용해서 작성하면 조회할때 마다 SELECT SQL을 사용해서 DB와 두 번 통신했을 것
JPA를 사용하면 회원을 조회하는 SELECT SQL을 한 번만 데이터베이스에 전달하고 두 번쨰는 조회한 회원 객체를 재사용함
- 다양한 성능 최적화 기회 제공
- 어플리케이션과 데이터베이스 사이에 존재함으로 여러 최적화 시도 가능

### 데이터 접근 추상화와 벤더 독립성
- 데이터베이스 기술에 종속되지 않도록 함
- 데이타베이스를 변경하면 JPA에게 다른 데이터베이스를 사용한다고 알려주면 됨

### 표준
- JPA는 자바 진영의 ORM 기술 표준이다. 표준을 사용하면 다른 구현 기술로 손쉽게 변경 가능
