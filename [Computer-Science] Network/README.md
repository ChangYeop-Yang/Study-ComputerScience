# ■ Study - NETWORK <kbd>[Kyungpook National University](http://www.knu.ac.kr/wbbs/)</kbd>

* 전송 링크로 연결된 상호 협력하는 통신 노드들의 그룹이다.

## 📣 파일 서술자 (File descriptor)

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f8/File_table_and_inode_table.svg/1920px-File_table_and_inode_table.svg.png" />
</p>

* In Unix and related computer operating systems, a file descriptor (FD, less frequently fildes) is an abstract indicator (handle) used to access a file or other input/output resource, such as a pipe or network socket. File descriptors form part of the POSIX application programming interface. A file descriptor is a non-negative integer, generally represented in the C programming language as the type int (negative values being reserved to indicate "no value" or an error condition).

* 파일 디스크립터란 운영체제가 만든 파일 또는 소켓의 지칭을 편히 하기 위해서 부여 된 숫자이다.

## 📣 PORT

* 인터넷 프로토콜 스위트에서 포트(port)는 운영 체제 통신의 종단점이다. 이 용어는 하드웨어 장치에도 사용되지만, 소프트웨어에서는 네트워크 서비스나 특정 프로세스를 식별하는 논리 단위이다. 주로 포트를 사용하는 프로토콜은 전송 계층 프로토콜이라 하며, 예를 들어 전송 제어 프로토콜(TCP)와 사용자 데이터그램 프로토콜(UDP)가 있다. 각 포트는 번호로 구별되며 이 번호를 포트 번호라고 한다. 포트 번호는 IP 주소와 함께 쓰여 해당하는 프로토콜에 의해 사용된다.

##### ※ PORT NUMBER

* 0번 ~ 1023번: 잘 알려진 포트 (well-known port)

* 1024번 ~ 49151번: 등록된 포트 (registered port)

* 49152번 ~ 65535번: 동적 포트 (dynamic port)

## 📣 Endianness

<p align="center">
  <img src="https://www.ibm.com/developerworks/library/l-ibm-xl-c-cpp-compiler/image001.png" />
</p>

* 엔디언(Endianness)은 컴퓨터의 메모리와 같은 1차원의 공간에 여러 개의 연속된 대상을 배열하는 방법을 뜻하며, 바이트를 배열하는 방법을 특히 바이트 순서(Byte order)라 한다. **엔디언은 보통 큰 단위가 앞에 나오는 빅 엔디언(Big-endian)과 작은 단위가 앞에 나오는 리틀 엔디언(Little-endian)으로 나눌 수 있으며, 두 경우에 속하지 않거나 둘을 모두 지원하는 것을 미들 엔디언(Middle-endian)이라 부르기도 한다.**

## 📣 Packet switching (패킷 교환)

<p align="center">
  <img src="https://user-images.githubusercontent.com/20036523/50885137-36176780-1430-11e9-9f85-954edc1e2b04.gif" />
</p>

* 패킷 교환(Packet switching)은 컴퓨터 네트워크와 통신의 방식 중 하나로 현재 가장 많은 사람들이 사용하는 통신 방식이다. **작은 블록의 패킷으로 데이터를 전송하며 데이터를 전송하는 동안만 네트워크 자원을 사용하도록 하는 방법**을 말한다. 정보 전달의 단위인 패킷은 여러 통신 지점(Node)을 연결하는 데이터 연결 상의 모든 노드들 사이에 개별적으로 경로가 제어된다. 이 방식은 통신 기간 동안 독점적인 사용을 위해 두 통신 노드 사이를 연결하는 회선 교환 방식과는 달리 짤막한 데이터 트래픽에 적합하다.

###### ※ :thumbsup: 패킷 교환의 장점

* 네트워크 자원을 패킷 단위로 나누어 시간을 공유하므로 회선 효율성이 높다.

* 트래픽이 많으면 회선 교환망은 네트워크 부하가 감소할 때까지 요청을 차단하나, 패킷 교환망은 Store-and-Forward 방식을 사용하기 때문에 데이터가 들어오는 속도와 나가는 속도를 맞출 필요 없이 각 스테이션에 맞도록 속도를 조절할 수 있다. 이로써 전송 지연이 줄어들고 통신 안정성이 늘어난다.

###### ※ :thumbsdown: 패킷 교환의 단점

