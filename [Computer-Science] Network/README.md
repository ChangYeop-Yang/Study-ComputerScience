# Study - NETWORK <kbd>[Kyungpook National University](http://www.knu.ac.kr/wbbs/)</kbd>

## ★ OSI 7 Layer
OSI 모형(Open Systems Interconnection Reference Model)은 국제표준화기구(ISO)에서 개발한 모델로, 컴퓨터 네트워크 프로토콜 디자인과 통신을 계층으로 나누어 설명한 것이다. 일반적으로 OSI 7 계층 모형이라고 한다.

<p align="center">
  <img src="https://t1.daumcdn.net/cfile/tistory/99B9493359B6408E23" />
</p>

* * *

#### * 7계층 – 응용 계층(Application)
디핑 소스 비유를 확장하면 응용 계층은 가장 위에 있다. 사용자에게 보이는 부분이다. OSI 모형에서는 “최종 사용자에게 가장 가까운” 계층이다. **7층에서 작동하는 응용프로그램은 사용자와 직접적으로 상호작용한다.** 구글 크롬(Google Chrome), 파이어폭스(Firefox), 사파리(Safari) 등 웹 브라우저와 스카이프(Skype), 아웃룩(Outlook), 오피스(Office) 등의 응용 프로그램이 대표적이다.

* * *

#### * 6계층 – 표현 계층(Presentation)
표현 계층은 응용 계층의 데이터 표현에서 독립적인 부분을 나타낸다. 일반적으로 **응용프로그램 형식을 준비 또는 네트워크 형식으로 변환하거나 네트워크 형식을 응용프로그램 형식으로 변환하는 것을 나타낸다.** 다시 말해 이 계층은 **응용프로그램이나 네트워크를 위해 데이터를 “표현”하는 것이다.** 대표적인 예로는 데이터를 안전하게 전송하기 위해 암호화, 복호화하는 것인데, 이 작업이 바로 6계층에서 처리된다.

* * *

#### * 5계층 – 세션 계층(Session)
2대의 기기, 컴퓨터 또는 서버 간에 “대화”가 필요하면 세션(session)을 만들어야 하는데 이 작업이 여기서 처리된다. 이 계층에는 **설정, 조율(예: 시스템의 응답 대기 기간), 세션 마지막에 응용프로그램 간의 종료 등의 기능**이 필요하다.

* * *

#### * 4계층 – 전송 계층(Transport)
전송 계층은 **최종 시스템 및 호스트 간의 데이터 전송 조율을 담당**한다. **보낼 데이터의 용량과 속도, 목적지 등을 처리**한다. 전송 계층의 예 중에서 가장 잘 알려진 것이 전송 제어 프로토콜(TCP)이다. TCP는 인터넷 프로토콜(IP) 위에 구축되는데 흔히 TCP/IP로 알려져 있다. 기기의 IP 주소가 여기서 작동한다.

* * *

#### * 3계층 – 네트워크 계층(Network)
네트워킹 전문가 대부분이 관심을 두고 좋아하는 라우터 기능 대부분이 여기 네트워크 계층에 자리잡는다. 가장 기본적으로 볼 때 이 계층은 **다른 여러 라우터를 통한 라우팅을 비롯한 패킷 전달을 담당한다.** 보스턴에 있는 컴퓨터가 캘리포니아에 있는 서버에 연결하려고 할 때 그 경로는 수백 만 가지다. 이 계층의 라우터가 이 작업을 효율적으로 처리한다.

* * *

#### * 2계층 – 데이터 링크 계층(Data Link)
**데이터 링크 계층은 (두 개의 직접 연결된 노드 사이의) 노드 간 데이터 전송을 제공하며 물리 계층의 오류 수정도 처리한다.** 여기에는 2개의 부계층도 존재한다. 하나는 매체 접근 제어(MAC) 계층이고 다른 하나는 논리적 연결 제어(LLC) 계층이다. 네트워킹 세계에서 대부분 스위치는 2계층에서 작동한다. 

* * *

#### * 1계층 – 물리 계층(Physical)
OSI 디핑 소스의 밑바닥에는 물리 계층이 있다. **시스템의 전기적, 물리적 표현을 나타낸다.** 케이블 종류, (802.11 무선 시스템에서와 같은) 무선 주파수 링크는 물론 핀 배치, 전압, 물리 요건 등이 포함된다. 네트워킹 문제가 발생하면 많은 네트워크 전문가가 물리 계층으로 바로 가서 모든 케이블이 제대로 연결돼 있는지, 라우터나 스위치 또는 컴퓨터에서 전원 플러그가 빠지지 않았는지 확인한다. 

* * *

### ※ OSI 7 Layer Purpose
이 모델은 프로토콜을 기능별로 나눈 것이다. 각 계층은 하위 계층의 기능만을 이용하고, 상위 계층에게 기능을 제공한다. '프로토콜 스택' 혹은 '스택'은 이러한 계층들로 구성되는 프로토콜 시스템이 구현된 시스템을 가리키는데, 프로토콜 스택은 하드웨어나 소프트웨어 혹은 둘의 혼합으로 구현될 수 있다. 일반적으로 하위 계층들은 하드웨어로, 상위 계층들은 소프트웨어로 구현된다.

