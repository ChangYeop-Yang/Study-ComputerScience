# 운영체제 (Operating System)

## ★ 운영체제의 정의
* 하드웨어를 제어하는 소프트웨어이다.
* 컴퓨터 본체 및 각 주변 장치를 가장 능률적이고, 경제적으로 사용할 수 있도록 하는 프로그램이다.
* 컴퓨터 자원들인 프로세서, 기억 장치, 파일 및 정보, 네트워크 및 보호 등을 효율적으로 관리할 수 있는 프로그램의 집합이다.

|IMAGE 1|IMAGE 2|
|:-----:|:-----:|
|<img src="https://user-images.githubusercontent.com/20036523/44776102-3e25e780-abb2-11e8-9020-004eb6c08078.png" width="250" height="250">|<img src=https://user-images.githubusercontent.com/20036523/44776115-441bc880-abb2-11e8-9ccf-79ed7f0f7476.png width="250" height="250">|

## ★ 운영체제의 목적
* 컴퓨터 시스템의 처리량, 신뢰성을 최대화한다.
* 컴퓨터 시스템의 반환 시간, 응답 시간, 처리 시간, 대기 시간, 경과 시간을 최소화한다.
* 운영체제는 스스로 어떤 기능도 수행하지 않고 다른 응용 프로그램이 유용한 작업을 할 수 있도록 환경을 마련하여 준다.
* 프로세서, 입출력 장치를 관리한다.

* * *

> **※ 운영체제의 성능 평가 기준 4가지**
> 1) 처리량 (Throughput): 일정한 시간(단위 시간) 내에서 얼마나 많은 작업량을 처리할 수 있는가의 기준이다. 처리량이 극대화되어야 성능 좋은 컴퓨터 시스템이라 할 수 있다.
> 2) 반환 시간 (Turn-around Time): 요청한 작업에 대하여 그 결과를 사용자에게 되돌려 줄 때까지 소요되는 시간이다. 반환 시간이 최소화되어야 성능 좋은 컴퓨터 시스템이라 할 수 있다. 특히 반환 시간 안에 포함된 응답 시간은 대화형 시스템에서 가장 중요한 기준이 된다.
> 3) 신뢰도 (Reliability): 작업의 결과가 얼마나 정확하고 믿을 수 있는가의 기준인다. 처리량이 높은 시스템이라도 처리 결과에 오류가 많다면 좋은 성능의 시스템이라고 할 수 없다. 따라서 신뢰도가 높을수록 성능 좋은 컴퓨터 시스템이라 할 수 있다.
> 4) 사용 가능도 (Availability): 컴퓨터 시스템 내의 한정된 각종 자원을 여러 사용자가 요구할 때, 어느 정도 신속하고 충분하게 지원해 줄 수 있는지의 정도이다. 이는 사용 가능한 하드웨어 자원의 수나 다중 프로그래밍 정도 등의 요소가 좌우하는 것으로 같은 종류의 시스템 자원수가 많은 경우에는 이것이 높아질 수 있다.

## ★ 로더(Loader)의 역할
* 목적 프로그램(기계어로 구성 된 파일)을 실행 가능한 파일로 변환하기 위해 주기억 장소를 할당하거나, 여러개의 프로그램을 연계 편집하여 CPU가 처리될 수 있는 프로그램으로 변환한다.
* 일반적으로 로더는 프로그램을 실행하기 위하여 프로그램을 보조 기억 장치로부터 컴퓨터의 주기억 장치에 올려놓은 기능을 가진 프로그램으로 **할당->연결->재배치->적재**의 순서로 진행된다.

# 프로세스(Process)

* 파일로 작성 된 프록램은 로더(Loader)에 의해 주기억 장치에 상주되어 CPU에 의해서 처리된다. 이때 주기억 장치에 상주된 프로그램이 CPU에 의해서 처리되는 상태를 프로세스라고 한다.
* CPU에 의해서 현재 실행되고 있는 프로그램이다.
* 비동기적 행위를 일으키는 주체이며 프로시저가 활동 중인 상태이다.
* 운영체제가 관리하는 최소 단위의 작업(프로그램)이다.

