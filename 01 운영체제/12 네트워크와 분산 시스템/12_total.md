# 12 네트워크와 분산 시스템

*<쉽게 배우는 운영체제> pg 589~590*



## 연습문제

1. 네트워크로 연결된 모든 컴퓨터의 프로세서가 하나의 메모리를 공유하는 네트워크 구성 방식은 무엇인가?

   ```
   강결합 시스템
   ```

2. 서로 다른 기기 간에 통신을 하기 위해 정한 약속을 무엇이라 하는가?

   ```
   프로토콜
   ```

3. 가까운 거리를 연결하는 네트워크를 무엇이라 하는가?

   ```
   LAN(Local Area Network)
   ```

4. LAN의 구조를 뜻하는 영어 단어는 무엇인가?

   ```
   토폴로지(Topology)
   ```

5. 버스 토폴로지에 데이터 전송을 위한 프로토콜로 CSMA/CD를 사용하는 LAN은 무엇인가?

   ```
   이더넷(Ethernet)
   ```

6. 완전한 분산 시스템은 구성하는 데 문제가 많아 작업을 요청하는 컴퓨터와 이를 처리하는 컴퓨터의 이중 구조로 나눈다. 이러한 분산 시스템을 무엇이라 하는가? 

   ```
   클라이언트/서버 시스템
   ```

7. 클라이언트/서버 시스템의 서버 과부화 문제를 해결한 시스템으로, 데이터 전송 시 서버를 거치지 않고 사용자 간에 직접 이루어지는 시스템은 무엇인가?

   ```
   P2P 시스템
   ```

8. 평상시에 대기 상태를 유지하다가 가동 시스템의 하드웨어 또는 네트워크 장비에 장애가 발생하면 가동 시스템의 자원을 백업 시스템으로 이전하여 서비스가 중단되지 않도록 하는 고가용성 시스템은 무엇인가?

   ```
   상시 대기
   ```

9. 2개의 시스템이 각각의 고유 서비스를 수행하다가 한쪽 시스템에 장애가 발생하면 상대 시스템으로 작업을 이동하는 고가용성 시스템은 무엇인가?

   ```
   상호 인계
   ```




## 심화문제

1. 1~5세대의 무선 전화망에 대해 설명하시오.

   ```
   - 1세대 무선 전화망 : 아날로그 신호만 전송
   - 2세대 무선 전화망 : 디지털 신호를 전송하면서 진화
   	- 같은 통신 대역폭에 더 많은 사용자를 수용할 수 있어 효율성이 좋음
   - 3세대 무선 전화망 : 기존의 전화 기능(음성망)에 데이터 통신(데이터망) 기능을 추가(휴대전화로도 인터넷 사용)
   - 4세대 무선 전화망 : 데이터 전송 속도를 높임,
   - 데이터 사용량이 급격하게 증가하고 음성 통화가 줄어들어, 음성망은 그대로 두고 데이터 통신을 고속으로 업그레이드
   - 고속 데이터 통신 + 음성 통화
   - LTE(Long Term Evolution) : 3.9세대 통신 (4G 데이터 통신 + 3G 음성 통화)
   - 5세대 무선 전화망 : 초고속 무선통신이 가능
   ```

2. 네트워크 구성 방식인 강결합 시스템과 약결합 시스템을 비교하여 설명하시오.

   ```
   - 강결합 시스템 : 네트워크로 연결된 모든 컴퓨터의 프로세서가 하나의 메모리를 공유하는 방식, 프로세서들이 하나의 공유 메모리를 사용하여 통신하기 때문에 공유 메모리를 서로 사용하려고 경쟁하며, 이러한 경쟁을 결합 교환 방법으로 해결
   	- 장점 : 약결합 시스템에 비해 속도가 빠르다
   	- 단점 : 하나의 시스템에 문제가 생기면 다른 시스템에도 영향을 미침
   - 약결합 시스템 : 둘 이상의 독립된 시스템을 연결한 것, 오늘날의 네트워크는 이 방식으로 이루어져 있다. 약결합 시스템은 독립적으로 운영되다가 필요할 때 통신선을 이용하여 메시지 전달이나 원격 프로시저 호출로 통신한다.
   	- 장점 : 컴퓨터들이 서로 독립적으로 작동하기 때문에 하나의 시스템에 장애가 발생해도 다른 시스템에 영향을 미치지 않는다.
   	- 단점 : 통신 오버헤드가 있기 때문에 강결합 시스템보다 느리다.
   ```
   
