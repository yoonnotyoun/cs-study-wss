# 03 네트워크 통신

*<네트워크 개론> pg 173~176*



## 연습문제

1. 

   ```
   - 유니캐스트 : 일대일 통신 방식(가장 많이 사용), 송신지와 수신지의 주소를 사용하고 주소가 동일하면 수신 다르면 프레임을 버림, 성능 문제 없음
   - 브로드캐스트 : 일대다 통신 방식, 주소가 동일하지 않아도 패킷을 CPU에 보냄, 성능이 떨어짐
   - 멀티캐스트 : 특정 그룹에만 한 번에 데이터를 전송, 스위치나 라우터가 지원할 때만 사용 가능
   ```

2. 

   ```
   단방향 통신
   ```

3. 

   ```
   양방향 통신
   ```

4. 

   ```
   - 반이중 통신 : 휴대용 무전기와 모뎀을 이용한 통신
   - 전이중 통신 : 라우터
   ```

5. 

   ```
   - 동기식 전송 : 송신기와 수신기가 동일한 클록 사용, 끊어지지 않는 0과 1의 문자열로 전송
   - 비동기식 전송 : 송신기와 수신기가 별도의 독립적인 클록 신호를 사용, 한 번에 한 문자씩 전송
   ```

6. 

   ```
   - 패리티 비트 검사 : 전송하는 데이터마다 패리티 비트를 하나씩 추가하여 홀수 또는 짝수 검사 방법으로 오류를 검출한다.
   - 블록 합 검사 : 문자를 블록으로 전송하면 오류 확률이 높아지므로 오류 검출 능력을 향상하기 위해 수평 패리티와 수직 패리티를 적용하여 문자 블록을 이차원적으로 검사하는 방식
   - 순환 중복 검사 : 정확히 오류를 검출하기 위해 다항식 코드를 사용하는 방식
   ```

7. 

   ```
   블록 합 검사
   ```

8. 

   ```
   P.129 참고
   ```

9. 

   ```
   베이스 밴드 방식
   ```

10. 

    ```
    - 동축 케이블에 연결된 컴퓨터를 서로 접속시키는 방식
    - 모든 컴퓨터는 버스(케이블)에 연결되어 있고 전송 매체는 컴퓨터로 공유할 수 있음
    ```

11. 

    ```
    - 토큰링 방식 : 각 컴퓨터(노드)마다 전송 기회가 공평하게 주어짐, 성능 저하가 심하지 않음, 구현이 어렵고 토큰 운용 관리가 복잡
    - 토큰버스 방식 : 이더넷 + 토큰링 특징을 합친 형태, 버스의 모든 컴퓨터는 논리적으로 링형 접속 형태를 띔, 데이터 충돌이 발생하지 않기 때문에 한 패킷을 전송하는 데 걸리는 시간이 일정함
    ```

12. 

    ```
    이더넷, 고속 이더넷, 기가비트 이더넷, FDDI
    ```

13. 

    ```
    - 회선 교환 방식 : 두 스테이션 사이에 전용 통신 경로가 있음, 데이터를 전송하기 전에 하나의 물리적 경로를 설정하며, 통신을 종료할 때까지 이 경로를 독점함
    - 메세지 교환 : 가변 길이의 메시지 단위로 저장/전송 방식에 따라 데이터를 교환
    - 패킷 교환 : 데이터는 패킷이라는 작은 조각으로 나뉘고, 각 패킷은 고유 번호가 있어 수신지에 전송되었을 때 원래의 데이터로 재결합해서 구성할 수 있음
    ```

14. 

    ```
    - 장점 : 케이블 배선이 필요 없어 LAN의 설치 및 네트워크 구축이 용이, 단말기의 이동이 자유로움, 유지 보수가 비교적 편함
    - 단점 : 전송 속도가 유선 LAN보다 느림, 접속 장치가 유선 LAN보다 비쌈
    ```

15. 

    ```
    잘 모르겠습니다...ㅜㅡㅜ 대체 어디에 채널에 대한 정의가 있나요
    ```

16. 

    ```
    애드혹 모드
    ```

17. 

    ```
    송신 측에서 데이터를 전송할 때 먼저 AP로 필요한 총 시간을 담은 RTS 프레임을 보내고, AP는 CTS 프레임을 브로드캐스팅하여 응답함
    ```

18. 

    ```
    1. 무선 AP는 자신을 알리는 신호인 비콘을 네트워크에 있는 모든 기기에 주기적으로 전송한다. 무선 클라이언트는 이 신호를 잡아서 연결하는 것이다.
    2. 신호를 받은 무선 클라이언트는 자신의 SSID와 동일한지 무선 AP에 문의한다.
    3. 동일한 SSID이면 무선 AP가 응답을 하고 서로의 존재를 알게 된다.
    4.5. 설정한 인증 방식이 올바른지 확인받은 후 무선 클라이언트는 무선 AP에 연결(접속)을 요청한다.
    6. 무선 AP로부터 승인을 받으면 연결하여 통신할 수 있다.
    ```




## 기출문제

1. 

   ```
   4
   ```

2. 

   ```
   1
   ```
   
3. 

   ```
   2
   ```
   
4. 

   ```
   4
   ```
   
5. 

   ```
   
   ```
   
6. 

   ```
   1
   ```

7. 

   ```
   1

8. 

   ```
   3
   ```

9. 

   ```
   3
   ```

10. 

    ```
    브로드밴드
    ```

11. 

    ```
    SSID
    ```

    



