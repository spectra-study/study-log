# 코드리뷰, Auditing, Bulk, Refresh, Analyze

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fspectra-study%2Fstudy-log&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

Date: 2023-09-20

## 코드 리뷰

- 패키지 구조 및 이름 역할
- [Sdo <-> Domain <-> Doc] 변환 과정 및 이유
- Collection Document 


## Auditing

- [Elasticsearch Auditing](https://docs.spring.io/spring-data/elasticsearch/docs/4.4.15/reference/html/#elasticsearch.auditing)

## Bulk

- [multi save VS bulk save](https://github.com/spectra-study/study-elasticsearch/blob/main/user/src/test/java/com/study/es/user/customer/store/elasticsearch/repository/CustomerRepositoryTest.java)

## Refresh

- Refresh Intervall: default to “1s”
- [Refresh api](https://www.elastic.co/guide/en/elasticsearch/reference/7.17/indices-refresh.html)

## 형태소 분석기

- docker

  - nori 설치

  ```bash
  bin/elasticsearch-plugin install analysis-nori
  ```

  - docker 재기동

  ```bash
  docker-compose stop
  docker-compose up
  ```

  - 설치 확인

  ```
  curl -X GET "http://localhost:9200/_cat/plugins?v"
  ```

  - [index setting](https://docs.spring.io/spring-data/elasticsearch/docs/4.4.15/reference/html/#elasticsearc.misc.index.settings)
  - [analyze](https://www.elastic.co/guide/en/elasticsearch/reference/7.17/indices-analyze.html#explain-analyze-api)
  - [한글 형태소 품사](http://kkma.snu.ac.kr/documents/?doc=postag)

## Next

- 마무리
