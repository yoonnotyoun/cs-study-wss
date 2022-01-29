# 99 총정리

*네트워크 면접 대비*



## 1. 네트워크의 이해와 설정

1. 네트워크란 무엇인가요?

   ```
   [Keyword] : 
   
   
   ```

2. 인터넷, 인트라넷, 엑스트라넷의 차이점은 무엇인가요?

   ```
   [Keyword] : 
   
   
   ```

## 2. 네트워크의 구성

1. 스위치와 허브의 차이점을 말해보세요.

   ```
   [Keyword] : 
   
   
   ```

2. 127.0.0.1과 localhost는 무엇을 의미합니까?

   ```
   [Keyword] : 
   
   
   ```

3. 네트워크에는 어떤 유형이 있나요?

   ```
   [Keyword] : 
   
   
   ```

## 3. 네트워크 통신

1. 무상태와 비연결성에 대해 설명해보세요.

   ```
   [Keyword] : 
   
   
   ```

## 4. OSI 참조 모델

1. OSI 참조 모델의 계층을 각각 간략하게 설명해보세요.

   ```
   [Keyword] : 
   
   
   ```

2. DNS에 대해 설명해보세요.

   ```
   [Keyword] : 
   
   
   ```

## 5. 네트워크 계층(IP)

1. 프로토콜이란 무엇인가요?

   ```
   [Keyword] : 
   
   
   ```

2. ARP와 RARP를 비교해보세요.

   ```
   [Keyword] : 
   
   
   ```

3. 데이터 캡슐화란 무엇입니까?

   ```
   [Keyword] : 
   
   
   ```

4. NIC란 무엇입니까?

   ```
   [Keyword] : 
   
   
   ```

5. 공인 IP와 사설 IP의 차이점을 설명해주세요.

   ```
   [Keyword] : 
   
   
   ```

6. 라우팅이 무엇인지 설명하고, 라우팅 테이블을 포함하여 라우팅 과정을 설명해보세요.

   ```
   [Keyword] : 
   
   
   ```

## 6. 전송 계층(TCP)

1. TCP와 UDP의 차이에 대해 설명해보세요.

   ```
   [Keyword] : TCP - 신뢰성, 순차적 전달, 3-way 핸드셰이킹 / UDP - 비연결형, 빠른 전송 속도
   
   [TCP (Transmission Control Protocol, 전송제어 프로토콜)]
   - TCP는 신뢰성 있는 데이터를 전송하기 위해 설계된 프로토콜로, 순차적인 전달을 한다는 특징을 갖습니다.
   - 패킷, 흐름 제어, 단편화, 전송 보장 기능을 제공합니다.
   - 신뢰적인 연결을 위해 3-way 핸드셰이킹이 진행됩니다.
   
   [UDP (User Datagram Protocol, 사용자 데이터그램 프로토콜)]
   - UDP는 비연결형 프로토콜로, 전송 속도가 빠르다는 특징이 있습니다.
   - 상위 계층에 신뢰성을 보장하는 프로토콜이 있거나, 멀티미디어 데이터 전송처럼 전송 속도가 중요할 때 주로 쓰입니다.
   ```

2. 3-Way-HandShaking에 대해 설명해보세요.

   ```
   [Keyword] : 데이터 전송, 신뢰, 패킷 요청
   
   - 3-way 핸드셰이킹이란 데이터를 전송하기 전에 신뢰할 수 있는 연결을 확립하기 위해 패킷 요청을 세 번 교환하는 것입니다.
   ```

## 7. 응용 계층