3. 클라이언트/서버 시스템의 구조와 미들웨어의 역할을 설명하시오.

   ```
   - 클라이언트/서버 시스템 : 모든 컴퓨터가 동일한 지위를 갖지 않고, 작업을 요청하는 클라이언트와 요청받은 작업을 처리하는 서버의 이중 구조로 되어 있음
   - 미들웨어 : 클라이언트/서버 시스템을 연결하여 데이터를 주고받을 수 있도록 중간에서 매개 역할을 하는 소프트웨어, 클라이언트/서버 시스템에서 필요에 따라 서버를 증설하면 서로 다른 기종의 서버를 운영해야 하는 경우도 있고, 서로 다른 데이터베이스를 연결해야 하는 경우도 있는데 이때 미들웨어로 서로 다른 기종의 서버를 묶어 사용하면 표준화된 인터페이스를 통해 일관된 작업 가능
   ```
   
4. P2P 시스템의 구조를 설명하시오.

   ```
   - 분산 시스템을 기본으로 하면서도 서버의 부하를 줄이고 몇 개의 컴퓨터가 고장나더라도 서비스를 지속할 수 있는 시스템
   - 비구조적 P2P 시스템 : 전체 노드에 대한 정보는 서버가 가지고 있고, 실제 데이터 전송은 일대일로 연결된 말단 노드를 통해 이루어지는 경우
   	- 데이터를 보내는 쪽이 프로그램을 중단하면 받는 쪽에서 데이터를 내려받는 데 어려움이 있음
   	- 전체 네트워크에 대한 정보를 모든 노드에 저장하여 관리하거나 하나의 노드에 집중 저장하여 관리
   - 구조적 P2P 시스템 : 각 노드가 전체 네트워크 정보가 아닌 부분적인 네트워크 정보를 유지함으로써 비구조적 P2P 시스템의 단점을 보완
   	- 특정 파일의 소유자 정보를 여러 노드가 공유함으로써, 시스템의 한 노드가 사라지더라도 데이터 공유가 지속적으로 이루어짐
   ```
   
5. 고가용성의 의미와 고가용성을 보장하기 위해 시스템을 구성하는 유형을 설명하시오.

   ```
   - 고가용성 : 업무 또는 서비스 중단을 최소화하기 위해 이중화 작업을 하는 것으로 작게는 운영체제의 디스크 미러링부터 크게는 시스템 자체를 이중화하는 것을 포함하는 개념
   - 상시 대기 : 가장 단순하면서도 많이 사용되는 고가용성 구성의 유형, 가동 시스템과 백업 시스템으로 구성됨, 평상시에 대기 상태를 유지하다가 가동 시스템의 하드웨어 또는 네트워크 장비에 장애가 발생하면 가동 시스템의 자원을 백업 시스템으로 이전하여 서비스가 중단되지 않게 함
   	- 데이터의 일관성이 보장됨
   - 상호 인계 : 2개의 시스템이 각각의 고유 서비스를 수행하다가 한쪽 시스템에 장애가 발생하면 상대 시스템으로 작업을 이동하여 동시에 2개의 업무를 수행함, 각 시스템은 장애 발생으로 인한 업무 이전에 대비하여 2개의 업무를 동시에 서비스할 수 있는 시스템 용량을 갖추고 있음
   	- 외부 저장장치는 업무가 이루어지는 시스템에서만 접근할 수 있어 데이터의 일관성이 보장됨
   - 컨커런트 액세스 : 여러 시스템이 동시에 업무를 나누어 병렬 처리, 시스템 전체가 가동 상태로 업무를 수행하기 때문에 한 시스템에 장애가 발생해도 다른 시스템으로 작업을 이동하지 않고도 고가용성 보장
   	- 두 클러스터가 동일한 업무를 수행하기 위해 L4 스위치를 이용하여 작업 분배
   	- 외부 저장장치는 전체 시스템에서 동시에 접근 가능
   	- 주로 데이터베이스와 쌍을 이루어 구성
   ```

