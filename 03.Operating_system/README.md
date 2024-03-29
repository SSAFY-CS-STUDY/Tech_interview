# Part 03. Operating System

Made by. [김민지](https://github.com/SSAFY-CS-STUDY/Tech_interview/tree/main/03.Operating_system/kmj) [박혜빈](https://github.com/SSAFY-CS-STUDY/Tech_interview/tree/main/03.Operating_system/phb) [이연주](https://github.com/SSAFY-CS-STUDY/Tech_interview/tree/main/03.Operating_system/lyj) [황성현](https://github.com/SSAFY-CS-STUDY/Tech_interview/tree/main/03.Operating_system/hsh)

## [Process & Thread](#process--thread-답변)
#### 💡 운영체제란 무엇인가? 
#### 💡 프로세스와 스레드에 대해 설명해주세요.
#### 💡 멀티 스레드의 장점 및 단점은 무엇인가?
#### 💡 멀티 프로세스 대신 멀티 스레드를 사용하는 이유
#### 💡 스레드에 스택을 독립적으로 할당하는 이유?
#### 💡 PC레지스터를 스레드마다 독립적으로 할당하는 이유?
#### 💡 자바 스레드란?
#### 💡 Thread-safe가 뭐에요?
#### 💡 세마포어와 뮤텍스를 설명해주세요.

## [Scheduling](#scheduling-답변)
#### 💡 스케줄러란?
#### 💡 스케줄링 단계를 설명해주세요. 
#### 💡 스케줄링이 무엇인지와 목적을 설명해주세요
#### 💡 Context Switching이 뭐에요?
#### 💡 PCB에 저장되는 정보는 어떤 것들이 있나요?
#### 💡 비선점방식과 선점방식을 설명해주세요.
#### 💡 Round Robin 스케줄링이 뭐에요?
#### 💡 스케줄링 기법 중 FCFS의 단점과 해결 방법을 설명해주세요.

## [메모리 관리 전략](#메모리-관리-전략-답변)
#### 💡 교착상태 vs 기아상태
#### 💡 운영 체제에서 에이징(Aging)는 무엇입니까?
#### 💡 외부 단편화와 내부 단편화란?
#### 💡 페이징의 장점과 단점은?
#### 💡 메모리 단편화 해결 기법에 대해 설명하시오.
#### 💡 페이지 교체 알고리즘 중 3가지를 선택해서 설명해주세요. 

## [가상 메모리](#가상-메모리-답변)
#### 💡 가상메모리의 역할은 무엇인가요?
#### 💡 Page Fault에 대해 설명하시오.
#### 💡 Demand Paging(요구 페이징)에 대해 설명하시오.
#### 💡 Swapping이 무엇인가요?
#### 💡 페이지 적중율을 극대화 시키기 위한 방법에는 무엇이 있는지 간략히 설명해주세요. 
#### 💡 Cache 메모리를 사용하는 이유에 대해 설명하시오.

## [커널](#커널-답변)
#### 💡 Kernel(커널)이란?
#### 💡 인터럽트가 필요한 이유 및 언제 발생되는지 말해주세요.
#### 💡 인터럽트 종류는 무엇이 있으며 우선순위를 말해주세요.
#### 💡 인터럽트 동작 과정을 말해주세요.
#### 💡 시스템콜이란 무엇이며 시스템 콜을 사용하는 예시를 말해주세요.
#### 💡 커널 모드와 유저 모드를 구분해 놓은 이유
#### 💡 커널 수준 스레드와 사용자 수준 스레드의 각각 장단점?


## [심화질문](#심화질문-답변)
#### 💡 부팅이란
#### 💡 파일 시스템이란
#### 💡 CISC(Complex)와 RISC(Reduced)의 차이
#### 💡 RISC가 단순하고 빠른 구조인데 왜 CISC를 사용하나요?
#### 💡 캐시와 레지스터의 차이점은 무엇인가요?

</br></br>

# Operating System 답변

#### ✏️ : 의논 중인 미완성 답변입니다.

## Process & Thread 답변
#### 💡 운영체제란 무엇인가? 
* 일반적으로 하드웨어를 관리하고, `응용 프로그램과 하드웨어 사이에서 인터페이스` 역할을 하며, 시스템의 동작을 제어하는 시스템 소프트웨어를 운영체제라고 합니다.

#### 💡 프로세스와 스레드에 대해 설명해주세요.
* 프로세스는 현재 실행 중인 프로그램을 의미하며 스레드는 프로세스 내부에서 실행되는 작업 흐름의 단위를 의미합니다.

#### 💡 멀티 스레드의 장점 및 단점은 무엇인가?  
* 스레드는 자원을 공유하기 때문에 `Context Switch가 적고 오버헤드가 작습니다.`
* 단점은 프로세스 내부의 자원을 공유하기 때문에 `동시에 자원에 접근했을 때 문제`가 될 수 있습니다. 또한, 하나의 스레드가 자신의 데이터 공간을 망가뜨린다면 해당 데이터를 공유하고 있는 모든 스레드에 치명적인 문제를 발생시킵니다.

#### 💡 멀티 프로세스 대신 멀티 스레드를 사용하는 이유 
* 프로그램을 여러 개 키는 것보다 하나의 프로그램 안에서 여러 작업을 해결하기 위해서 입니다. 이유는 `프로세스를 생성하여 자원을 할당하는 시스템 콜`이 줄어 들어 자원을 효율적으로 관리할 수 있습니다. 또한 프로세스간의 통신보다 쓰레드 간의 `통신의 비용`이 적기 때문에 멀티 프로세스보다 멀티 스레드를 사용하는 이유입니다.

#### 💡 스레드에 스택을 독립적으로 할당하는 이유? ✏️
* 스택: 인자, 변수 등을 저장하는 메모리 공간
* 스레드마다 `독립적인 함수 호출`, 실행을 하기 위해서 스레드에 스택을 독립적으로 할당합니다. 

#### 💡 PC(Program Counter) 레지스터를 스레드마다 독립적으로 할당하는 이유? ✏️
* PC 레지스터: 스레드가 명령어의 어디까지 수행했는지
* Context Switch 할 때 이전에 어디 부분까지 작업을 수행했는지 기억하기 위해서 PC 레지스터를 스레드마다 독립적으로 할당합니다. 

#### 💡 자바 스레드란?
* 일반 스레드와 거의 차이가 없으며, JVM이 운영체제의 역할을 합니다.
* **자바는 프로세스가 존재하지 않고 스레드만 존재합니다.**
* 자바 스레드는 JVM에 의해 스케줄링되는 코드블록입니다.
* 개발자는 스레드 코드를 작성하고 JVM에 실행을 요청합니다.

#### 💡 Thread-safe가 뭐에요?
* 멀티 스레드 환경에서 공유 자원에 **여러 스레드 접근이 있어도 프로그램 실행에 문제 없음**을 의미합니다.

#### 💡 세마포어와 뮤텍스를 설명해주세요.
* 여러 프로세스나 쓰레드가 `공유 자원에 접근`하는 것을 제어하기 위한 방법입니다. 
* 세마포어는 `count`를 주어 count 값만큼 프로세스/스레드가 접근 가능하도록 하는 기법이며 뮤텍스는 `lock/unlock`으로 권한을 가진 프로세스/스레드만 접근할 수 있도록하는 기법입니다.

## Scheduling 답변
#### 💡 스케줄러란?
 * 어떤 프로세스에게 자원을 할당할지 결정하는 운영체제의 커널 모듈입니다. 

#### 💡 스케줄링 단계를 설명해주세요.
* 장기 스케줄러에 의해 어떤 프로세스가 준비 큐에 삽입될지 결정합니다.
  * Ready Queue란 현재 메모리 내에 있으면서 CPU에 의해 실행되기를 기다리는 프로세스의 집합을 의미합니다.
* 단기 스케줄러는 스케줄링 알고리즘에 따라 CPU를 할당할 프로세스를 선택합니다. 
* 선택된 프로세스는 Running 상태가 되고 작업이 끝나면 Terminated 상태가 됩니다.
* 중기 스케줄러는 메모리에 너무 많은 프로그램이 동시에 올라가는 것을 조절합니다.

#### 💡 스케줄링이 무엇인지와 목적을 설명해주세요.
* 스케줄링은 프로세서에게 필요한 자원을 어떻게 할당할 것인지 선택하는 알고리즘 입니다.
* 단위 시간당 처리량을 최대화하고 효율적으로 자원을 할당하기 위한 목적을 가지고 있습니다.

#### 💡 Context Switching이 뭐에요? ✏️
* Context Switching이란 하나의 프로세스가 CPU를 사용 중인 상태에서 다른 프로세스가 CPU를 사용하도록 하기 위해, 이전의 프로세스의 상태(문맥)를 보관하고 새로운 프로세스의 상태를 적재하는 작업을 말한다.
#### 💡 PCB에 저장되는 정보는 어떤 것들이 있나요?
* PID(프로세스 식별자), PS(프로세스 상태), PC(프로그램 카운터)등의 프로세스 정보가 있습니다.
    * PCB란? 메모리에 저장되는 프로세스 관련 정보 데이터 블록으로 스케줄링 및 문맥교환에 필요합니다.

#### 💡 비선점방식과 선점방식을 설명해주세요.
* 비선점 방식은 프로세스가 CPU를 점유하고 있는 경우 다른 프로세스가 CPU를 `빼앗지 못하는 방식`입니다. 비선점방식은 CPU를 중간에 가로채지 않기 때문에 응답시간 예측이 용이하다는 장점이 있지만 중요한 작업이 오래 기다리는 경우가 발생할 수 있다는 단점이 있습니다.
* 선점 방식은 프로세스가 CPU를 점유하고 있어도 우선 순위가 높은 프로세스가 오면 CPU를 `빼앗을 수 있는 방식`입니다. 선점방식은 우선 순위가 높은 프로세스가 빠르게 처리할 수 있다는 장점이 있지만 잦은 Context Switching으로 오버헤드가 증가한다는 단점이 있습니다.

#### 💡 Round Robin 스케줄링이 뭐에요?
* 스케줄링 방식 중 시분할 시스템을 위해 설계된 선점 방식의 알고리즘 입니다. 각 프로세스는 `같은 크기의 CPU 시간을 할당`받게 됩니다. 할당된 시간 안에 작업이 끝나지 않으면 해당 프로세스는 ready 큐에 들어가는 선입선출 방식입니다.

#### 💡 스케줄링 기법 중 FCFS의 단점과 해결 방법을 설명해주세요.
* FCFS 는 `대기 큐에 도착한 순서`에 따라 CPU를 할당합니다. 그래서 긴 작업이 짧은 작업을 오랫 동안 기다릴 수 있습니다.
* 단점을 해결하는 방법으로는 준비 큐에서 기다리고 있는 프로세스 중 **가장 CPU 요구량이 적은 것을 먼저 실행시켜 주는** `SJF(Shortest Job First)`가 있습니다.

## 메모리 관리 전략 답변
#### 💡 교착상태 vs 기아상태
* 교착상태는 둘 이상의 프로세스들이 자원을 점유한 상태에서 `서로 다른 프로세스가 점유`하고 있는 자원을 요구하며 무한정 기다리는 상황입니다.
* 기아상태는 병행 프로세스에서 프로세스가 실행되는데에 필수적인 `자원을 끊임없이 사용하지 못하는 상황`입니다.

#### 💡 운영 체제에서 에이징(Aging)는 무엇입니까?
- aging이란 프로세스의 `대기 시간에 비례하는 높은 우선순위`를 부여하여 가까운 시간 안에 자원을 할당하는 기법입니다.
- Priority 스케줄링에서 기아 상태 및 무한정 대기를 에이징으로 해결할 수 있습니다.

#### 💡 외부 단편화와 내부 단편화란?
- 내부 단편화는 프로세스가 `필요한 양보다 더 큰 메모리 공간에 할당`되어 메모리가 낭비되는 것을 말합니다. 
- 외부 단편화는 메모리에 프로세스가 할당될 만큼 `충분한 공간이 존재하지만 공간이 쪼개어져서` 프로세스를 넣을 수 없는 것을 의미합니다.

#### 💡 메모리 단편화 해결 기법에 대해 설명하시오.
* 가상메모리를 이용하여 내부 단편화 기법을 해결하는 세그멘테이션과 외부 단편화를 해결하는 페이징 기법이 있습니다.
    * Segmentation은 메모리를 서로 크기가 다른 논리적인 블록 단위인 세그먼트로 분할하여 메모리를 할당하는 기법입니다.
    * Paging은 프로세스를 일정 크기인 페이지로 잘라서 메모리에 적재하는 방식입니다.

#### 💡 페이징의 장점과 단점은? ✏️ 
- 페이징 기법을 사용하게되면 **하나의 프로세스가 사용하는 메모리 공간이 연속적이어야 한다는 제약을 없애 외부 단편화 문제점을 해결**할 수 있습니다.
- ✏️ 하지만 그만큼 Mapping 과정 또한 늘어나기 때문에 Trade-Off 가 발생할 수 있습니다. 그리고 보통 페이지 단위에 알맞게 꽉채워 쓰는게 아니므로 내부 단편화 문제는 여전히 있습니다.

#### 💡 페이지 교체 알고리즘 중 3가지를 선택해서 설명해주세요. 
- FIFO(First In First Out)는 가장 간단한 페이지 교체 알고리즘으로  **먼저 물리 메모리에 들어온 페이지 순서대로 페이지 교체 시점에 먼저 나가게 되는** 알고리즘입니다.
- OPT(OPTimal replacement)는 가장 오랫동안 사용되지 않을 페이지를 찾아 교체하는 알고리즘입니다.
- LRU(Least Recently Used)는 페이지 교체 알고리즘 중 가장 많이 쓰이는 알고리즘으로 가장 오랫동안 사용되지 않은 페이지를 선택하여 교체하는 알고리즘입니다.

## 가상 메모리 답변
#### 💡 가상메모리의 역할은 무엇인가요? 
* 실제 메모리를 보조하여 프로세스 전체가 메모리 내에 올라오지 않더라도 실행이 가능하도록 해주는 역할입니다. 

#### 💡 Page Fault에 대해 설명하시오.
* Page fault란 지금 실행시켜야 할 Page가 실제 메모리에 올라와 있지 않는 것을 말합니다.
* Page Fault 로 인한 I/O 작업은 CPU 의 효율성을 낮추게 됩니다.

#### 💡 Demand Paging(요구 페이징)에 대해 설명하시오.
* 요구 페이징이란 가상 메모리 관리 방법입니다.
* 프로그램 실행 시작 시에 프로그램 전체를 디스크에서 물리 메모리에 적재하는 대신, 초기에 필요한 것들만 적재하는 전략을 요구 페이징이라고 합니다.
* 가상 메모리 시스템에서 많이 사용됩니다.
    * 프로세스 실행에 실제 필요한 페이지들만 메모리로 읽어옴으로써, 사용되지 않을 페이지를 가져오는 시간과 메모리 낭비를 줄일 수 있습니다.

#### 💡 Swapping이 무엇인가요?
* 메모리 관리를 위해 사용되는 기법 중 하나입니다. 프로세스를 불러들이기 위한 공간이 메모리에 부족하다면 현재 메모리에 적재된 프로세스들을 내보내고(swap out), 원하는 프로세스를 불러들이는 (swap in) 방식입니다.

#### 💡 페이지 적중률을 극대화 시키기 위한 방법에는 무엇이 있는지 간략히 설명해주세요. 
* 페이지 적중률을 높이기 위해 지역성을 사용합니다. 
* 한 번 참조된 메모리 옆에 있는 메모리를 참조할 확률이 높다는 공간 지역성과 최근에 참조된 주소 내용은 곧 다음에 다시 참조된다는 시간 지역성이 있습니다.

#### 💡 Cache 메모리를 사용하는 이유에 대해 설명하시오. 
* 캐시 메모리는 CPU의 처리속도와 주기억장치의 접근 속도 차이를 줄이기 위해 사용하는 고속 Buffer Memory입니다.

## 커널 답변
#### 💡 Kernel(커널)이란? 
* 커널은 `하드웨어와 응용 프로그램 사이에서 인터페이스`를 제공하며 응용 프로그램이 하드웨어에서부터 오는 자원을 관리하고 사용 할 수 있게 해주는 역할을 합니다.

#### 💡 인터럽트가 필요한 이유 및 언제 발생되는지 말해주세요.
* CPU와 I/O의 속도 차이를 극복하기 위해 인터럽트가 필요합니다.(입출력 연산이 CPU 명령 수행속도보다 현저히 느리기 때문입니다.) 
* CPU가 프로그램을 실행하고 있을 때, 입출력 하드웨어 등의 장치나 예외상황이 발생하여 처리가 필요한 경우에 발생합니다.

#### 💡 인터럽트 종류는 무엇이 있으며 우선순위를 말해주세요. 
* 인터럽트는 외부 인터럽트, 내부 인터럽트, 소프트웨어 인터럽트 3가지로 나눌 수 있습니다.
* 외부인터럽트, 내부인터럽트, 소프트웨어 인터럽트 순으로 인터럽트의 우선순위가 높습니다.
    * 외부 인터럽트는 하드웨어가 발생시키는 인터럽트입니다. ex) CPU가 아닌 다른 하드웨어 장치가 CPU에 요청하는 경우 
    * 내부 인터럽트는 CPU 내부에서 인터럽트에 걸리는 경우 발생합니다. ex) Divide by Zero 
    * 소프트웨어 인터럽트는 소프트웨어가 발생시키는 인터럽트를 말합니다. ex)시스템 콜 