* 보낸 자료의 순서가 도착 자료에 의해서 변경이 된다. 

* Overflow 발생으로 인한 Packet 손실이 발생한다.

## 📣 Circuit switching (회선 교환)

<p align="center">
  <img src="https://i.pinimg.com/originals/99/2e/ed/992eed994ae26883c1febabb8cbb90c6.gif" />
</p>

* 발신자와 수신자 또는 통신 쌍방이 통신을 시작하기 전에 미리 전용 연결(회선 또는 채널)을 설정해야만 하는 네트워크를 말한다. 통신하는 동안에는 해당 연결이 독점적으로 발신자 및 수신자에 의해서만 사용된다. 통신이 끝났을 때는 반드시 연결을 해제하는 절차가 필요하다.

## 📣 [전송 제어 프로토콜 (TCP, Transmission Control Protocol, `SOCK_STREAM`)](https://ko.wikipedia.org/wiki/%EC%A0%84%EC%86%A1_%EC%A0%9C%EC%96%B4_%ED%94%84%EB%A1%9C%ED%86%A0%EC%BD%9C)

* 전송 제어 프로토콜(Transmission Control Protocol, TCP, 문화어: 전송조종규약)은 인터넷 프로토콜 스위트(IP)의 핵심 프로토콜 중 하나로, IP와 함께 TCP/IP라는 명칭으로도 널리 불린다. **TCP는 근거리 통신망이나 인트라넷, 인터넷에 연결된 컴퓨터에서 실행되는 프로그램 간에 일련의 옥텟을 안정적으로, 순서대로, 에러없이 교환할 수 있게 한다. TCP는 전송 계층에 위치한다.** 네트워크의 정보 전달을 통제하는 프로토콜이자 인터넷을 이루는 핵심 프로토콜의 하나로서 국제 인터넷 표준화 기구(IETF)의 RFC 793에 기술되어 있다.

###### 📌 Connection Establishment (3 Way handshaking)

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f0/Three-way-handshake-example.gif/500px-Three-way-handshake-example.gif" width="300" height="300" />
</p>

###### 📌 Connection Termination (4 Way handshaking)

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/55/TCP_CLOSE.svg/1280px-TCP_CLOSE.svg.png" width="300" height="300" />
</p>

* In telecommunications, a handshake is an automated process of negotiation between two communicating in between participants (example "Alice and Bob") through the exchange of information that establishes the protocols of a communication link at the start of the communication, before full communication begins. The handshaking process usually takes place in order to establish rules for communication when a computer attempts to communicate with another device. Signals are usually exchanged between two devices to establish a communication link. For example, when a computer communicates with another device such as a modem, the two devices will signal each other that they are switched on and ready to work, as well as to agree to which protocols are being used.

###### 📌 전송 제어 프로토콜의 특징 (Transmission Control Protocol Features)

* 중간에 데이터가 소멸되지 않고 목적지로의 전송을 보장한다.

* 전송 순서대로 데이터가 수신된다.

* 전송되는 데이터의 경계 (Boundary)가 존재하지 않는다.

###### 🔍 TCP Server 함수호출 순서

<p align="center">
	<img src="https://www.wut.de/pics/misc/e-58www-16-grus-000.gif" />
</p>

1. `Socket()` - 소켓생성

```C++
private:		
   int szClntAddr;
   SOCKET hServSock;
   SOCKADDR_IN servAddr;
   
/* ^---------HEADER---------^ */

// MARK: Create TCP Socket
this->hServSock = socket(PF_INET, SOCK_STREAM, 0);
if (this->hServSock == INVALID_SOCKET) {
	// here error message.
}
```

2. `Bind()` - 소켓 주소할당

```C++
std::memset(&this->servAddr, 0, sizeof(SOCKADDR_IN));
this->servAddr.sin_family		= AF_INET;
this->servAddr.sin_addr.s_addr		= htonl(INADDR_ANY); // INADDR_ANY 모든 IP 대역 접속을 허가한다.
this->servAddr.sin_port			= htons(port);

// MARK: bind 함수는 지역주소를 소켓과 함께 결합(연관)시킵니다.
if (bind(this->hServSock, (sockaddr *)&this->servAddr, sizeof(SOCKADDR_IN)) == SOCKET_ERROR) {
	// here error message.
}
```

3. `Listen()` - 연결요청 대기상태

