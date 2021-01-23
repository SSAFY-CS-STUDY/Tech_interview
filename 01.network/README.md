# Part 01. Network

## 01-1. Core of Network Overview

|설명|링크|
|------|-----|
|OSI 7 layers와 TCP/IP 4 layers|[✅보러가기](#OSI-7-layers와-TCP/IP-4-layers)|
|TCP와 UDP|[✅보러가기](#TCP와-UDP)|
|HTTP와 HTTPS|[✅보러가기](#HTTP와-HTTPS)|
|DNS와 DHCP|[✅보러가기](#DNS와-DHCP)|
|로드밸런서|[✅보러가기](#로드밸런서)|


## 01-2. Web of Network Overview

|설명|링크|
|------|-----|
|basic|[✅보러가기](#basic)|
|cookie와 session|[✅보러가기](#cookie와-session)|
|RESTful API|[✅보러가기](#RESTful-API)|
|AJAX|[✅보러가기](#AJAX)|
|CORS|[✅보러가기](#CORS)|
|Socket|[✅보러가기](#Socket)|
|DOM과 가상DOM|[✅보러가기](#DOM과-가상DOM)|
|SPA|[✅보러가기](#SPA)|
|JWT|[✅보러가기](#JWT)|


[뒤로](https://github.com/SSAFY-CS-STUDY/Tech_interview)

</br>




## 01-1. Core of Network

## 추가해야할 것

- [ ] MAC주소와 IP주소
- [ ] 서브네팅과 서브넷 주소
- [ ] 방화벽


## OSI 7 layers와 TCP/IP 4 layers



#### 💡 프로토콜이란?

서로 다른 기기들 간의 데이터 교환을 위해 표준화한 통신 규약입니다. 프로토콜의 기능에는 흐름제어, 오류제어, 순서제어 등이 있습니다.
* __흐름제어__ 는 수신측에서 송신측이 송신하는 데이터의 전송량이나 전송 속도를 조절하는 기능입니다. 
이 때, 정지 대기 방식과 슬라이딩 윈도우 방식을 사용합니다.
* __오류제어__ 는 전송중에 발생하는 오류를 검출하고 정정하여 정보의 파손에 대비하는 기능입니다.
* __순서제어__ 는 데이터 블록에 전송 순서를 부여하는 기능입니다.
송신 데이터들이 순서적으로 전송되도록 함으로써 흐름제어 및 오류제어를 용이하게 합니다.

#### 💡 패킷이란?
   * 3계층인 네트워크 계층에서 교환되는 정보의 단위입니다.
패킷에는 번호가 붙여지고, 목적지 주소와 오류검출 비트가 포함됩니다.


#### 💡 OSI 7 Layer와 각 계층에 대한 설명을 해주세요.
OSI 7 계층은 국제 표준 기관 ISO가 통신 접속부터 완료까지의 과정을 총 7단계로 정의한 국제 통신 표준 모델입니다.

OSI 7 계층은 Physical, Data Link, Network, Transport, Session, Presentation, Application으로 구성되어 있습니다.
* 물리계층은 데이터를 전기신호로 바꿔주는 계층입니다.
* 데이터링크 계층은 MAC 주소를 가지고 통신하는 계층입니다. 오류검출과 흐름제어를 통해 데이터가 안전하게 도달하도록 합니다.
* 네트워크 계층은 IP주소를 이용해서 최적의 경로를 제공하는 역할입니다.
* 전송계층은 데이터 전송을 위한 논리적인 연결을 하는 역할을 합니다. 
* 표현계층은 서로 다른 Application들이 data를 이해할 수 있도록 도와주는 계층입니다. 데이타의 압축, 암호화, JPEG포맷 등을 수행합니다.

#### 💡 TCP/IP Layer와 각 계층에 대한 설명을 해주세요.
#### 💡 OSI 7 Layer 또는 TCP/IP Layer에서 계층화하는 이유가 무엇인가요?
#### 💡 Encapsulation과 Decapsulation을 서로 비교하며 설명해주세요
#### 💡 IP란?
#### 💡 IP 주소란?
#### 💡 IPV4 vs IPV6 을 설명해주세요.
#### 💡 IPv4의 주소 부족현상을 해결하기 위해 현재 어떤 방법을 사용하고 있나요?

## TCP와 UDP
#### 🐸 외우기 꿀팁 대방출
- TCP 연결형/신뢰성/흐름제어 
- UDP 비연결형/비신뢰성/속도빠름

#### 💡 TCP와 UDP의 특징과 차이점을 설명해주세요.
#### 💡 TCP를 사용하는 대표적인 프로토콜은 무엇인가요?
#### 💡 3-Handshaking과 4-Handshaking의 과정을 설명해주세요.
#### 💡 3-way handshaking 과정에서 클라이언트가 서버가 보낸 ACK+SYN을 받지 못하면?
#### 💡 클라이언트와 서버는 무엇인가요?
#### 💡 4-way handshaking 과정에서 서버가 마지막에 FIN을 보내는 이유?
#### 💡 4-way handshaking 과정에서 클라이언트가 마지막에 ACK를 굳이 보내는 이유?
#### 💡 만약 Server에서 FIN 세그먼트를 전송하기 전에 전송한 패킷이 Routing 지연이나 패킷 유실로 인한 재전송 등으로 인해 FIN 패킷보다 늦게 도착하는 상황이 발생하면 어떻게 될까?
#### 💡 TCP의 연결 설정 과정(3단계)과 연결 종료 과정(4단계)이 단계가 차이나는 이유?
#### 💡 초기 Sequence Number인 ISN을 0부터 시작하지 않고 난수를 생성해서 설정하는 이유?
#### 💡 UDP에서 신뢰도를 보장하는 방법을 설명해주세요.

## HTTP와 HTTPS

#### 💡 HTTP와 HTTPS를 설명해주세요
#### 💡 HTTP의 단점을 설명해주세요
#### 💡 HTTP1.1와 HTTP2.0 차이점은 무엇인가요?
#### 💡 HTTP는 왜 비연결성인가?
#### 💡 모든 웹 페이지에서 HTTPS 를 사용하지 않는 이유를 설명해주세요.
#### 💡 대칭키 암호화 방식은 무엇인가요?
#### 💡 비대칭키 또는 공개키 암호화 방식은 무엇인가요?
#### 💡 HTTP REQUEST 방식 중 GET과 POST의 차이을 설명해주세요.
#### 💡 GET, POST를 제외하고 다른 방식들을 설명해주세요.
#### 💡 조회하기 위한 용도 POST가 아닌 GET 방식을 사용하는 이유?
#### 💡 현대 웹 에서는 비연결성을 해결방법을 설명해주세요.

## DNS와 DHCP

#### 💡 도메인과 DNS가 무엇인지 설명해주세요
#### 💡 Domain Name 구조를 설명해주세요.
#### 💡 DNS round robin 방식의 문제점과 해결방법을 설명해주세요.
#### 💡 DHCP 서버의 역할을 간단히 설명해주세요
#### 💡 Domain Name System 과정을 설명해주세요.

## 로드밸런서

#### 💡 로드 밸런싱을 설명해주세요.
#### 💡 L4 로드 밸런싱과 L7 로드 밸런싱에 대해 설명하고, 차이를 말해보세요
#### 💡 게이트웨이란?
#### 💡 서버에 트래픽이 주어졌을 때 어떻게 응답속도를 개선할 수 있는가요


</br>



</br>


## 01-2. Web of Network 

## basic
#### 💡 클라이언트와 서버는 무엇인가요?
#### 💡 url과 uri에 대해 각각 설명해주세요
#### 💡 브라우저에 "www.google.com" 입력하면 어떤일이 일어날까요?

## cookie와 session
#### 💡 현대 웹 에서는 비연결성을 해결방법을 설명해주세요.
#### 💡 cookie와 session에 대해 설명해주세요
#### 💡 Session 동작 순서를 설명해주세요.
#### 💡 cookie를 쓰는 이유를 설명해주세요
#### 💡 Cookie, Session Storage, Local Storage 사이 차이점을 설명해주세요

## RESTful API
#### 💡 RESTful API란 무엇인가요?

Rest를 Rest답게 쓰기 위한 방법입니다.

Restful의 목적은 이해하기 쉽고 사용하기 쉬운 REST API를 만드는 것입니다.

Rest란 네트워크 상에서 Client와 Server 가 통신하는 방식입니다. HTTP URI를 통해 자원을 명시하고, HTTP method(Post, Put, Get, Delete)를 통해 해당 자원에 대한 CRUD를 적용하는 것을 의미합니다.

#### 💡 GET방식과 POST 방식의 차이점을 설명해보세요
#### 💡 GET, POST를 제외하고 다른 방식들을 설명해주세요.

## AJAX
#### 💡 Ajax는 무엇인가요?
#### 💡 Ajax의 장점과 단점은 무엇인가요?

## CORS
#### 💡 CORS는 무엇인가요?

CORS란 서로 다른 Origin끼리 자원을 공유할 수 있는 방식입니다.

HTTP 헤더를 사용해서 한 origin에서 실행중인 웹앱이 다른 origin의 자원에 접근할 수 있는 권한을 부여할 수 있는 방식입니다. 

서로 다른 Origin이란 것은 Protocol, Host, Port 중 하나라도 다른 것을 의미합니다.

#### 💡 CORS preflight는 무엇인가요?

preflight request는 실제 요청을 보내도 안전한지 판단하기 위해 사전에 보내는 요청입니다.

OPTIONS 메서드로 요청하며 CORS를 허용하는지 확인합니다. CORS가 허용된 웹서버라면 사용 가능한 리소스를 헤더에 담아 응답합니다.

## Socket
#### 💡 소켓이란 무엇인가요?
#### 💡 HTTP와 웹소켓 차이점은 무엇인가요?
#### 💡 웹소켓 (WebScoket)과 TCP/IP 소켓의 차이점은 무엇인가요?

## DOM과 가상DOM

## OAuth2
#### 💡 OAuth2의 동작방식이 어떻게 되나요?


## SPA
## JWT


[뒤로](https://github.com/SSAFY-CS-STUDY/Tech_interview)/[위로](#part-1-3-network)

</br>

</br>

_Network.end_