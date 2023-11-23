# 개발환경, spring-boot-data-elasticsearch

Date: 2023-09-07

## Repository 소개

- [study-share](https://github.com/spectra-study/study-share)
  - share-docker
    - command
      - $ docker-compose up -d
      - $ docker-compose down -v
  - share domain
    - domain
      - NameValue.java
      - NameValueList.java
    - util
      - JsonSerializable.java
      - SamplePrinter.java

- [study-elasticsearch](https://github.com/spectra-study/study-elasticsearch)
  - user application
    - domain
    - store
    - service
    - controller
    - elasticsearch repository query logging
    - testcase

## 개발환경

- https://github.com/settings/tokens 생성

## Spring boot data elasticsearch

- Docs
  - https://docs.spring.io/spring-data/elasticsearch/docs/4.4.15/reference/html/

- [ElasticsearchRepository](https://docs.spring.io/spring-data/elasticsearch/docs/current/api/org/springframework/data/elasticsearch/repository/ElasticsearchRepository.html)
  - [Mapping Annotation](https://docs.spring.io/spring-data/elasticsearch/docs/4.4.15/reference/html/#elasticsearch.mapping.meta-model.annotations)
  - [Query Method Keyword](https://docs.spring.io/spring-data/elasticsearch/docs/4.4.15/reference/html/#appendix.query.method.predicate)

- Testcase
  - [UserRepositoryTest (findAllByNameContains)](https://github.com/spectra-study/study-elasticsearch/blob/main/user/src/test/java/com/study/es/user/store/elasticsearch/repository/UserRepositoryTest.java)

- [Query Logging (request/response)](https://docs.spring.io/spring-data/elasticsearch/docs/4.4.15/reference/html/#elasticsearch.clients.logging)

  - ex) findAll()

    ```json
    {
      "from": 0,
      "size": 0,
      "query": {
        "wrapper": {
          "query": "eyJtYXRjaF9hbGwiOnt9fQ=="
        }
      },
      "version": true,
      "explain": false,
      "track_total_hits": 2147483647
    }
    ```

  - [Base64 Decode](https://www.base64decode.org/)

    - eyJtYXRjaF9hbGwiOnt9fQ==

    - ```json
      {"match_all":{}}
      ```

## Etc

- http://172.16.100.51:9200/
- http://172.16.100.51:9200/_cat/indices
- http://172.16.100.51:9200/_cat/shards
- http://172.16.100.51:9200/attic_btalk_ticket/

## Next

- 개별 repository 소개 및 코드리뷰
- Application logging in elasticsearch
- Elasticsearch client
