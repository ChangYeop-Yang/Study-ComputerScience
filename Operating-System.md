# ■ 운영체제 (Operating System, 運營 體制)

<p align="center">
  <img src=https://user-images.githubusercontent.com/20036523/44776115-441bc880-abb2-11e8-9ccf-79ed7f0f7476.png />
</p>

* 하드웨어를 제어하는 소프트웨어이다.

* 컴퓨터 본체 및 각 주변 장치를 가장 능률적이고, 경제적으로 사용할 수 있도록 하는 프로그램이다.

* 컴퓨터 자원들인 프로세서, 기억 장치, 파일 및 정보, 네트워크 및 보호 등을 효율적으로 관리할 수 있는 프로그램의 집합이다.

* **시스템 하드웨어를 관리할 뿐 아니라 응용 소프트웨어를 실행하기 위하여 하드웨어 추상화 플랫폼과 공통 시스템 서비스를 제공하는 시스템 소프트웨어이다.**

* 입출력과 메모리 할당과 같은 하드웨어 기능의 경우 운영 체제는 응용 프로그램과 컴퓨터 하드웨어 사이의 중재 역할을 한다.

* 운영 체제는 실행되는 응용 프로그램들이 메모리와 CPU, 입출력 장치 등의 자원들을 사용할 수 있도록 만들어 주고, 이들을 추상화하여 파일 시스템 등의 서비스를 제공한다. 또한 멀티태스킹을 지원하는 경우, 여러 개의 응용 프로그램을 실행하고 있는 동안, 운영 체제는 이러한 모든 프로세스들을 스케줄링하여 마치 그들이 동시에 수행되는 것처럼 보이는 효과를 낸다.

## :mega: 운영체제의 목적 (Operating System Goal)

* 컴퓨터 시스템의 처리량, 신뢰성을 최대화한다.

* 컴퓨터 시스템의 반환 시간, 응답 시간, 처리 시간, 대기 시간, 경과 시간을 최소화한다.

* 운영체제는 스스로 어떤 기능도 수행하지 않고 다른 응용 프로그램이 유용한 작업을 할 수 있도록 환경을 마련하여 준다.

* 프로세서, 입출력 장치를 관리한다.

##### :key: 운영체제의 성능 평가 기준 4가지

* 처리량 (Throughput) - **일정한 시간(단위 시간) 내에서 얼마나 많은 작업량을 처리할 수 있는가의 기준**이다. **처리량이 극대화**되어야 성능 좋은 컴퓨터 시스템이라 할 수 있다.

* 반환 시간 (Turn-around Time) - **요청한 작업에 대하여 그 결과를 사용자에게 되돌려 줄 때까지 소요되는 시간이다.** **반환 시간이 최소화되어야 성능 좋은 컴퓨터 시스템**이라 할 수 있다. 특히 반환 시간 안에 포함된 응답 시간은 대화형 시스템에서 가장 중요한 기준이 된다.

* 신뢰도 (Reliability) - **작업의 결과가 얼마나 정확하고 믿을 수 있는가의 기준이다.** 처리량이 높은 시스템이라도 처리 결과에 오류가 많다면 좋은 성능의 시스템이라고 할 수 없다. 따라서 **신뢰도가 높을수록 성능 좋은 컴퓨터 시스템**이라 할 수 있다.

* 사용 가능도 (Availability) - **컴퓨터 시스템 내의 한정된 각종 자원을 여러 사용자가 요구할 때, 어느 정도 신속하고 충분하게 지원해 줄 수 있는지의 정도**이다. 이는 사용 가능한 하드웨어 자원의 수나 다중 프로그래밍 정도 등의 요소가 좌우하는 것으로 같은 종류의 시스템 자원수가 많은 경우에는 이것이 높아질 수 있다.

## ★ 로더(Loader)의 역할
* 목적 프로그램(기계어로 구성 된 파일)을 실행 가능한 파일로 변환하기 위해 주기억 장소를 할당하거나, 여러개의 프로그램을 연계 편집하여 CPU가 처리될 수 있는 프로그램으로 변환한다. (**할당->연결->재배치->적재**)

* 로더(loader)는 컴퓨터 운영 체제의 일부분으로, 하드디스크와 같은 오프라인 저장 장치에 있는 특정 프로그램을 - 대부분의 경우 응용 프로그램이지만, 경우에 따라서는 운영 체제 그 자신의 일부가 될 수도 있다 - 찾아서 주기억장치에 적재하고, 그 프로그램이 실행되도록 하는 역할을 담당한다. 또한 적재되는 프로그램은 그 자체에 초기에는 주기억장치에 적재되지 않지만, 필요할 때 적재될 수 있는 요소들을 포함할 수 있다. 멀티태스킹이 지원되는 운영 체제에서, 디스패처(dispatcher)라는 프로그램은 서로 다른 태스크들 간에 컴퓨터 CPU의 할당시간을 조절하고, 특정 태스크와 관련된 프로그램이 주기억장치에 있지 않을 때에는 로더를 호출한다.

# 프로세스(Process)

* 프로세스(process)는 컴퓨터에서 연속적으로 실행되고 있는 컴퓨터 프로그램을 말한다. 종종 스케줄링의 대상이 되는 작업(task)이라는 용어와 거의 같은 의미로 쓰인다. 여러 개의 프로세서를 사용하는 것을 멀티프로세싱이라고 하며 같은 시간에 여러 개의 프로그램을 띄우는 시분할 방식을 멀티태스킹이라고 한다. 프로세스 관리는 운영 체제의 중요한 부분이 되었다.

