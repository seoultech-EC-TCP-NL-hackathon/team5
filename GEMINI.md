# GEMINI.md
_AI Development Guide for Team5 (SeoulTech Hackathon)_

---

## 📌 프로젝트 배경
- 프로젝트명: **PriceMate**
- 해커톤: **SeoulTech EC & TCP & NL Hackathon**
- 팀명: **Team5**
- 서비스 개요:  
  여러 쇼핑몰(쿠팡, 네이버스토어, 옥션 등)의 상품 가격을 수집하고,  
  AI가 **최저가**를 추천해주는 웹 서비스.
- 주요 기능:
    - 상품 검색, 카테고리, 필터링
    - 최저가 추천 (AI 로직 기반)
    - 장바구니, 결제, 배송 조회
    - 로그인 및 회원 관리

---

## 🎯 코딩 규약 & 스타일 가이드

### Backend (Spring Boot, Java)
- **언어 버전**: Java 17
- **프레임워크**: Spring Boot 3.x
- **코드 스타일**:
    - 변수명: `camelCase`
    - 클래스명: `PascalCase`
    - 상수: `UPPER_SNAKE_CASE`
- **패키지 구조 (예시)**:
  com.team5.backend
  ├─ controller
  ├─ service
  ├─ repository
  ├─ model (Entity, DTO)
  └─ config

markdown
코드 복사
- **ORM**: Spring Data JPA
- **API 규칙**: RESTful
- **예외 처리**: `@RestControllerAdvice`
- **로그**: `Slf4j` (Lombok)

---

## 🔧 자주 사용하는 라이브러리

### Backend
- Spring Web
- Spring Data JPA
- MySQL Driver
- Lombok
- Spring Security (JWT 인증)

---

## 🧠 비즈니스 로직 (간단 흐름)
1. **사용자 로그인**
- JWT 토큰 기반 인증
2. **상품 탐색**
- 검색/카테고리 선택 → API 호출
- AI/크롤링 모듈 → 가격 비교 + 최저가 반환
3. **장바구니 & 결제**
- 장바구니 담기 → 모의 결제 API
4. **배송 조회**
- Mock 데이터로 응답

---

## 📂 모노레포 구조
seoultech-hackathon-team5/
├─ backend/ # Spring Boot
├─ frontend/ # React
├─ docs/ # ERD, API 명세, 발표자료
└─ GEMINI.md # AI 가이드 문서

## branch 구조
