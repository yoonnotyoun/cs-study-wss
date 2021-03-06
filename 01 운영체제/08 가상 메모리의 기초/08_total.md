# 08 가상 메모리의 기초

*<쉽게 배우는 운영체제> pg 418~420*



## 연습문제

1. 가상 메모리에서 메모리 관리자가 사용할 수 있는 전체 크기는 어떻게 결정되는가?

   ```
   물리 메모리와 스왑 영역의 합
   ```

2. 가상 주소에서 하나의 프로세스가 사용할 수 있는 최대 주소는 무엇과 연관이 있는가?

   ```
   물리 메모리 (CPU의 비트)
   ```

3. 가상 메모리에서 가상 주소를 골라 주소로 변환하기 위해 사용하는 자료 구조를 무엇이라 하는가?

   ```
   매핑 테이블 (또는 페이지 테이블)
   ```
   
4. 페이징 기법의 주소 변환 과정 식을 쓰시오.

   ```
   VA = <P, D> -> PA = <F, D>
   ```

5. 페이지 테이블에서 각각의 한 줄을 무엇이라 하는가?

   ```
   페이지 테이블 엔트리(Page Table Entry, PTE)
   ```

6. 가상 주소를 <P, D>로 변환하는 공식을 쓰시오.

   ```
   P = 나눗셈(가상주소/한 페이지의 크기)의 몫
   D = 나눗셈(가상주소/한 페이지의 크기)의 나머지
   ```

7. 각 페이지 테이블의 시작 주소를 가지고 있는 레지스터는 무엇인가?

   ```
   페이지 테이블 기준 레지스터(Page Table Base Register, PTBR)
   ```

8. 페이지 테이블 매핑 방식 중, 모든 페이지 테이블을 스왑 영역에 저장하고 그중 일부만 물리 메모리에 무작위로 가지고 있는 방식은 무엇인가?

   ```
   연관 매핑
   ```

9. 페이지 테이블 매핑 방식 중, 모든 페이지 테이블을 물리 메모리에 보관하는 방식은 무엇인가?

   ```
   직접 매핑
   ```

10. 페이지 테이블 매핑 방식 중, 모든 페이지 테이블을 스왑 영역에 저장하고 페이지 테이블을 일정한 집합 단위로 물리 메모리에 보관하는 방식은 무엇인가?

    ```
    집합-연관 매핑
    ```

11. 페이지 테이블 매핑 방식 중, 물리 메모리의 프레임 번호를 기준으로 테이블을 구성하는 방식은 무엇인가?

    ```
    역매핑
    ```

12. 연관 매핑에서 사용하는 테이블의 이름은 무엇인가?

    ```
    변환 색인 버퍼 (TLB, Translation Look-aside Buffer)
    ```

13. 연관 매핑에서 원하는 데이터가 변환 색인 버퍼에 없는 상태를 무엇이라 하는가?

    ```
    TLB 미스
    ```

14. 연관 매핑에서는 전체-매핑 테이블을 어디에 보관하는가?

    ```
    스왑 영역
    ```

15. 가상 메모리에서 메모리 관리자는 물리 메모리 영역과 스왑 영역을 합쳐서 프로세스가 사용하는 가상 주소를 실제 메모리의 물리 주소로 변환한다. 이러한 작업을 무엇이라 하는가?

    ```
    동적 주소 변환 (DAT)
    ```

16. 사용자 프로세스가 자신의 크기보다 더 큰 주소에 접근하려고 하면 메모리 관리자는 그 프로세스를 강제 종료한다. 이때 발생하는 오류를 무엇이라 하는가? 

    ```
    트랩
    ```

17. 세그멘테이션-페이징 혼용 기법에서는 접근 권한을 어디에서 관리하는가?

    ```
    세그멘테이션 테이블
    ```



## 심화문제