```C++
// MARK: listen 함수는 소켓을 들어오는 연결에 대해 listening 상태에 배치합니다.
if (listen(this->hServSock, MAX_REQUEST_QUEUE_SIZE) == SOCKET_ERROR) {
	// here error message.
}
```

4. `Accept()` - 연결허용

```C++
// MARK: Accpet 함수는 소켓에 들어오는 연결 시도에 대해서 허가한다.
SOCKADDR_IN clientAddr;
this->szClntAddr    = sizeof(SOCKADDR_IN);
SOCKET hClientSock  = accept(this->hServSock, (SOCKADDR *)&clientAddr, &this->szClntAddr);

if (hClientSock == INVALID_SOCKET || hClientSock == SOCKET_ERROR) {
	// here error message and close sock.
}
```

5. `Read()/Write()` - 데이터 송수신

```C++
const bool OnSendMessage(const SOCKET sock, const std::string message) {
	return send(sock, message.c_str(), message.size(), 0) == 0 ? true : false; // ZERO == Success, EOF == Fail
}

const int OnReceiveMessage(const SOCKET sock) {
	char message[BUFSIZ];
	const int length = recv(sock, message, BUFSIZ, 0);
	return length;
}
```

6. `Close()` - 연결종료

```C++
closesocket(this->hServSock);
```

###### 🔍 TCP Client 함수호출 순서

1. `Socket()` - 소켓생성

```C++
private:		
   SOCKET hServSock;
   SOCKADDR_IN servAddr;
   
/* ^---------HEADER---------^ */

this->hServSock = socket(PF_INET, SOCK_STREAM, 0);
if (this->hServSock == INVALID_SOCKET) { 
	// here error message and close sock.
}
```

2. `Connect()` - 연결요청

```C++
std::memset( &this->servAddr, 0, sizeof(SOCKADDR_IN) );
this->servAddr.sin_family	= AF_INET; // IPv4
this->servAddr.sin_addr.s_addr	= inet_addr("127.0.0.1");
this->servAddr.sin_port		= htons(1234);

// MARK: 생성한 소켓을 통해 서버로 접속을 요청합니다.
if ( connect(this->hServSock, (SOCKADDR *)&servAddr, sizeof(SOCKADDR)) == SOCKET_FAIL_ERROR) {
	// here error message and close sock.
}
```

3. `Read()/Write()` - 데이터 송수신

```C++
const bool OnSendMessage(const SOCKET sock, const std::string message) {
	return send(sock, message.c_str(), message.size(), 0) == 0 ? true : false; // ZERO == Success, EOF == Fail
}

const int OnReceiveMessage(const SOCKET sock) {
	char message[BUFSIZ];
	const int length = recv(sock, message, BUFSIZ, 0);
	return length;
}
```

4. `Close()` - 연결종료

```C++
closesocket(this->hServSock);
```

## 📣 [사용자 데이터그램 프로토콜 (UDP, User Datagram Protocol, `SOCK_DGRAM`)](https://ko.wikipedia.org/wiki/%EC%82%AC%EC%9A%A9%EC%9E%90_%EB%8D%B0%EC%9D%B4%ED%84%B0%EA%B7%B8%EB%9E%A8_%ED%94%84%EB%A1%9C%ED%86%A0%EC%BD%9C)

* 사용자 데이터그램 프로토콜(User Datagram Protocol, UDP)은 인터넷 프로토콜 스위트의 주요 프로토콜 가운데 하나이다. 1980년에 데이빗 리드가 설계하였고, 현재 IETF의 RFC 768로 표준으로 정의되어 있으며, TCP와 함께 데이터그램으로 알려진 단문 메시지를 교환하기 위해서 사용된다. UDP는 유니버설 데이터그램 프로토콜(Universal Datagram Protocol)이라고 일컫기도 한다. **UDP의 전송 방식은 너무 단순해서 서비스의 신뢰성이 낮고, 데이터그램 도착 순서가 바뀌거나, 중복되거나, 심지어는 통보 없이 누락시키기도 한다. UDP는 일반적으로 오류의 검사와 수정이 필요 없는 애플리케이션에서 수행할 것으로 가정한다.** UDP를 사용하는 네트워크 애플리케이션에는 도메인 이름 서비스 (DNS), IPTV, 음성 인터넷 프로토콜 (VoIP), TFTP, IP 터널, 그리고 많은 온라인 게임 등이 있다.

###### 📌 사용자 데이터그램 프로토콜의 특징 (User Datagram Protocol Features)

