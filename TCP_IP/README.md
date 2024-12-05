# TCP/IP 프로토콜

## 개요

TCP/IP는 인터넷에서 컴퓨터들이 서로 정보를 주고받는 데 사용하는 통신 규약으로, 데이터의 전송과 수신을 관리하는 핵심 프로토콜입니다.

## 주요 개념

### 1. TCP (Transmission Control Protocol)

- **특징**:
  - 연결 지향적 프로토콜
  - 신뢰성 있는 데이터 전송
  - 흐름 제어와 혼잡 제어
- **동작 방식**:
  - 3-way handshake
  - 순서 보장
  - 오류 검출 및 재전송

### 2. IP (Internet Protocol)

- **특징**:
  - 비연결성 프로토콜
  - Best Effort 전송
  - 패킷 단위 전송
- **주소 체계**:
  - IPv4 (32비트)
  - IPv6 (128비트)
  - 서브넷 마스크

### 3. TCP/IP 계층 구조

1. **응용 계층**:
   - HTTP, FTP, SMTP, DNS
   - 사용자 인터페이스 제공
   - 데이터 형식 정의

2. **전송 계층**:
   - TCP, UDP
   - 종단간 통신
   - 신뢰성과 흐름 제어

3. **인터넷 계층**:
   - IP
   - 라우팅
   - 패킷 전달

4. **네트워크 접근 계층**:
   - 이더넷, Wi-Fi
   - 물리적 주소 지정
   - 매체 접근 제어

### 4. 주요 프로토콜

- **HTTP/HTTPS**:
  - 웹 통신
  - 80/443 포트
- **FTP**:
  - 파일 전송
  - 20/21 포트
- **SMTP/POP3/IMAP**:
  - 이메일 서비스
  - 25/110/143 포트

## 실제 예시

1. **웹 브라우징**:
   ```
   브라우저 요청 → DNS 조회 → TCP 연결 → HTTP 요청 → 웹 페이지 수신
   ```

2. **이메일 전송**:
   ```
   메일 작성 → SMTP 서버 연결 → TCP 전송 → 수신자 메일서버 → POP3/IMAP 수신
   ```

## 참고 자료

- TCP/IP Illustrated
- Computer Networks (Andrew S. Tanenbaum)
- RFC 793: TCP Specification