## ★ RESTful API
REST는 네트워크 아키텍처 원리의 모음이다. 여기서 **'네트워크 아키텍처 원리'란 자원(Image, Video, Data)을 정의하고 자원에 대한 주소를 지정하는 방법 전반**을 일컫는다. 간단한 의미로는, 웹 상의 자료를 HTTP위에서 SOAP이나 쿠키를 통한 세션 트랙킹 같은 별도의 전송 계층 없이 전송하기 위한 아주 간단한 인터페이스를 말한다.

#### # RESTful API Purpose
* 구성 요소 상호작용의 규모 확장성(scalability of component interactions)
* 인터페이스의 범용성 (Generality of interfaces)
* 구성 요소의 독립적인 배포(Independent deployment of components)
* 중간적 구성요소를 이용해 응답 지연 감소, 보안을 강화, 레거시 시스템을 인캡슐레이션 (Intermediary components to reduce latency, enforce security and encapsulate legacy systems)

## ★ SOAP
SOAP(Simple Object Access Protocol)은 일반적으로 널리 알려진 HTTP, HTTPS, SMTP 등을 통해 XML 기반의 메시지를 컴퓨터 네트워크 상에서 교환하는 프로토콜이다. SOAP은 웹 서비스에서 기본적인 메시지를 전달하는 기반이 된다. SOAP에는 몇가지 형태의 메시지 패턴이 있지만, 보통의 경우 원격 프로시져 호출(Remote Procedure Call:RPC) 패턴으로, 네트워크 노드(클라이언트)에서 다른 쪽 노드(서버)쪽으로 메시지를 요청 하고, 서버는 메시지를 즉시 응답하게 된다. SOAP는 XML-RPC와 WDDX에서 envelope/header/body로 이루어진 구조와 전송(transport)과 상호 중립성(interaction neutrality)의 개념을 가져왔다.

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/59/SOAP.svg/220px-SOAP.svg.png" />
</p>

* SOAP은 XML을 근간으로 헤더와 바디를 조합하는 디자인 패턴으로 설계되어 있다. 「헤더」는 선택사항으로 반복이나 보안 및 트랜잭션을 정보로 하는 메타 정보를 가지고 있다. 「바디」부분은 주요한 정보인 정보를 가지고 있다.

## ★ Sliding Window
두 개의 네트워크 호스트간의 패킷의 흐름을 제어하기 위한 방법이다. (슬라이딩 윈도우 방식 = 연속적 ARQ(Continuous ARQ) = Go Back n ARQ)

<p align="center">
  <img src="https://images.slideplayer.com/33/8175417/slides/slide_4.jpg" />
</p>

* TCP와 같이 데이터의 전달을 보증하는 프로토콜에서는 패킷 하나 하나가 정상적으로 전달되었음을 알리는 확인 신호(acknowledgement, 이하 ACK)를 받아야하며, 만약 패킷이 중도에 잘못되었거나 분실되어 확인받지 못하는 경우, 해당 패킷을 재전송해야하는 필요가 있다. 슬라이딩 윈도는 일단 '윈도(메모리 버퍼의 일정 영역)'에 포함되는 모든 패킷을 전송하고, 그 패킷들의 전달이 확인되는대로 이 윈도를 옆으로 옮김(slide)으로서 그 다음 패킷들을 전송하는 방식이다. 

* 슬라이딩 윈도는 아직 확인을 받지 않고도 여러 패킷을 보내는 것을 가능케 하기 때문에, 매번 전송한 패킷에 대해 확인을 받아야만 그 다음 패킷을 전송하는 방법(stop-and-wait)을 사용하는 것보다 훨씬 네트워크를 효율적으로 사용할 수 있다.

* 흐름제어를 위한 검출후 재전송 방식(ARQ)의 일종 (혼잡제어도 가능)

## ★ Selective Repeat ARQ

<p align="center">
  <img src="http://www.oocities.org/siliconvalley/pines/1572/images/image9.gif" />
</p>

Selective Repeat is part of the automatic repeat-request (ARQ). With selective repeat, the sender sends a number of frames specified by a window size even without the need to wait for individual ACK from the receiver as in Go-Back-N ARQ. The receiver may selectively reject a single frame, which may be retransmitted alone; this contrasts with other forms of ARQ, which must send every frame from that point again. The receiver accepts out-of-order frames and buffers them. The sender individually retransmits frames that have timed out.

## ★ REFERENCE
* [REST - 위키백과](https://ko.wikipedia.org/wiki/REST)
* [OSI 모형 - 위키백과](https://ko.wikipedia.org/wiki/OSI_%EB%AA%A8%ED%98%95)
* [네트워크의 기본 'OSI 7계층'··· 한번에 이해하고 외우는 방법](http://www.ciokorea.com/news/36536#csidxc5d64590057e2ba9a875e48a4a11a61)
* [OSI 7 계층 (OSI 7 Layer) 과 TCP/IP 4 계층 (TCP/IP 4 Layer) - Blog](http://jaeri.tistory.com/2)
* [슬라이딩 윈도 - 위키백과](https://ko.wikipedia.org/wiki/%EC%8A%AC%EB%9D%BC%EC%9D%B4%EB%94%A9_%EC%9C%88%EB%8F%84)
* [GBN - 정보통신기술용어해설](http://www.ktword.co.kr/abbr_view.php?m_temp1=1469)
* [Error Control - SlidePlayer](https://slideplayer.com/slide/8175417/)