* 전송되는 순서에 상관없이 가장 빠른 전송을 지향한다.

* 전송되는 데이터는 손실의 우려가 있고, 파손의 우려가 있다.

* 전송되는 데이터의 경계 (Boundary)가 존재한다.

* 한번에 전송할 수 있는 데이터의 크기가 제한된다.

## 📣 OSI 7 Layer

* OSI 모형(Open Systems Interconnection Reference Model)은 국제표준화기구(ISO)에서 개발한 모델로, 컴퓨터 네트워크 프로토콜 디자인과 통신을 계층으로 나누어 설명한 것이다. 일반적으로 OSI 7 계층 모형이라고 한다.

<p align="center">
  <img src="https://t1.daumcdn.net/cfile/tistory/99B9493359B6408E23" />
</p>

* 이 모델은 프로토콜을 기능별로 나눈 것이다. 각 계층은 하위 계층의 기능만을 이용하고, 상위 계층에게 기능을 제공한다. '프로토콜 스택' 혹은 '스택'은 이러한 계층들로 구성되는 프로토콜 시스템이 구현된 시스템을 가리키는데, 프로토콜 스택은 하드웨어나 소프트웨어 혹은 둘의 혼합으로 구현될 수 있다. 일반적으로 하위 계층들은 하드웨어로, 상위 계층들은 소프트웨어로 구현된다.

###### 📌 7계층 – 응용 계층 (Application)

* 디핑 소스 비유를 확장하면 응용 계층은 가장 위에 있다. 사용자에게 보이는 부분이다. OSI 모형에서는 “최종 사용자에게 가장 가까운” 계층이다. **7층에서 작동하는 응용프로그램은 사용자와 직접적으로 상호작용한다.** 구글 크롬(Google Chrome), 파이어폭스(Firefox), 사파리(Safari) 등 웹 브라우저와 스카이프(Skype), 아웃룩(Outlook), 오피스(Office) 등의 응용 프로그램이 대표적이다.

###### 📌 6계층 – 표현 계층 (Presentation)

* 표현 계층은 응용 계층의 데이터 표현에서 독립적인 부분을 나타낸다. 일반적으로 **응용프로그램 형식을 준비 또는 네트워크 형식으로 변환하거나 네트워크 형식을 응용프로그램 형식으로 변환하는 것을 나타낸다.** 다시 말해 이 계층은 **응용프로그램이나 네트워크를 위해 데이터를 “표현”하는 것이다.** 대표적인 예로는 데이터를 안전하게 전송하기 위해 암호화, 복호화하는 것인데, 이 작업이 바로 6계층에서 처리된다.

###### 📌 5계층 – 세션 계층 (Session)

* 2대의 기기, 컴퓨터 또는 서버 간에 “대화”가 필요하면 세션(session)을 만들어야 하는데 이 작업이 여기서 처리된다. 이 계층에는 **설정, 조율(예: 시스템의 응답 대기 기간), 세션 마지막에 응용프로그램 간의 종료 등의 기능**이 필요하다. 전송 단위는 `message`이다.

###### 📌 4계층 – 전송 계층 (Transport)

* 전송 계층은 **최종 시스템 및 호스트 간의 데이터 전송 조율을 담당**한다. **보낼 데이터의 용량과 속도, 목적지 등을 처리**한다. 전송 계층의 예 중에서 가장 잘 알려진 것이 전송 제어 프로토콜(TCP)이다. TCP는 인터넷 프로토콜(IP) 위에 구축되는데 흔히 TCP/IP로 알려져 있다. 기기의 IP 주소가 여기서 작동한다.

* 프로세스 간 전송을 담당하며 전송 단위는 `Segment`이다.

###### 📌 3계층 – 네트워크 계층 (Network)

* 네트워킹 전문가 대부분이 관심을 두고 좋아하는 라우터 기능 대부분이 여기 네트워크 계층에 자리잡는다. 가장 기본적으로 볼 때 이 계층은 **다른 여러 라우터를 통한 라우팅을 비롯한 패킷 전달을 담당한다.** 보스턴에 있는 컴퓨터가 캘리포니아에 있는 서버에 연결하려고 할 때 그 경로는 수백 만 가지다. 이 계층의 라우터가 이 작업을 효율적으로 처리한다.

* 호스트 간 전송을 담당하며 전송 단위는 `Packet`이다.

