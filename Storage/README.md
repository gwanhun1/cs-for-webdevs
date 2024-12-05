# 보조기억장치

## 개요

보조기억장치는 컴퓨터의 주기억장치(RAM)와 달리 전원이 꺼져도 데이터가 유지되는 비휘발성 저장장치입니다.

## 주요 개념

### 1. HDD (Hard Disk Drive)

- **구조**: 
  - 플래터(자기 디스크)
  - 헤드(읽기/쓰기)
  - 스핀들 모터
- **특징**:
  - 기계적 동작으로 인한 상대적 저속
  - 대용량 저장 가능
  - 저렴한 가격

### 2. SSD (Solid State Drive)

- **구조**:
  - NAND 플래시 메모리
  - 컨트롤러
  - DRAM 캐시
- **특징**:
  - 빠른 읽기/쓰기 속도
  - 내구성 향상
  - 소음 없음
  - HDD 대비 고가

### 3. 저장 방식

1. **HDD 저장 방식**:
   - 자기 디스크에 데이터를 자기적으로 기록
   - 섹터 단위로 데이터 저장
   - 디스크 조각모음으로 성능 최적화

2. **SSD 저장 방식**:
   - 전기적 신호로 데이터 저장
   - 페이지/블록 단위로 데이터 관리
   - TRIM 명령어로 성능 유지

### 4. 성능 특성

- **접근 시간**:
  - HDD: ~10ms
  - SSD: ~0.1ms
- **전송 속도**:
  - HDD: ~150MB/s
  - SSD: ~500MB/s~3000MB/s
- **수명**:
  - HDD: 기계적 마모
  - SSD: P/E 사이클 제한

## 실제 예시

1. **운영체제 설치**:
   - SSD에 설치 시 빠른 부팅과 응답 속도
   - HDD는 대용량 데이터 저장용으로 활용

2. **데이터베이스 서버**:
   - 로그 파일: SSD (빠른 쓰기 속도 필요)
   - 백업 데이터: HDD (대용량 저장 필요)

## 참고 자료

- Computer Architecture: A Quantitative Approach
- Storage Systems: Organization, Performance, Coding, Reliability
- Flash Memory Integration: Performance and Energy Issues
