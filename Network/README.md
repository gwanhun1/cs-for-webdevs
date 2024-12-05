# 네트워크: HTTP와 HTTPS

## 개요

HTTP(HyperText Transfer Protocol)와 HTTPS(HTTP Secure)는 웹에서 데이터를 전송하기 위한 핵심 프로토콜입니다.

## 주요 개념

### 1. HTTP

- **정의**:
  - 웹 브라우저와 서버 간 통신 프로토콜
  - 텍스트 기반의 통신 규약
- **특징**:
  - Stateless (무상태)
  - Request-Response 모델
  - 평문 통신

### 2. HTTPS

- **정의**:
  - HTTP에 보안 계층 추가
  - SSL/TLS 암호화 적용
- **보안 기능**:
  - 데이터 암호화
  - 서버 인증
  - 데이터 무결성 보장

### 3. HTTP 메서드

1. **주요 메서드**:
   - GET: 리소스 조회
   - POST: 리소스 생성
   - PUT: 리소스 수정
   - DELETE: 리소스 삭제
   - PATCH: 리소스 부분 수정

2. **특성**:
   - 멱등성
   - 안전성
   - 캐시 가능성

### 4. 상태 코드

- **2xx (성공)**:
  - 200 OK
  - 201 Created
  - 204 No Content
- **4xx (클라이언트 오류)**:
  - 400 Bad Request
  - 401 Unauthorized
  - 404 Not Found
- **5xx (서버 오류)**:
  - 500 Internal Server Error
  - 503 Service Unavailable

## 실제 예시

1. **웹 브라우저 통신**:
   ```http
   GET /index.html HTTP/1.1
   Host: www.example.com
   ```

2. **API 요청**:
   ```http
   POST /api/users HTTP/1.1
   Content-Type: application/json
   
   {
     "name": "John Doe",
     "email": "john@example.com"
   }
   ```

## 참고 자료

- HTTP: The Definitive Guide
- Web Security & HTTPS (Mozilla Developer Network)
- RFC 2616: HTTP/1.1 Specification
