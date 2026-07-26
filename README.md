# 안성훈 · Backend Engineer

Java와 Spring을 중심으로 데이터 정합성과 실패 복구를 고민하는 백엔드
개발자입니다. 기능 구현에서 멈추지 않고 쿼리 실행 계획, 동시 요청,
캐시 복구 기준과 테스트 결과까지 확인합니다. Rust를 학습하며 기존
오픈소스 코드베이스의 동작 차이를 수정하고 upstream review를 경험하고
있습니다.

## Featured Work

### 🐾 [PawShop](https://github.com/shAn-kor/PawShop) — 애견용품 커머스 백엔드

사료·간식·장난감·산책용품을 브랜드별로 탐색하고 주문하는 흐름에서
조회 성능, 재고 정합성, 랭킹 복구 문제를 다뤘습니다.

- 상품 30만 건과 대표 쿼리 20개를 비교해 `brand + likes DESC` 조회를
  72.7ms에서 10.6ms로 개선했습니다.
- 재고 10개에 20개 요청을 동시에 보내 성공 10건·품절 10건·최종 재고
  0을 검증했습니다.
- Kafka 이벤트를 DB 기준 데이터로 적재하고 Redis top 100을 조회용으로
  동기화해 랭킹 복구 기준을 분리했습니다.

[검색 인덱스 실험](https://github.com/shAn-kor/PawShop/blob/shAn-kor/docs/adr/2026-03-13-product-search-index-benchmark-adr.md)
· [동시성 결정](https://github.com/shAn-kor/PawShop/blob/shAn-kor/docs/adr/2026-03-05-stock-deduction-concurrency-adr.md)
· [랭킹 배치 비교](https://github.com/shAn-kor/PawShop/blob/shAn-kor/docs/performance/batch-ranking-aggregation-comparison-20260416.md)

### 🦀 [RustPython](https://github.com/RustPython/RustPython) — Open Source Contribution

`TextIOWrapper._CHUNK_SIZE` setter의 타입 변환, 범위 검사, 오류 동작을
CPython과 맞추고 회귀 테스트를 추가했습니다. 리뷰 피드백을 반영한 변경은
[PR #8265](https://github.com/RustPython/RustPython/pull/8265)로 병합됐습니다.

## Other Open Source

- [DBeaver PR #40078](https://github.com/dbeaver/dbeaver/pull/40078) — PostgreSQL
  Row-Level Security 정책을 테이블 DDL에 표시하도록 기능을 추가했습니다.

## Tech

`Java` · `Spring Boot` · `Rust` · `MySQL` · `Redis` · `Kafka` ·
`Testcontainers`

## Contact

[kjn0406@gmail.com](mailto:kjn0406@gmail.com)