* * *

> **PCB (Process Control Block)**
> * 프로세스 제어 블록(Process Control Block, 줄여서 PCB)은 특정한 프로세스를 관리할 필요가 있는 정보를 포함하는 운영 체제 커널의 자료 구조이다. 작업 제어 블록(Task Control Block, 줄여서 TCB) 또는 작업 구조라고도 한다. "PCB는 운영 체제가 프로세스를 표현한 것이다."
> * PCB가 프로세스의 중요한 정보를 포함하고 있기 때문에, 일반 사용자가 접근하지 못하도록 보호된 메모리 영역 안에 남는다. 일부 운영 체제에서 PCB는 커널 스택의 처음에 위치한다. (이 메모리 영역은 편리하면서도 보호를 받는 위치이기 때문이다.)

## ★ 프로세스의 상태 (Process Status)

* In a multitasking computer system, processes may occupy a variety of states. These distinct states may not be recognized as such by the operating system kernel. However, they are a useful abstraction for the understanding of processes.

<p align=center>

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Process_states.svg/400px-Process_states.svg.png">

</p>

**1. 준비(Ready) 상태**
* 프로세스가 처리기(CPU)를 사용하고 있지는 않지만 언제든 사용할 수 있는 상태이다.
* 프로세스가 처리기의 배정을 기다리고 있는 상태이다.
* 다른 프로세스 실행을 위해서 일시적으로 정지해 있는 상태이다.
* CPU에 의해 처리되기 위해 주 기억장치에 존재하는 상태이다.

**2. 실행(Run) 상태**
* 프로세스가 CPU를 차지하고 있는 상태이다.
* 프로세스의 명령이 실행되고 있는 상태이다.

**3. 대기(Block, Wait) 상태**
* 프로세스가 어떤 사건이 일어나기를 기다리고 있는 상태이다.
* 처리 속도가 느린 I/O 작업 중인 상태이다.
* 외부적인 사건이 생길 때까지 실행할 수 없는 상태이다.

* * *

> **＃ Additional process states (추가적인 프로세스 상태)**
> * Two additional states are available for processes in systems that support virtual memory. In both of these states, processes are "stored" on secondary memory (typically a hard disk).
> * **Swapped out and waiting** : (Also called suspended and waiting.) In systems that support virtual memory, a process may be swapped out, that is, removed from main memory and placed on external storage by the scheduler. From here the process may be swapped back into the waiting state.
> * **Swapped out and blocked** : (Also called suspended and blocked.) Processes that are blocked may also be swapped out. In this event the process is both swapped out and blocked, and may be swapped back in again under the same circumstances as a swapped out and waiting process (although in this case, the process will move to the blocked state, and may still be waiting for a resource to become available).

## ★ 교착상태 (DeadLock)
* 교착 상태(膠着狀態, 영어: deadlock)란 두 개 이상의 작업이 서로 상대방의 작업이 끝나기 만을 기다리고 있기 때문에 결과적으로 아무것도 완료되지 못하는 상태를 가리킨다. 예를 들어 하나의 사다리가 있고, 두 명의 사람이 각각 사다리의 위쪽과 아래쪽에 있다고 가정한다. 이때 아래에 있는 사람은 위로 올라 가려고 하고, 위에 있는 사람은 아래로 내려오려고 한다면, 두 사람은 서로 상대방이 사다리에서 비켜줄 때까지 하염없이 기다리고 있을 것이고 결과적으로 아무도 사다리를 내려오거나 올라가지 못하게 되듯이, 전산학에서 교착 상태란 다중 프로그래밍 환경에서 흔히 발생할 수 있는 문제이다. 이 문제를 해결하는 일반적인 방법은 아직 없는 상태이다.

* * *