1. 가상 메모리가 이론적으로 가질 수 있는 크기와 실제 운영되는 크기는 어떤 차이가 있는지 설명하시오.

   ```
   이론적으로는 가상 메모리는 무한대의 크기이다. 그러나 실제로 가상 메모리의 최대 크기는 그 컴퓨터 시스템이 가진 물리 메모리의 최대 크기로 한정되며, CPU의 비트에 따라 결정된다. 32bit CPU의 경우 32bit로 표현할 수 있는 최댓값인 2의 32제곱 - 1, 즉 약 4GB가 메모리의 최대 크기이고, 가상 메모리의 최대 크기도 약 4GB이다. -> 더 큰 운영체제를 실행하려면 물리 메모리의 내용 중 일부를 하드디스크의 일부 공간, 즉 스왑 영역으로 옮긴다.
   ```

2. 페이징 기법의 주소 변환 과정을 그림으로 그리고 설명하시오.

   ```
   VA = <P, D> -> PA = <F, D>
   
   <과정>
   1. 가상 주소가 어느 페이지에 있는지 찾기
   2. 페이지 테이블에서 해당 페이지가 어떤 프레임에 있는지 확인
   3. 확인한 물리 메모리 프레임에 접근(D는 같음)
   
   페이지 테이블을 사용하여 P는 F로 바꾸고 D는 변경 없이 그대로 사용한다. D를 변경하지 않는 이유는 페이지와 프레임의 크기를 똑같이 나누었기 때문이다.
   ```

3. 연관 매핑의 동작을 설명하시오.

   ```
   연관 매핑 : 페이지 테이블 전체를 스왑 영역에서 관리하고 일부만 물리 메모리로 가져오는 방식
   동작 : 페이지 테이블 일부만 가져옴 -> 물리 메모리 내에 페이지 테이블을 다 검색 -> 못 찾으면 스왑 영역에 있는 테이블을 검색
   
   - 메모리에 접근하기 위해 변환 색인 버퍼를 찾아본다.
   - 원하는 페이지 번호가 있는 경우 : TLB 히트로, 곧바로 물리주소로 변환
   - 원하는 페이지 번호가 없는 경우 : TLB 미스로, 스왑 영역에 저장된 직접 매핑 테이블을 사용하여 프레임 번호로 변환
   ```

4. 집합-연관 매핑의 동작을 설명하시오.

   ```
   집합-연관 매핑 : 연관 매핑과 비슷하지만 페이지 테이블을 일정한 집합(여러 묶음)으로 자르고, 자른 덩어리 단위로 물리 메모리에서 가져 옴
   동작 : 페이지 테이블을 일정한 집합으로 자르고, 자른 덩어리 단위로 물리 메모리에 가져옴 -> 메모리에 있는지 스왑 영역에 있는지 표시하는 디렉터리 테이블을 이용해서 어디에 있는지 알 수 있다.
   
   - P1을 이용하여 디렉터리 테이블에서 주소를 찾음
   - I라고 표시되어 있지 않은 경우 : TLB히트로, 묶음 테이블의 시작 주소에 시작 주소가 명시되어 있음.
   - I라고 표시되어 있는 경우 : TLB미스가 발생한 것
   - P2를 이용하여 묶음 테이블에서 원하는 프레임 번호를 얻음
   ```

5. 역매핑의 동작을 설명하시오.

   ```
   역매핑 : 물리 메모리의 프레임 번호를 기준으로 테이블을 구성
   동작 : 물리 메모리의 프레임에 어떤 프로세스의 어떤 페이지가 올라와 있는지 표시 -> 프로세스의 아이디와 페이지 번호가 물리 메모리에 있는지 역매핑 테이블에서 검색 -> 없으면 스왑 영역에서 가져옴
   ```

6. 세그먼테이션-페이징 혼용 기법을 사용하는 이유를 설명하시오.

   ```
   페이징 기법에서 권한비트를 추가하면 메모리 접근 권한이 거의 같은데도 불구하고 행마다 페이지 테이블에 생겨 낭비가 발생한다.
   
   권한 비트 추가에 따라 페이지 테이블의 크기가 커지는 문제를 세그먼테이션 테이블을 이용하여 해결할 수 있다.
   ```