1. 주요 프로토콜에 대해 간략하게 설명하세요. (HTTP, FTP, SMTP, POP, SNMP, DHCP, TCP, UDP, IP, ARP, RARP, ICMP)

   ```
   HTTP (HyperText Transfer Protocol)
   - 하이퍼텍스트 문서를 교환하기 위한 프로토콜
   
   FTP (File Transfer Protocol)
   - 파일 전송을 위한 프로토콜
   
   SMTP (Simple Mail Transfer Protocol)
   - 메일을 송신하기 위한 프로토콜
   
   POP (Post Office Protocol)
   - 메일을 수신하기 위한 프로토콜
   
   SNMP (Simple Network Management Protocol)
   - 네트워크 장비 요소 간에 네트워크 관리 및 전송을 위한 프로토콜
   
   DHCP (Dynamic Host Configuration Protocol)
   - IP주소를 자동으로 할당하고 관리하는 프로토콜
   
   TCP (Transmission Control Protocol)
   - 데이터 흐름을 제어하고 에러 유무를 검사하는 프로토콜
   
   UDP (User Datagram Protocol)
   - 데이터그램(데이터 전송 단위) 전송을 위한 프로토콜
   
   ARP (Address Resolution Protocol)
   - IP주소를 물리적 주소(MAC)로 대응시켜 주는 프로토콜
   
   RARP (Reverse Address Resolution Protocol)
   - 물리적 주소(MAC)로 IP주소를 알려주는 프로토콜
   
   ICMP (Internet Control Message Protocol)
   - 통신 중에 발생하는 오류 처리와 정보 경로 변경 등을 위한 제어 메시지 관리 프로토콜
   ```

2. DHCP에 대해, 동작 과정을 포함하여 설명해주세요.

   ```
   [Keyword] : 
   
   
   ```

3. 슬라이딩 윈도우란 무엇인가?

   ```
   [Keyword] : 송신 버퍼, 고정 크기 윈도우, 옮김, 패킷
   
   - 슬라이딩 윈도우란, 송신 버퍼 역할을 하기 위해 송신 윈도우를 이동하는 방식입니다.
   - 수신 측에서 설정한 윈도우 크기에 포함되는 모든 패킷을 전송하고, 전송이 확인되는 대로 다음 요청 값으로 윈도우를 옮겨 다음 패킷들을 전송합니다.
   ```

   

## 10. 네트워크 보안

1. SSL 인증서 암호와 방식인 비밀키 암호화 방식과 공개키 암호화 기법에 대해 설명해보세요.

   ```
   [Keyword] : 
   
   
   ```

2. HTTP와 HTTPS 통신 방식의 차이에 대해 설명해보세요. (암호화되지 않은 프로토콜 vs 암호화된 프로토콜)

   ```
   [Keyword] : 
   
   
   ```

## 11. 기타

1. 프록시 서버란 무엇인가?

   ```
   [Keyword] : 
   
   
   ```

2. REST API에 대해 설명해보세요.

   ```
   [Keyword] : 
   
   
   ```

3. GET과 POST 방식을 비교해주세요.

   ```
   [Keyword] : HTTP 프로토콜, 서버 요청, HTTP Request Message, url, Body, 데이터 크기, 보안성, 조회, 변경
   
   - GET과 POST는 둘 다 HTTP 프로토콜을 이용해서 서버에 요청할 때 사용하는 방식입니다.
   - GET의 경우, 요청하는 데이터가 HTTP Request Message의 Header 부분에 url 안에 담겨서 전송됩니다. 이때 url에 담겨서 전송되기 때문에, 데이터의 크기가 제한적이고 보안성이 떨어집니다.
   - 이에 따라 보통 서버에서 데이터를 가져와서 보여주는 용도로 사용됩니다.
   - POST의 경우, 요청하는 데이터가 HTTP Request Message의 Body 부분에 데이터가 담겨서 전송됩니다. 따라서 담을 수 있는 데이터 크기가 크고 암호화가 가능하며 보안성이 높습니다.
   - 중요하게 서버 DB의 값을 변경할 때 주로 사용됩니다.
   ```

4. URL에 www.naver.com을 쳤을 때 일어나는 일들을 설명하세요.

   ```
   (답변 참고: [https://owlgwang.tistory.com/1](https://owlgwang.tistory.com/1))
   ```
