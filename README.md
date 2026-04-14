# Accommodation API

Spring Boot 기반 숙박 예약 플랫폼 REST API 서버

## 기술 스택

**Backend**
- Java 21
- Spring Boot 3.x
- Spring Data JPA / QueryDSL
- Spring Security (JWT)

**Database**
- MySQL
- Redis

**Infra**
- Docker / docker-compose
- GitHub Actions

## 주요 기능
- 숙박 상품 등록 / 조회 / 검색
- 예약 생성 / 취소 / 변경
- JWT 기반 회원 인증 / 인가
- Redis 기반 재고 동시성 제어
- 페이징 / 필터링 / 정렬

## 핵심 설계 포인트
- 동시 예약 요청 처리 (Redis 분산락)
- 대용량 상품 검색 최적화 (인덱스 튜닝)
- 레거시 MyBatis → JPA 마이그레이션 구조 적용

## 프로젝트 구조
\```
accommodation-api
├── domain         # 도메인 모델 (숙박, 예약, 회원)
├── application    # 서비스 레이어
├── infrastructure # DB, Redis, 외부 API 연동
└── presentation   # REST 컨트롤러
\```