###### 📌 2계층 – 데이터 링크 계층 (Data Link)

* 데이터 링크 계층은 (두 개의 직접 연결된 노드 사이의) 노드 간 데이터 전송을 제공하며 물리 계층의 오류 수정도 처리한다. 여기에는 2개의 부계층도 존재한다. 하나는 매체 접근 제어(MAC) 계층이고 다른 하나는 논리적 연결 제어(LLC) 계층이다. 네트워킹 세계에서 대부분 스위치는 2계층에서 작동한다. 

* 인접한 노드 간 전송을 담당하며 전송 단위는 `Frame`이다.

###### 📌 1계층 – 물리 계층 (Physical)

* OSI 디핑 소스의 밑바닥에는 물리 계층이 있다. **시스템의 전기적, 물리적 표현을 나타낸다.** 케이블 종류, (802.11 무선 시스템에서와 같은) 무선 주파수 링크는 물론 핀 배치, 전압, 물리 요건 등이 포함된다. 네트워킹 문제가 발생하면 많은 네트워크 전문가가 물리 계층으로 바로 가서 모든 케이블이 제대로 연결돼 있는지, 라우터나 스위치 또는 컴퓨터에서 전원 플러그가 빠지지 않았는지 확인한다. 

## 📣 [TTL (Time To Live)](https://terms.naver.com/entry.nhn?docId=3483862&cid=58439&categoryId=58439)

<p align="center">
  <img src="https://www.cloudflare.com/img/learning/cdn/glossary/ttl/icmp-traceroute-diagram.png" />
</p>

* TTL은 IP헤더 내에서 폐기까지의 시간을 나타낸 부분이다. IP 패킷 내에 있는 값으로서, 그 패킷이 네트워크 내에 너무 오래 있어서 버려져야 하는지의 여부를 라우터에게 알려준다. 패킷들은, 여러 가지 이유로 적당한 시간 내에 지정한 장소에 배달되지 못하는 수가 있다. 예를 들어, 부정확한 라우팅 테이블의 결합은 패킷을 끝없이 순환하게 만들 수도 있다. 일정한 시간이 지나면 그 패킷을 버리고, 재전송할 것인지를 결정하도록 그 사실을 발신인에게 알릴 수 있게 하기 위한 해결책으로 TTL이 사용된다.

## 📣 TCP/IP Protocol

<p align="center">
  <img src="http://www.ktword.co.kr/img_data/205_1.JPG" />
</p>

* 인터넷에서 컴퓨터들이 서로 정보를 주고받는 데 쓰이는 통신규약(프로토콜)의 모음이다. 인터넷 프로토콜 슈트 중 TCP와 IP가 가장 많이 쓰이기 때문에 TCP/IP 프로토콜 슈트라고도 불린다.

<p align="center">
  <img src="http://www.ktword.co.kr/img_data/205_2.jpg" />
</p>

###### 📌 4계층 - 응용 계층 (Application Layer)

* 컴퓨터 네트워크 프로그래밍에서 인터넷 프로토콜(IP) 컴퓨터 네트워크를 통하는 프로세스 간 통신 접속을 위해 설계되어 통신 프로토콜과 방식을 위해 보유된 추상 계층이다. 응용 계층 프로토콜은 기반이 되는 전송 계층 프로토콜을 사용하여 호스트 간 연결을 확립한다.

###### 📌 3계층 - TCP/IP 계층 (TCP/IP Layer)

* IP계층에서 선택 된 경로정보를 바탕으로 데이터의 실제 송수신의 역할을 수행하는 계층이다. 서비스 지정 주소지정, 흐름제어, 분할과 재조립, 오류제어, 연결제어와 같은 기능을 수행하며 `Sagment` 단위로 통신을 수행한다.

###### 📌 2계층 - IP 계층 (Internet Protocol Layer)

* 목적지로 데이터를 전송하기 위해서 어떠한 경로를 거쳐야 할지 경로선택 역할을 수행하는 계층이다. 논리주소지정 및 경로지정와 같은 기능을 수행하며 `Datagram` 단위로 통신을 수행한다.

###### 📌 1계층 - LINK 계층 (Link Layer)

* LAN, WAN, MAN과 같은 네트워크 표준과 관련된 프로토콜을 정의하는 영역이다. 프레임 구성, 물리 주소 지성, 흐름제어, 오류제어, 접근제어와 같은 기능을 수행하며 `Frame` 단위로 통신을 주고 받는다.

