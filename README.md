# Subscription Backend Platform
기업이 쉽게 구독 서비스를 구축할 수 있도록 지원하는 MSA 기반 백엔드 플랫폼
## Overview
- 목표: 기업이 구독 서비스 구축 시 복잡한 결제/구독/알림 로직을 직접 구현하지 않아도 되도록 지원
- 주요 기능:
  - 기업별 구독 상품 관리
  - 사용자 결제 처리
  - 구독 상태 관리 (Pending, Active, Cancelled)
  - 알림 서비스 (결제 완료, 구독 시작/만료)
- 기술 스택: Java, Spring Boot, PostgreSQL, Kafka(RabbitMQ),  Kubernetes
## Services
### User Service
- 기업 및 최종 사용자 계정 관리
- 인증/권한 관리

### Subscription Service
- 구독 상품 생성/갱신/취소
- 구독 상태 관리

### Payment Service
- 결제 처리 및 이벤트 발행
- PG Sandbox 연동

### Notification Service
- 결제 완료, 구독 시작/만료 알림
- 이메일/푸시/Webhook 지원
