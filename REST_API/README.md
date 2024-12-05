# REST API

## 📌 REST API란?

REST(Representational State Transfer)는 웹 서비스를 위한 소프트웨어 아키텍처 스타일입니다. REST API는 이 REST 아키텍처를 따르는 API를 의미합니다.

## 🔍 주요 개념

### 1. REST 구성 요소

- **자원(Resource)**: URI를 통해 식별
- **행위(Verb)**: HTTP Method를 통해 표현
- **표현(Representation)**: 자원의 특정 시점의 상태를 표현

### 2. REST 특징 (제약조건)

1. **Client-Server 구조**
   - 클라이언트와 서버가 독립적으로 진화할 수 있음
   - 서버의 확장성이 향상됨

2. **Stateless (무상태성)**
   - 각 요청은 독립적이며 이전 요청과 무관
   - 서버는 클라이언트의 상태를 저장하지 않음

3. **Cacheable (캐시 가능)**
   - HTTP의 캐싱 기능 활용
   - 응답은 캐시 가능 여부를 명시해야 함

4. **Uniform Interface (인터페이스 일관성)**
   - 리소스 식별
   - 표현을 통한 리소스 조작
   - 자기 서술적 메시지
   - HATEOAS (Hypermedia as the Engine of Application State)

5. **Layered System (계층화)**
   - 클라이언트는 서버에 직접 연결되었는지 중간 서버를 통해 연결되었는지 알 수 없음
   - 보안, 로드 밸런싱, 캐시 등의 계층을 추가할 수 있음

### 3. HTTP Methods

- **GET**: 리소스 조회
- **POST**: 리소스 생성
- **PUT**: 리소스 전체 수정
- **PATCH**: 리소스 부분 수정
- **DELETE**: 리소스 삭제

### 4. REST API 설계 규칙

1. **URI는 리소스를 표현해야 함**
   ```
   Good: /users
   Bad: /getUsers
   ```

2. **행위는 HTTP Method로 표현**
   ```
   GET /users (사용자 목록 조회)
   POST /users (새로운 사용자 생성)
   ```

3. **URI는 복수형 명사 사용**
   ```
   Good: /products
   Bad: /product
   ```

4. **계층 관계는 슬래시(/)로 표현**
   ```
   /users/123/orders
   ```

## 💡 RESTful API의 장단점

### 장점
- HTTP 프로토콜의 인프라를 그대로 사용
- 별도의 인프라 구축이 필요 없음
- HTTP 클라이언트와 서버를 사용하는 모든 플랫폼에서 사용 가능
- 서버와 클라이언트의 역할을 명확하게 분리

### 단점
- HTTP Method의 제한
- 표준이 존재하지 않음
- 완벽한 REST를 구현하기 어려움

## 🌐 실제 사용 예시

```http
# 사용자 목록 조회
GET /api/users

# 특정 사용자 조회
GET /api/users/123

# 새로운 사용자 생성
POST /api/users
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example.com"
}

# 사용자 정보 수정
PUT /api/users/123
Content-Type: application/json

{
  "name": "John Smith",
  "email": "john.smith@example.com"
}

# 사용자 삭제
DELETE /api/users/123
```
