# 21.01.23

## 주요 질문

#### 💡 [질문1](#개념1)
   * 답변
   
#### 💡 질문2
   * 답변
   
#### 💡 질문3
   * 답변



<br/>

## 심화 질문

#### 💡 질문1
   * 답변
   
#### 💡 질문2
   * 답변
   
#### 💡 질문3
   * 답변


<br/>

## ⭐ 개념 정리

### 프로토콜(Protocol)
   * 컴퓨터나 원거리 통신 장비 사잉에서 메시지를 주고 받는 양식과 규칙

<br/>

### TCP/UDP
   |TCP|UDP|공통점|
   |-|-|-|
   |연결형 서비스|비연결형 서비스|포트번호로 주소를 지정|
   |흐름제어|신뢰성 보장 X|데이터 오류 검출을 위한 체크섬 존재|
   |오류제어|빠른 속도||
   |신뢰성 보장|낮은 네트워크 부하||
   |가상 회선 방식|데이터그램 방식||

<br/>

   <details markdown="1">
    <summary>출처</summary>
    <!--summary 아래 빈칸 공백 두고 내용을 적는공간-->
    출처적어주세요
  </details>

<br/>

### TCP
   * 연결형 서비스  
      * 3-way handshake (연결)
      ![image](https://user-images.githubusercontent.com/36289638/105574098-9d997900-5da5-11eb-8ac0-67fd1ca1a7c8.png)

      * 4-way handshake (종료)
      ![image](https://user-images.githubusercontent.com/36289638/105574320-249b2100-5da7-11eb-9905-2ae894a7e3d8.png)

   
   * 흐름제어  
   송신측의 처리 속도 > 수신측의 속도 경우에 발생하는 문제 제어  
      1. 수신 측은 자신이 처리할 수 있는 데이터 양인 윈도우 크기를 응답 헤더에 담아 송신 측에 전달  
      2. 송신 측은 이를 참고하여 윈도우 크기와 네트워크 상황을 참고해 알맞은 양의 데이터 전송  

   * 오류제어  
   통신 중 오류가 발생하여 데이터를 재전송(비효율적)하는 상황 제어
      * NACK : 송신 측에게 ACK이 오지 않거나 중복된 ACK이 오는 경우 NACK 전송  
      * Stop and Wait : ACK 응답을 받은 뒤에 다음 데이터 보내기
      * Go Back N : 데이터 오류 발생된 시점부터 데이터를 다시 전송
      * Selective Repeat : 오류난 데이터만 재전송


   * 가상 회선 방식  
      * 패킷 전송되기 전에 패킷 헤더에 미리 경로를 설정  
      * 설정된 경로만을 따라 데이터를 전송  
   ![image](https://user-images.githubusercontent.com/36289638/105573716-d71cb500-5da2-11eb-8198-86d2f2c0a1bc.png)


   <details markdown="1">
    <summary>출처</summary>
    <!--summary 아래 빈칸 공백 두고 내용을 적는공간-->
    출처적어주세요
  </details>

<br/>

### UDP
   * 비연결형 서비스  
   ![image](https://user-images.githubusercontent.com/36289638/105574739-e94e2180-5da9-11eb-80bf-ff356b91e40f.png)


   * 데이터그램 방식  
      * 패킷마다 최적의 경로를 선택  
   ![image](https://user-images.githubusercontent.com/36289638/105573732-f87da100-5da2-11eb-9b9a-f9fb0fdaf711.png)

<br/>
