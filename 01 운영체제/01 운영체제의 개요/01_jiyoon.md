# 운영체제의 개요

*<쉽게 배우는 운영체제> pg 72~74*



## 연습문제

1. 운영체제
2. 임베디드 운영체제
3. 응용 프로그램
4. 새로운 기능 추가 어려움
5. 인터페이스
6. 일괄 작업 시스템 
7. 대화형 시스템
8. 시분할 시스템
9. 일괄 작업 시스템
10. 다중 사용자 시스템, 분산 시스템
11. 경성 실시간 시스템
12. 분산 시스템
13. P2P 시스템
14. 시스템 호출
15. 드라이버
16. 단일형 구조 커널
17. 마이크로 구조 커널
18. 가상머신



## 심화문제

1. 자원 관리, 자원 보호, 하드웨어 인터페이스 제공, 사용자 인터페이스 제공

2. 효율성, 안정성, 확장성, 편리성

3. CPU 집중 작업은 계산 작업 등 프로그램이 실행되는 동안 입출력이 불가능한 작업이다.

   입출력 집중 작업은 대부분의 작업 시간을 주변장치의 입출력에 사용하며 동영상 플레이어와 데이터베이스 같은 프로그램을 예로 들 수 있다.

4. 실시간 시스템은 특정 시스템에서 일정 시간 내에 작업이 처리되도록 보장하는 시스템이다. 경성 실시간 시스템과 연성 실시간 시스템으로 구분되는데, 경성 실시간 시스템은 지정한 응답 시간을 정확히 지키는 시스템으로 원자력이나 미사일을 제어하는 데 사용되고, 연성 실시간 시스템은 어느 정도의 융통성을 허용한 시스템이다.

5. 클라우드 컴퓨팅은 그리드 컴퓨팅과 SaaS를 합쳐놓은 형태로, 언제 어디서나 응용 프로그램과 데이터를 자유롭게 사용할 수 있는 컴퓨팅 환경이다. 기기를 통해 인터넷에 접속하고, 다영한 작업을 수행하며, 기기 간의 데이터 이동이 자유롭다.

6. API(Application Programming Interface)는 응용 프로그램이 자신과 연관된 프로그램을 만들 수 있도록 제공하는 인터페이스이다. 운영체제의 API를 시스템 호출이라고 할 수 있다.

   SDK(System Developer's Kit)는 프로그램 개발자를 위해 API, 매뉴얼, 코드 편집기, 에뮬레이터 같은 각종 개발용 응용 프로그램까지 하나로 묶어서 배포하는 개발 툴이다.

7. 단일형 구조 커널은 초창기의 운영체제 구조로, 모듈 구분 없이 하나로 구성된다. 모듈 간의 통신 비용이 줄어 효율적인 운영이 가능하지만, 버그나 오류 처리, 다양한 환경의 시스템에 적용이 어렵다.

8.  마이크로 구조 커널은 프로세스 관리, 메모리 관리, 프로세스 간 통신 관리 등 가장 기본적인 개념만 제공하는 커널이다. 