* 프로그램은 일반적으로 하드 디스크 등에 저장되어 있는 실행코드를 뜻하고, 프로세스는 프로그램을 구동하여 프로그램 자체와 프로그램의 상태가 메모리 상에서 실행되는 작업 단위를 지칭한다. 예를 들어, 하나의 프로그램을 여러 번 구동하면 여러 개의 프로세스가 메모리 상에서 실행된다.

* A process is a set of activities that interact to achieve a result.

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

## ★ 문맥교환 (Context Switching)
* In computing, a context switch is the process of storing the state of a process or of a thread, so that it can be restored and execution resumed from the same point later. This allows multiple processes to share a single CPU, and is an essential feature of a multitasking operating system.

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

## ★ [Stack memory vs Heap memory](https://www.gribblelab.org/CBootCamp/7_Memory_Stack_vs_Heap.html)

<p align="center">
  <img src="https://techdifferences.com/wp-content/uploads/2017/10/Untitled-6.jpg" />
</p>

###### ※ Key Differences Between Stack and Heap

* In a stack, the allocation and deallocation is done by CPU and is automatic whereas, in heap, it needs to be done by the programmer manually.
* Heap frame handling is costlier than stack frame handling.
* Implementation of a stack is complex. As against, implementation of a heap is simple.
* A function call in stack takes O(N) time. In contrast, it takes O(1) time in a heap.
* Stack implementation mainly suffers from the memory shortage problem. On the contrary, the main issue in a heap is fragmentation.
* Access to a stack frame is easier than the heap as the stack is confined to the small region of memory and it always hit the cache, but heap frames are dispersed throughout the memory so the memory accessing can cause more cache misses.
Stack is not flexible, the memory size allotted cannot be changed. On the other hand, a heap is flexible, and the allotted memory can be altered.
* A heap takes more accessing time than a stack.

* * *

###### ※ Stack Pros and Cons

* very fast access
* don't have to explicitly de-allocate variables
* space is managed efficiently by CPU, memory will not become fragmented
* local variables only
* limit on stack size (OS-dependent)
* variables cannot be resized

###### ※ Heap Pros and Cons

* variables can be accessed globally
* no limit on memory size
* (relatively) slower access
* no guaranteed efficient use of space, memory may become fragmented over time as blocks of memory are allocated, then freed
* you must manage memory (you're in charge of allocating and freeing variables)
* variables can be resized using realloc()

## ★ 용어 정리
* 프로시저(Procedure): 루틴, 서브루틴, 함수와 같은 뜻으로 사용되며 하나의 프로시저는 특정 작업을 수행하기 위한 프로그램의 일부이다. 또는 **어떤 행동을 수행하기 위한 일련의 작업 순서**를 말한다.

* 스풀(Spool): 프로그램과 이를 이용하는 I/O(입출력) 장치와의 속도 차를 극복하기 위한 장치로 대부분 하드 디스크가 중재한다.

* 버퍼링(Buffering): CPU와 입출력 장치와의 속도 차이를 줄이기 위해 메모리가 중재한다. 버퍼링은 한 레코드를 읽어서 CPU가 그것에 대한 작업을 시작함과 동시에 입출력 장치가 필요한 레코드를 미리 읽어 CPU에 저장해 두고 CPU가 필요한 레코드를 읽기 위해 기다리는 일이 없도록 한다.

* 임계구역(Critical Section): 임계 구역(critical section) 또는 공유변수 영역은 병렬컴퓨팅에서 둘 이상의 스레드가 동시에 접근해서는 안되는 공유 자원(자료 구조 또는 장치)을 접근하는 코드의 일부를 말한다. 임계 구역은 지정된 시간이 지난 후 종료된다. 때문에 어떤 스레드(태스크 또는 프로세스)가 임계 구역에 들어가고자 한다면 지정된 시간만큼 대기해야 한다. 스레드가 공유자원의 배타적인 사용을 보장받기 위해서 임계 구역에 들어가거나 나올때는 세마포어 같은 동기화 매커니즘이 사용된다.

* 상호배제(Mutual Exclusion): 상호 배제(相互排除, mutual exclusion, Mutex, 뮤텍스)는 동시 프로그래밍에서 공유 불가능한 자원의 동시 사용을 피하기 위해 사용되는 알고리즘으로, 임계 구역(critical section)으로 불리는 코드 영역에 의해 구현된다.

* 세마포어(Semaphore): 에츠허르 다익스트라가 제안한 교착 상태에 대한 해법으로 두개의 Atomic한 함수로 제어되는 정수 변수로 멀티프로그래밍 환경에서 공유자원에 대한 접근 제어를 하는 방식으로 1개의 공유되는 자원에 제한된 개수의 프로세스, 또는 스레드만 접근할 수 있도록 한다. 세마포어의 카운트는 1 이상이며 카운트를 조절하여 진입 가능한 프로세스/스레드 수를 조절할 수 있다. 세마포터 카운트가 항상 1인 것은 아니다.

* 기아상태(Aging): 컴퓨터 과학 용어의 하나로, 프로세스가 끊임없이 필요한 컴퓨터 자원을 가져오지 못하는 상황으로, 이러한 자원 없이는 처리를 끝낼 수 없는 병행 컴퓨팅에서 마주치는 문제이다. 기아 상태는 스케줄링이나 상호 배제 알고리즘의 오류에 기인하지만 자원 누수에 의해 일어날 수도 있으며 포크 폭탄과 같은 서비스 거부 공격을 통해 고의적으로 발생할 수도 있다.

## ★ REFERENCE

:laughing: [OPERATING SYSTEM REFERENCE](https://github.com/ChangYeop-Yang/Study-ComputerScience/issues/4)