> **＃ 교착상태의 조건**
> 1. 상호배제(Mutual exclusion) : 프로세스들이 필요로 하는 자원에 대해 배타적인 통제권을 요구한다.
> 2. 점유대기(Hold and wait) : 프로세스가 할당된 자원을 가진 상태에서 다른 자원을 기다린다.
> 3. 비선점(No preemption) : 프로세스가 어떤 자원의 사용을 끝낼 때까지 그 자원을 뺏을 수 없다.
> 4. 순환대기(Circular wait) : 각 프로세스는 순환적으로 다음 프로세스가 요구하는 자원을 가지고 있다.

### ※ 교착상태의 관리 

> **＃ 교착상태 예방**
> 1. 상호배제 조건의 제거 : 교착 상태는 두 개 이상의 프로세스가 공유가능한 자원을 사용할 때 발생하는 것이므로 공유 불가능한, 즉 상호 배제 조건을 제거하면 교착 상태를 해결할 수 있다.
> 2. 점유와 대기 조건의 제거 : 한 프로세스에 수행되기 전에 모든 자원을 할당시키고 나서 점유하지 않을 때에는 다른 프로세스가 자원을 요구하도록 하는 방법이다. 자원 과다 사용으로 인한 효율성, 프로세스가 요구하는 자원을 파악하는 데에 대한 비용, 자원에 대한 내용을 저장 및 복원하기 위한 비용, 기아 상태, 무한대기 등의 문제점이 있다.
> 3. 비선점 조건의 제거 : 비선점 프로세스에 대해 선점 가능한 프로토콜을 만들어 준다.
> 4. 환형 대기 조건의 제거 : 자원 유형에 따라 순서를 매긴다.

* * *