#### 💡 인터럽트 동작 과정을 말해주세요.
* CPU가 프로그램을 실행합니다.
* 인터럽트 요청이 들어옵니다.
* CPU는 프로그램을 중단하고 다음 실행할 명령어와 현재 상태를 PCB 블록에 저장합니다.
* ISR(Interrupt Service Routine)을 실행합니다.
* 인터럽트 종료 후 기존 상태를 복구합니다.
* 프로그램을 계속 실행합니다.

#### 💡 시스템콜이란 무엇이며 시스템 콜을 사용하는 예시를 말해주세요. ✏️
* 응용 프로그램의 요청에 따라 커널에 접근하기 위한 인터페이스입니다.
* 사용자 모드에서 시스템 콜이나 라이브러리 함수를 통해 I/O 요청커널 모드로 전환 후 커널의 I/O 관리자에 의해 장치 드라이버에 요청장치 드라이버에서 받은 값을 커널에 전달받은 값을 커널이 사용자에게 전달사용자 모드로 전환 fork(),exec() 
* 사용자 모드에서 malloc 함수를 이용하여 메모리 할당 요청 ← System call커널 모드로 전환 후 메모리값을 사용자에게 전달. 사용자 모드로 전환
* `cp in.txt out.txt` 에서 in.txt 파일을 접근할 수 있는지 검사하기 위해 시스템 콜을 호출합니다. 만약 파일이 존재하지 않는다면 에러발생, 종료 할 때도 시스템 콜이 사용됩니다.

