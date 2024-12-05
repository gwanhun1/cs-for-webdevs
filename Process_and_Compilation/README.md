# 프로세스와 컴파일 과정

## 개요

프로그램이 실행 가능한 프로세스로 변환되고 메모리에서 실행되는 과정을 이해하는 것은 소프트웨어 개발의 기초입니다.

## 주요 개념

### 1. 프로세스

- **정의**:
  - 실행 중인 프로그램의 인스턴스
  - 독립된 메모리 공간
  - 시스템 자원 할당 단위
- **구성 요소**:
  - 코드 영역
  - 데이터 영역
  - 스택 영역
  - 힙 영역

### 2. 컴파일 과정

1. **전처리(Preprocessing)**:
   - 매크로 치환
   - 헤더 파일 포함
   - 주석 제거

2. **컴파일(Compilation)**:
   - 어셈블리어로 변환
   - 문법 검사
   - 최적화

3. **어셈블(Assembly)**:
   - 기계어로 변환
   - 오브젝트 파일 생성

4. **링킹(Linking)**:
   - 라이브러리 연결
   - 실행 파일 생성

### 3. 프로세스 상태

- **생성(Created)**:
  - 프로세스 생성
  - PCB 할당
- **실행(Running)**:
  - CPU 점유
  - 명령어 실행
- **대기(Waiting)**:
  - I/O 작업 대기
  - 이벤트 대기
- **종료(Terminated)**:
  - 실행 완료
  - 자원 반환

### 4. 프로세스 관리

- **스케줄링**:
  - CPU 할당
  - 우선순위 관리
- **동기화**:
  - 임계 영역 관리
  - 상호 배제
- **통신**:
  - IPC
  - 파이프, 소켓

## 실제 예시

1. **C 프로그램 컴파일**:
   ```bash
   gcc -E source.c -o source.i    # 전처리
   gcc -S source.i -o source.s    # 컴파일
   gcc -c source.s -o source.o    # 어셈블
   gcc source.o -o program        # 링킹
   ```

2. **프로세스 생성**:
   ```c
   pid_t pid = fork();           // 프로세스 복제
   if (pid == 0) {
       // 자식 프로세스
   } else {
       // 부모 프로세스
   }
   ```

## 참고 자료

- Modern Operating Systems
- Compilers: Principles, Techniques, and Tools
- Advanced Programming in the UNIX Environment