## 📣 [REST API](https://meetup.toast.com/posts/92)

* REST는 네트워크 아키텍처 원리의 모음이다. 여기서 **'네트워크 아키텍처 원리'란 자원(Image, Video, Data)을 정의하고 자원에 대한 주소를 지정하는 방법 전반**을 일컫는다. 간단한 의미로는, 웹 상의 자료를 HTTP위에서 SOAP이나 쿠키를 통한 세션 트랙킹 같은 별도의 전송 계층 없이 전송하기 위한 아주 간단한 인터페이스를 말한다.

* REST API는 `자원(Resource) - URI`, `행위(Verb) - HTTP METHOD`, `표현(Representations)`으로 구성된다.

<p align="center">
  <img src="https://user-images.githubusercontent.com/20036523/57290221-f1f35580-70f7-11e9-81cd-19931c38f999.png" />
</p>

#### 💊 REST API Purpose

* 구성 요소 상호작용의 규모 확장성(scalability of component interactions)

* 인터페이스의 범용성 (Generality of interfaces)

* 구성 요소의 독립적인 배포(Independent deployment of components)

* 중간적 구성요소를 이용해 응답 지연 감소, 보안을 강화, 레거시 시스템을 인캡슐레이션 (Intermediary components to reduce latency, enforce security and encapsulate legacy systems)

#### 💊 REST API Features

###### 🔑 유니폼 인터페이스 (Uniform) 

* Uniform Interface는 URI로 지정한 리소스에 대한 조작을 통일되고 한정적인 인터페이스로 수행하는 아키텍처 스타일을 말합니다.

###### 🔑 무상태성 (Stateless) 

* REST는 무상태성 성격을 갖습니다. 다시 말해 작업을 위한 상태정보를 따로 저장하고 관리하지 않습니다. 세션 정보나 쿠키정보를 별도로 저장하고 관리하지 않기 때문에 API 서버는 들어오는 요청만을 단순히 처리하면 됩니다. 때문에 서비스의 자유도가 높아지고 서버에서 불필요한 정보를 관리하지 않음으로써 구현이 단순해집니다.

* 각 요청 간 클라이언트의 콘텍스트가 서버에 저장되어서는 안 된다.

###### 🔑 캐시 가능 (Cacheable)

* REST의 가장 큰 특징 중 하나는 HTTP라는 기존 웹표준을 그대로 사용하기 때문에, 웹에서 사용하는 기존 인프라를 그대로 활용이 가능합니다. 따라서 HTTP가 가진 캐싱 기능이 적용 가능합니다. HTTP 프로토콜 표준에서 사용하는 Last-Modified태그나 E-Tag를 이용하면 캐싱 구현이 가능합니다.

* WWW에서와 같이 클라이언트는 응답을 캐싱할 수 있어야 한다. 또한 잘 관리되는 캐싱은 클라이언트-서버 간 상호작용을 부분적으로 또는 완전하게 제거하여 scalability와 성능을 향상시킨다.

###### 🔑 자체 표현 구조 (Self-descriptiveness)

* REST의 또 다른 큰 특징 중 하나는 REST API 메시지만 보고도 이를 쉽게 이해 할 수 있는 자체 표현 구조로 되어 있다는 것입니다.

###### 🔑 Client <---> Server 구조 

* REST 서버는 API 제공, 클라이언트는 사용자 인증이나 컨텍스트(세션, 로그인 정보)등을 직접 관리하는 구조로 각각의 역할이 확실히 구분되기 때문에 클라이언트와 서버에서 개발해야 할 내용이 명확해지고 서로간 의존성이 줄어들게 됩니다.

* 일관적인 인터페이스로 분리되어야 한다.

###### 🔑 계층형 구조

* REST 서버는 다중 계층으로 구성될 수 있으며 보안, 로드 밸런싱, 암호화 계층을 추가해 구조상의 유연성을 둘 수 있고 PROXY, 게이트웨이 같은 네트워크 기반의 중간매체를 사용할 수 있게 합니다.

* 클라이언트는 보통 대상 서버에 직접 연결되었는지, 또는 중간 서버를 통해 연결되었는지를 알 수 없다. 중간 서버는 로드 밸런싱 기능이나 공유 캐시 기능을 제공함으로써 시스템 규모 확장성을 향상시키는 데 유용하다.

