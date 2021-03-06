# 07 응용 계층

*<네트워크 개론> pg 356~357*



## 연습문제

1. 

   ```
   FTP(TCP 포트: 21)
   - 클라이언트-서버 간의 파일 전송
   - 클라이언트는 소스 포트 번호로 1023보다 큰 임의의 번호를 사용하고, FTP 서버의 포트 번호는 21을 사용
   - FTP 클라이언트 프로그램에서 서버의 주소를 입력하여 접속이 되면 파일을 업로드하거나 다운로드할 수 있음
   - ID와 패스워드가 필요한 일반적인 FTP와 누구나 접속 가능한 익명 FTP로 구분
   ```

2. 

   ```
   HTTP 서비스(TCP 포트: 80)
   ```

3. 

   ```
   HTTP 1.0
   - 전송받을 문서에 이미지가 있으면 문서를 받을 때와 이미지를 받을 때 각각 연결을 설정
   
   HTTP 1.1
   - 다시 연결을 설정하지 않고 연결된 소켓을 통해 데이터(이미지)를 전송받음
   - 프로토콜의 수행 성능이 향상된 것
   ```

4. 

   ```
   DHCP(UDP 포트: 67, 68)
   ```

5. 

   ```
   - 루프백 주소 127.0.0.1 이고 이름은 localhost
   - 이 과정을 통해 컴퓨터에서 TCP/IP 서비스가 제대로 작동하는지 확인할 수 있음
   - 정상 작동하면 해당 호스트의 내부적인 IP 설정에 문제가 없음을 의미
   ```

6. 

   ```
   세션 계층
   ```

7. 

   ```
   TCP
   - FTP, HTTP, SMTP, POP3, IMAP
   
   UDP
   - SNMP, DHCP
   ```

8. 

   ```
   - 에코 요청과 에코 응답 메시지가 담겨 있음
   - Ping 프로그램은 ARP 유틸리티를 이용하여 목적지 컴퓨터 이름을 IP 주소로 해석하고 그 판독 정보를 화면에 출력


## 기출문제

1. 

```
   4
```

2. 

   ```
   2: HTTP
   ```

3. 

   ```
   1
   ```

4. 

   ```
   1
   ```

5. 

   ```
   4
   ```
