# 코드리뷰, Elasticsearch(client, operations, repository) CRUD, Query, Application logging

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fspectra-study%2Fstudy-log&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

Date: 2023-09-13

## 코드 리뷰

- 검색 조건 5개 이상으로 도메인 모델링
- Entity, Value Object 구별 및 차이점
  - 객체를 식별할 수 있는 아이디 유무

- 객체 기본 생성자
  - 데이터 변환 과정에서 reflection

- setValues 사용이유
  - 객체 속성에 대해 단일 변경 지점 및 변경가능한 범위 정의

- sdo, domain, doc 상관 관계 및 변환 과정
  - sdo <-> domain <-> doc


## Elasticsearch

- [Elastic search client](https://docs.spring.io/spring-data/elasticsearch/docs/current/reference/html/#elasticsearch.clients)
  - Elastic search lib 활용
- [Elastic search operations](https://docs.spring.io/spring-data/elasticsearch/docs/current/reference/html/#elasticsearch.operations)
  - Spring Data Elasticsearch operations 활용
    - [CriteriaQuery](https://docs.spring.io/spring-data/elasticsearch/docs/current/reference/html/#elasticsearch.operations.criteriaquery)
    - [StringQuery](https://docs.spring.io/spring-data/elasticsearch/docs/current/reference/html/#elasticsearch.operations.stringquery)
    - [NativeQuery](https://docs.spring.io/spring-data/elasticsearch/docs/current/reference/html/#elasticsearch.operations.nativequery)
- [Elastic search respository](https://docs.spring.io/spring-data/elasticsearch/docs/current/reference/html/#elasticsearch.repositories)
  - Spring Data Elasticsearch repository 활용 
    - [Query methods](https://docs.spring.io/spring-data/elasticsearch/docs/current/reference/html/#elasticsearch.query-methods)
    - [@Query Annotation](https://docs.spring.io/spring-data/elasticsearch/docs/current/reference/html/#elasticsearch.query-methods.at-query)

## Application logging

- [logback-elasticsearch-appender](https://github.com/internetitem/logback-elasticsearch-appender) 적용
  - [application.yml](https://github.com/spectra-study/study-elasticsearch/blob/main/user/src/main/resources/application.yml)
  - [logback-spring.xml](https://github.com/spectra-study/study-elasticsearch/blob/main/user/src/main/resources/logback/logback-spring.xml)

## Etc

- [java rest high query builders](https://www.elastic.co/guide/en/elasticsearch/client/java-rest/current/java-rest-high-query-builders.html)

## Next

- 코드리뷰
- auditing, bulk, refresh, 기타 등등