#### 💊 REST API Design Caution

* `/`는 계층 관를 나타내는데 사용한다.

* URI 마지막 문자로 `/`를 포함하지 않는다.

* `-`은 URI 가독성을 높이는데 사용한다.

* `_`은 URI에 사용하지 않는다.

* URI 경로에는 소문자가 적합하다.

* 파일 확장자는 URI에 포함시키지 않는다.

## 📣 [멀티캐스트 (Multicast) - UDP](https://ko.wikipedia.org/wiki/%EB%A9%80%ED%8B%B0%EC%BA%90%EC%8A%A4%ED%8A%B8)

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/30/Multicast.svg/250px-Multicast.svg.png" />
</p>

* 인터넷에서 같은 내용의 데이터를 여러 명의 특정한 그룹의 수신자들에게 동시에 전송하는 방식을 말한다. 데이터 중복전송으로 인한 정보체증을 완화하며, 그룹 멤버십 정보를 관리할 수 있다. 즉, 멀티캐스트 전송방식은 데이터 중복전송으로 인한 네트워크 자원낭비를 막고, 그 정보를 필요로 하지 않는 곳에는 부담을 주지 않으면서 실시간 공동작업을 효율적으로 보장하는 전송기법이다.

* 멀티캐스트(Multicast)는 보통 IP 멀티캐스트 형태로 구현되는데, 이는 스트리밍을 위한 인터넷 프로토콜 응용 프로그램(Internet Protocol application) 및 인터넷 텔레비전에서 주로 사용된다. IP 멀티캐스트에서 멀티캐스트는 주로 IP 라우팅 단계에서 구현되며, 이 때 라우터는 데이터그램을 멀티캐스트 대상 주소로 보내기 위한 최적의 전송 경로를 생성한다.

* IP 멀티캐스트(Multicast)는 기업, 증권거래소, 그리고 멀티미디어 컨텐츠 전달 네트워크 등에서 광범위하게 이용된다. 원격 학습이나 원격 화상 회의와 같은 IPTV 응용 프로그램이 일반적으로 기업에서 사용되는 IP 멀티캐스트이다.

## 📣 [유니캐스트 (Unicast) - TCP](https://terms.naver.com/entry.nhn?docId=1207832&cid=40942&categoryId=32851)

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/Unicast.svg/200px-Unicast.svg.png" />
</p>

* 한 사람의 특정 수신자에게만 데이터 패킷을 전송하는 방식. 인터넷에서 전자메일, 화상회의를 위한 화상·음성 데이터 등을 하나의 송신자가 다른 하나의 수신자에게 1:1로 전송하는 방식이다. </br></br>이 전송방식은 데이터를 보내는 송신자측에서 지정된 수신자측의 IP 주소로만 데이터가 전송된다. **즉 여러 수신자가 같은 데이터를 원할 때 송신자는 데이터를 여러 번 복사하여 각각의 수신자의 IP 주소로 전송해야 한다. 따라서 받는 사람의 수만큼 데이터 패킷을 반복해서 보내야 하기 때문에 통신망의 효율을 저하시키고, 제한된 회선용량을 접속자들이 서로 나누어 가져야 한다는 문제점 때문에 전송 부담도 크다.**

* 유니캐스트 메시징은 개인적이거나 고유한 리소스가 필요한 모든 네트워크 프로세스에서 사용될 수 있다.

## 📣 [브로드캐스트 (Broadcast) - UDP](https://upload.wikimedia.org/wikipedia/commons/thumb/d/dc/Broadcast.svg/100px-Broadcast.svg.png)

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/dc/Broadcast.svg/1024px-Broadcast.svg.png" />
</p>

* IP 네트워크에 있는 모든 로컬 네트워크 호스트로 데이터를 전송하는 방식이다. 또한 브로드캐스트(Broadcast)는 두 가지의 방식으로 구분이 된다. 첫번째는 Directed Broadcast 방식으로 네트워크 주소를 제외한 나머지 호스트 주소를 전부 1로 설정하여 얻을 수 있는 방식이다. 두번째는 Local Broadcast 방식으로 255.255.255.255의 특별 예약 주소를 사용하여 IP 주소의 모든 호스트에 데이터를 전달하는 방법이 있다.

## 📣 SOAP