#### 💡 커널 모드와 유저 모드를 구분해 놓은 이유
* 시스템에 중요한 영향을 미치는 연산은 커널 모드에서만 실행 가능하도록 함으로써 하드웨어의 보안을 유지하기 위해서 입니다. 

#### 💡 커널 수준 스레드와 사용자 수준 스레드의 각각 장단점?
* 커널 수준 스레드는 커널이 직접 스레드를 제공해 주기 떄문에 안정성과 다양한 기능이 제공됩니다. 또한 커널이 각 스레드를 개별적으로 관리할 수 있습니다.
* 단점은 유저 모드에서 커널 모드로 전환이 빈번하게 이루어지기 때문에 성능이 저하됩니다.
* 사용자 수준 스레드는 커널 모드/유저모드 간 전환이 일어나지 않기 때문에 오버헤드 적다는 장점이 있습니다. 또한 라이브러리를 사용하기 때문에 이식성이 높고 유연한 스케줄링이 가능합니다. +) 운영체제에서 스레드를 지원할 필요가 없습니다.
* 반면, 하나의 스레드가 블록되면 전체 프로세스가 블록된다는 단점이 있습니다.


## 심화질문 답변
#### 💡 부팅이란
* pc에 전원이 들어온 후 운영체제가 실행되기 전까지의 과정을 말합니다.
* 리눅스 부팅은 0단계부터 4단계까지 있습니다. 다음의 순서로 진행됩니다.
    * 전원 공급 
    * BIOS 단계
        * ROM에 탑재된 `BIOS`가 키보드나 스크린의 부팅에 필요에 필요한 하드웨어의 각 장치들을 인식하고 초기화 하는 단계입니다. 
    * 부트로더 단계
    * 커널 로딩
    * init 프로세스 