> **＃ 교착상태 회피** <br>
> 자원이 어떻게 요청될지에 대한 추가정보를 제공하도록 요구하는 것으로 시스템에 circular wait가 발생하지 않도록 자원 할당 상태를 검사한다.
> 1. 자원 할당 그래프 알고리즘 (Resource Allocation Graph Algorithm)
> 2. 은행원 알고리즘 (Banker's algorithm)

* * *

> **＃ 교착상태 무시** <br>
> 예방 혹은 회피기법을 프로그래밍해서 넣으면 성능에 큰 영향을 미칠 수 있게 된다. 그렇기 때문에 데드락의 발생 확률이 비교적 낮은 경우 별다른 조치를 취하지 않는다.

* * *

> **＃ 교착상태 발견** <br>
감시/발견을 하는 detection 알고리즘으로 Deadlock 발생을 체크하는 방식. 이 역시 성능에 큰 영향을 미칠 수 있다.

## ★ 인터럽트 (Interupt)
* 프로세스가 수행 중에 다른 프로세스를 수행하기 위하여 현재 수행 중인 프로세스를 중단하거나 외부 입력 장치에 의해 프로세스가 중단되는 상태이다. 인터럽트는 어떤 이유에서든 H/W적, S/W적으로 현재 프로세스를 중단시키는 모든 행위라고 할 수 있다.

<p align=center>

<img src="http://www.jidum.com/upload/ckeditor/2016/09/20160908134022750.png">

</p>

# ★ 문맥교환 (Context Switching)
* 다중 프로그래밍 시스템에서 CPU가 할당되는 프로세스를 변경하기 위하여 현재 CPU를 사용하여 실행되고 있는 프로세서의 상태 정보를 저장하고 제어권을 인터럽트 서비스 루틴(ISR)에게 넘기는 작업을 말한다.

* 문맥 교환(Context Switch)이란 하나의 프로세스가 CPU를 사용 중인 상태에서 다른 프로세스가 CPU를 사용하도록 하기 위해, 이전의 프로세스의 상태(문맥)를 보관하고 새로운 프로세스의 상태를 적재하는 작업을 말한다. 한 프로세스의 문맥은 그 프로세스의 프로세스 제어 블록에 기록되어 있다.

<p align=center>

<img src="https://upload.wikimedia.org/wikipedia/commons/0/04/Context_switch.png">

</p>

* 문맥교환의 시점으로는 **멀티 태스킹, 인터럽트 핸들링, 사용자 모드와 커널 모드 간 전환**이다.

> ＃ 문맥 교환과 인터럽트
> CPU는 하나의 프로세스 정보만을 기억한다. 여러 개의 프로세스가 실행되는 다중 프로그래밍 환경에서 CPU는 각각의 프로세스의 정보를 저장했다 복귀하고 다시 저장했다 복귀하는 일을 반복한다. 프로세스의 저장과 복귀는 프로세스의 중단과 실행을 의미한다. 프로세스의 중단과 실행 시 인터럽트가 발생하므로, 문맥 교환이 많이 일어난다는 것은 인터럽트가 많이 발생한다는 것이다.

> ＃ 문맥 교환과 시간 할당량
> 프로세스들 시간 할당량은 시스템 성능의 중요한 역할을 한다. 시간 할당량이 적을수록 사용자 입장에서는 여러 개의 프로세스가 거의 동시에 수행되는 느낌을 갖지만 인터럽트의 수와 문맥 교환의 수가 늘어난다. 프로세스의 실행을 위한 부가적인 활동을 오버헤드(간접 부담 비용)이라고 하는데, 이 또한 문맥 교환 수와 같이 늘어나게 된다.
> * 시간 할당량이 적어지면 문맥 교환 수, 인터럽트 횟수, 오버헤드가 증가하지만 여러 개의 프로세스가 동시에 수행되는 느낌을 갖는다.
> * 시간 할당량이 커지면 문맥 교환 수, 인터럽트 횟수, 오버헤드가 감소하지만 여러 개의 프로세스가 동시에 수행되는 느낌을 갖지 못한다.

## ★ 용어 정리
* 프로시저(Procedure): 루틴, 서브루틴, 함수와 같은 뜻으로 사용되며 하나의 프로시저는 특정 작업을 수행하기 위한 프로그램의 일부이다. 또는 **어떤 행동을 수행하기 위한 일련의 작업 순서**를 말한다.

* 스풀(Spool): 프로그램과 이를 이용하는 I/O(입출력) 장치와의 속도 차를 극복하기 위한 장치로 대부분 하드 디스크가 중재한다.

* 버퍼링(Buffering): CPU와 입출력 장치와의 속도 차이를 줄이기 위해 메모리가 중재한다. 버퍼링은 한 레코드를 읽어서 CPU가 그것에 대한 작업을 시작함과 동시에 입출력 장치가 필요한 레코드를 미리 읽어 CPU에 저장해 두고 CPU가 필요한 레코드를 읽기 위해 기다리는 일이 없도록 한다.

## ★ REFERENCE
1. [2018 정보처리기사 필기 기본서 - NaverBook](https://book.naver.com/bookdb/book_detail.nhn?bid=12696851)
2. [당신을 블로깅하세요. - 운영체제](http://dongbo.tistory.com/21)
3. [jiransnc님의블로그 - 네이버 ](https://m.blog.naver.com/PostView.nhnblogId=jiransnc&logNo=60195780909&proxyReferer=https%3A%2F%2Fwww.google.co.kr%2F)
4. [프로세스 제어 블록 - 위키백과](https://ko.wikipedia.org/wiki/%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4_%EC%A0%9C%EC%96%B4_%EB%B8%94%EB%A1%9D)
5. [텀즈 - Procedure](http://www.terms.co.kr/procedure.htm)
6. [Process state - 위키백과](https://en.wikipedia.org/wiki/Process_state)
7. [인터럽트 - iLiFO 지덤](http://www.jidum.com/jidums/view.do?jidumId=445)
8. [문맥 교환(Context Switch) - 위키백과](https://ko.wikipedia.org/wiki/%EB%AC%B8%EB%A7%A5_%EA%B5%90%ED%99%98)