* SOAP(Simple Object Access Protocol)은 일반적으로 널리 알려진 HTTP, HTTPS, SMTP 등을 통해 XML 기반의 메시지를 컴퓨터 네트워크 상에서 교환하는 프로토콜이다. SOAP은 웹 서비스에서 기본적인 메시지를 전달하는 기반이 된다. SOAP에는 몇가지 형태의 메시지 패턴이 있지만, 보통의 경우 원격 프로시져 호출(Remote Procedure Call:RPC) 패턴으로, 네트워크 노드(클라이언트)에서 다른 쪽 노드(서버)쪽으로 메시지를 요청 하고, 서버는 메시지를 즉시 응답하게 된다. SOAP는 XML-RPC와 WDDX에서 envelope/header/body로 이루어진 구조와 전송(transport)과 상호 중립성(interaction neutrality)의 개념을 가져왔다.

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/59/SOAP.svg/220px-SOAP.svg.png" />
</p>

* SOAP은 XML을 근간으로 헤더와 바디를 조합하는 디자인 패턴으로 설계되어 있다. 「헤더」는 선택사항으로 반복이나 보안 및 트랜잭션을 정보로 하는 메타 정보를 가지고 있다. 「바디」부분은 주요한 정보인 정보를 가지고 있다.

## 📣 Sliding Window
두 개의 네트워크 호스트간의 패킷의 흐름을 제어하기 위한 방법이다. (슬라이딩 윈도우 방식 = 연속적 ARQ(Continuous ARQ) = Go Back n ARQ)

<p align="center">
  <img src="https://images.slideplayer.com/33/8175417/slides/slide_4.jpg" />
</p>

* TCP와 같이 데이터의 전달을 보증하는 프로토콜에서는 패킷 하나 하나가 정상적으로 전달되었음을 알리는 확인 신호(acknowledgement, 이하 ACK)를 받아야하며, 만약 패킷이 중도에 잘못되었거나 분실되어 확인받지 못하는 경우, 해당 패킷을 재전송해야하는 필요가 있다. 슬라이딩 윈도는 일단 '윈도(메모리 버퍼의 일정 영역)'에 포함되는 모든 패킷을 전송하고, 그 패킷들의 전달이 확인되는대로 이 윈도를 옆으로 옮김(slide)으로서 그 다음 패킷들을 전송하는 방식이다. 

* 슬라이딩 윈도는 아직 확인을 받지 않고도 여러 패킷을 보내는 것을 가능케 하기 때문에, 매번 전송한 패킷에 대해 확인을 받아야만 그 다음 패킷을 전송하는 방법(stop-and-wait)을 사용하는 것보다 훨씬 네트워크를 효율적으로 사용할 수 있다.

* 흐름제어를 위한 검출후 재전송 방식(ARQ)의 일종 (혼잡제어도 가능)

## 📣 Selective Repeat ARQ

<p align="center">
  <img src="http://www.oocities.org/siliconvalley/pines/1572/images/image9.gif" />
</p>

Selective Repeat is part of the automatic repeat-request (ARQ). With selective repeat, the sender sends a number of frames specified by a window size even without the need to wait for individual ACK from the receiver as in Go-Back-N ARQ. The receiver may selectively reject a single frame, which may be retransmitted alone; this contrasts with other forms of ARQ, which must send every frame from that point again. The receiver accepts out-of-order frames and buffers them. The sender individually retransmits frames that have timed out.

## 📣 암호화 알고리즘 (Security Algorithms)

* 원문과 암호화 키를 입력으로 하여 암호화된 데이터를 출력으로 생성하는 알고리즘이다.

##### 📌 암호화 알고리즘의 종류 (Security Algorithms Types)

* MD5 - 무선 클라이언트와 네트워크에 대한 상호 인증 단계가 없는 단 방향 인증만을 제공한다.

* TLS - 클라이언트와 AP 사이에 보안강화를 위하여 WEP키 및 세션 기반 WEP키를 동적으로 생선한다.

* TTLS - 암호화된 채널을 통하여 클라이언트와 네트워크에 대한 인증서 기반 상호 인증 방법을 제공한다.

* PEAP - PEAT 클아이언트와 인증서버 간 터널링을 사용하여 기능을 수행한다.

* LEAP - 동적으로 생성된 WEP키를 사용하여 전송 데이터를 암호화하며 상호 인증을 지원한다.

## ★ REFERENCE

:airplane: [NETWORK REFERENCE URL](https://github.com/ChangYeop-Yang/Study-ComputerScience/issues/5)