#### 💡 파일 시스템이란 
* 컴퓨터에서 파일을 쉽게 접근할 수 있도록 관리하는 체제를 말합니다.

#### 💡 CISC(Complex)와 RISC(Reduced)의 차이
* CISC는 RISC에 비해 연산에 처리되는 복잡한 명령어들을 탑재하고 있기 때문에 전력소모가 크고 속도가 느립니다. 다만, RISC는 CISC에 비해 하드웨어가 간단한 대신 명령어들을 조합하기 때문에 소프트웨어가 복잡해 질 수 있습니다.
* 
#### 💡 RISC가 단순하고 빠른 구조인데 왜 CISC를 사용하나요?
* 많은 프로세서가 CISC로 구축되어 있어 모두 RISC로 변경하기에는 많은 비용이 소모되기 때문입니다.
* 또, 호환성이 RISC보다 높습니다. 

#### 💡 캐시와 레지스터의 차이점은 무엇인가요?
* 캐시는 cpu와 별도로 있는 공간이며, 메인 메모리와 cpu 간의 속도 차이를 극복하기 위한 것입니다.
* 레지스터는 cpu 안에서 연산을 처리하기 위하여 데이터를 저장하는 공간입니다. 
![image](https://user-images.githubusercontent.com/39117025/109632749-b9edba00-7b8a-11eb-84fd-e3ac90a06b57.png)

#### 💡 메모리 풀(Memory pool)

* 필요한 메모리 공간과 개수만큼 메모리 풀을 만들어 놓고, 필요할 때마다 사용하고 반납하는 메모리 단편화 해결 기법입니다.
    * 메모리의 할당과 해제가 잦은 경우 쓰면 효과적입니다.
    * 필요한 크기만큼 할당을 해놓기 때문에 내부 단편화가 발생하지 않습니다.
    * 미리 공간을 할당해놓고 가져다 쓰고 반납하기 때문에 외부 단편화가 발생하지 않습니다.
* 메모리의 할당과 해제가 잦은 경우 쓰면 효과적이지만 메모리 풀을 만들고 사용하지 않아도 계속 할당을 해놓으므로 메모리 누수가 발생할 수 있습니다. 
* 메모리 단편화로 인한 메모리 낭비보다 사용하지 않는 메모리가 더 크다면 사용하지 않는게 낫습니다. 
