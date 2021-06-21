# Part 04.Java

Made by. [김민지](https://github.com/SSAFY-CS-STUDY/Tech_interview/tree/main/04.Java/kmj) [박혜빈](https://github.com/SSAFY-CS-STUDY/Tech_interview/tree/main/04.Java/phb) [이연주](https://github.com/SSAFY-CS-STUDY/Tech_interview/tree/main/04.Java/lyj) [황성현](https://github.com/SSAFY-CS-STUDY/Tech_interview/tree/main/04.Java/hsh)

## [객체지향](#객체지향-답변)

#### 💡 객체지향 프로그래밍과 절차지향 프로그래밍의 차이에 대해 설명하시오.

#### 💡 객제지향 프로그래밍의 특징에 대해 설명하시오.

#### 💡 객체지향 설계 5원칙에 대해 설명하시오.

#### 💡 오버로딩과 오버라이딩에 대해 설명하시오.

#### 💡 클래스와 객체의 차이는 무엇인가요?

#### 💡 객체와 인스턴스의 차이는 무엇인가요?

## [Java](#java-답변)

#### 💡 자바의 특징에 대해 설명하시오.

#### 💡 Java SE와 EE의 차이점은 무엇인가요?

#### 💡 참조형 변수와 기본형 변수의 차이점을 설명해주세요.

#### 💡 변수의 3가지 타입에 대해 설명해주세요.

#### 💡 Wrapper Class에 대해 설명하시오.

#### 💡 public 접근 제어자와 private 접근 제어자의 차이

#### 💡 Boxing, Unboxing에 대해 설명하시오.

#### 💡 non-static 멤버와 static 멤버의 차이에 대해 설명하시오.

#### 💡 main 메소드가 public static인 이유는?

#### 💡 Final 키워드의 용도에 대해 설명하시오.

#### 💡 Generic에 대해 설명하시오.

#### 💡 ==과 equals()의 차이에 대해 설명하세요.

#### 💡 Call by Reference와 Call by Value의 차이에 대해 설명하시오.

#### 💡 추상 클래스와 인터페이스의 차이에 대해 설명하시오.

#### 💡 java reflection에 대해 설명하시오.

#### 💡 StringBuilder와 StringBuffer의 차이점을 설명해주세요.

#### 💡 Java 8에 추가된 기능은 무엇이 있나요?

#### 💡 Lambda란 무엇이고 어떠한 장점이 있는가?

#### 💡 Stream API 특징이나 장점은 무엇이 있나요?

#### 💡 Garbage Collector(GC)란?

#### 💡 GC에 의해 변수가 초기화되는 시점을 설정해주세요.

#### 💡 JAVA에서 바이트코드에 대해 설명해보세요.

#### 💡 예외처리 방법을 설명해주세요.

#### 💡 JAVA 동작 원리

#### 💡 자바에서 쓰레드를 구현하기 위한 2가지 방법을 간단하게 설명하시오.

#### 💡 Collection 정의와 종류를 말씀해주세요

#### 💡 ArrayList와 LinkedList의 차이는 무엇인가요

#### 💡 CheckedException과 UnCheckedException의 차이

#### 💡 Synchronized(동기화)를 하기 위한 방법은 무엇이 있나요

#### 💡 try-with-resource란?

#### 💡 Functional Interface란 무엇인가요?

#### 💡 Method Reference는 무엇인가요?

#### 💡 Optional 클래스는 무엇인가요?

#### 💡 업캐스팅과 다운캐스팅의 차이는 무엇인가요?

#### 💡 this 키워드는 언제 사용되나요?

</br></br>

# Java 답변

#### ✏️ : 의논 중인 미완성 답변입니다.

## 객체지향 

#### 💡 객체지향 프로그래밍과 절차지향 프로그래밍의 차이에 대해 설명하시오.

- 절차지향 프로그래밍은 데이터 중심의 함수를 구현하며 프로그램을 순차적으로 처리하는 기법입니다. 속도가 빠르다는 장점이 있지만, 코드의 순서가 바뀌면 올바른 결과를 보장하기 어렵습니다.
- 객체지향 프로그래밍은 기능 중심으로 데이터와 기능을 하나로 묶어서 개발하는 방법입니다. 코드의 재활용성이 높다는 장점이 있지만, 설계하는 데 시간이 오래 걸립니다.

#### 💡 객제지향 프로그래밍의 특징에 대해 설명하시오.

- 캡슐화, 상속, 추상화, 다형성 4가지 특징을 가지고 있습니다.
  - 캡슐화는 연관 있는 변수와 함수를 클래스로 묶는 작업을 의미합니다.
  - 상속은 자식 클래스가 부모 클래스의 특성과 기능을 물려받아 재사용성을 높이는 역할을 합니다.
  - 추상화란 인터페이스로 공통적인 특성들을 묶어 표현하는 것을 의미합니다.
  - 다형성의 대표적인 특징으로는 오버로딩, 오버라이딩이 있습니다.

#### 💡 객체지향 설계 5원칙에 대해 설명하시오.

- SRP(단일 책임 원칙), OCP(개방-폐쇄 원칙), LSP(리스코프 치환 원칙), DIP(의존 역전 원칙), ISP(인터페이스 분리 원칙)을 말하며, 앞자를 따서 SOILD 원칙이라고 부릅니다.
- 프로그래머가 시간이 지나도 유지 보수와 확장이 쉬운 소프트웨어를 만드는데 이 원칙들을 적용할 수 있습니다.
  - SRP( Single Responsibility Principle ), 단일 책임 원칙
    - 객체는 단 하나의 책임만 가져야 한다는 원칙을 말합니다.
    - 시스템에 변화가 생기더라도 영향을 최소화 할 수 있다는 장점이 있습니다.
  - OCP ( Open-Closed Principle ), 개방-폐쇄 원칙
    - 기존의 코드를 변경하지 않으면서, 기능을 추가할 수 있도록 설계가 되어야 한다는 원칙을 말합니다.
    - 확장에 대해서는 개방적이고 수정에 대해서는 폐쇄적으로 설계해야 한다는 의미입니다.
  - L (LSP : Liskov’s Substitution Principle)
    - 자식 클래스는 최소한 자신의 부모 클래스에서 가능한 행위는 수행할 수 있어야 한다는 설계 원칙입니다.
  - I (ISP : Interface Segregation Principle)
    - 자신이 사용하지 않는 인터페이스는 구현하지 말아야 한다는 설계 원칙입니다.
  - D (DIP : ependency Inversion Principle)
    - 객체들이 서로 정보를 주고 받을 때 의존 관계가 형성되는데, 이 때 객체들은 나름대로의 원칙을 갖고 정보를 주고 받아야 한다는 설계 원칙입니다.

#### 💡 오버로딩과 오버라이딩에 대해 설명하시오.

- 오버로딩은 메서드의 이름은 같고, 매개변수의 개수나 타입이 다른 함수를 정의하는 것을 의미합니다.
- 오버라이딩은 상위 클래스의 메서드를 하위 클래스에서 재정의 하는 것을 의미합니다.

#### 💡 클래스와 객체의 차이는 무엇인가요?

- 클래스는 ‘설계도’, 객체는 ‘설계도로 구현한 모든 대상’을 의미합니다.

#### 💡 객체와 인스턴스의 차이는 무엇인가요?

- 클래스의 타입으로 선언되었을 때 객체라고 부르고, 그 객체가 메모리에 할당되어 실제 사용될 때 인스턴스라고 부른다.

## Java

#### 💡 자바의 특징에 대해 설명하시오.

- 자바는 객체지향적 프로그래밍 언어이며 플랫폼 독립성, 멀티쓰레드, 자동 메모리 관리 등 다양한 특징을 가지고 있습니다.

#### 💡 Java SE와 EE의 차이점은 무엇인가요?

- Java SE란 Java Platform Standard Edition의 약자로 데스크톱, 서버, 임베디드를 위한 표준 자바 플랫폼을 말합니다.
- Java EE란 Java Platform EnterPrise Edition의 약자로 자바를 이용한 서버측 개발을 위한 플랫폼입니다. SE에 서버측을 위한 기능을 추가하여 SE의 모든 기능을 이용 할 수 있습니다.

#### 💡 참조형 변수와 기본형 변수의 차이점을 설명해주세요.

- 기본형 변수에는 실제 사용되는 데이터가 저장됩니다.
- byte, short, int, long, float, double, boolean, char 이 있으며 스택에 저장됩니다.
- 참조형 변수에는 실제 데이터의 위치를 담은 주소값이 저장됩니다.

#### 💡 변수의 3가지 타입에 대해 설명해주세요.

- 로컬 변수는 메서드 내에서 선언된 위치부터 소속된 중괄호가 끝나는 지점까지 사용이 가능합니다.
- 인스턴스 변수는 클래스를 통해 생성된 인스턴스 내에서 접근이 가능합니다.
- 클래스 변수는 클래스의 모든 인스턴스에서 공유하는 변수로서 클래스가 메모리에 올라갈 때 static 영역에 생성됩니다.

#### 💡 Wrapper Class에 대해 설명하시오.

- 8개의 기본 타입에 해당하는 데이터를 객체로 포장해주는 클래스
- Wrapper 클래스를 이용할 때 주의할 점은 참조형끼리 연산이 불가능하기 때문에 기본 자료형으로 변환하여 연산해야 한다.

#### 💡 public 접근 제어자와 private 접근 제어자의 차이

- Public 접근 제어자는 같은 패키지 안의 클래스뿐 아니라, 다른 패키지 안의 클래스에서도 사용 가능합니다.
- Private 접근 제어자는 오로지 그 클래스에서만 사용할 수 있습니다.

#### 💡 Boxing, Unboxing에 대해 설명하시오.

- 참조 타입의 값을 "Wrapper" 클래스로 바꿔주는것이 박싱이라고 하고, 반대로 "Wrapper" 클래스 타입의 값을 프리미티브 타입으로 바꿔주는 것을 언박싱이라고 합니다.
  - 자바 1.5 이후 부터 Auto Boxing/ Auto Unboxing으로 명시적으로 원시타입을 참조타입으로 변환시켜주지 않아도 자동으로 Boxing / Unboxing한다. 하지만 이러한 기능은 메모리 누수 원인일 될 수 있다.

#### 💡 non-static 멤버와 static 멤버의 차이에 대해 설명하시오.

- static 멤버는 클래스 당 하나만 생성되고 non-static 멤버는 객체마다 별도로 존재합니다.
- static 멤버는 동일한 클래스의 모든 객체들에 의해 공유되는 특성을 가지고 있습니다.

#### 💡 main 메소드가 public static인 이유는?

- 어떤 패키지에 있던 main 메소드는 JVM에 의해서 가장 먼저 실행되야 하므로 public을 사용합니다.
- 실행 전 main 메소드는 메모리에 적재되어 있어야 하므로 static으로 선언되어 있어야 합니다.

#### 💡 Final 키워드의 용도에 대해 설명하시오.

- 변수, 메서드, 클래스에 사용 할 수 있으며 변수에 사용 시 값이 변경 불가능하고 메서드에 사용 시 오버라이딩을 못하게 만들며 클래스에 사용할 시에 상속을 할 수 없게 만드는 용도입니다.

#### 💡 Generic에 대해 설명하시오.

- 객체 타입을 컴파일 시에 체크해주는 것입니다.
- 컴파일 시에 타입을 체크하므로 타입 안정성을 높이고 형변환의 번거로움을 줄일 수 있습니다.

#### 💡 ==과 equals()의 차이에 대해 설명하세요.

- 동등연산자(==)는 두 객체가 같은 메모리 공간을 가리키는지 확인을 할 때 사용합니다.
- equals()는 두 객체의 값이 같은지를 확인할 때 사용하는 메서드입니다.

#### 💡 Call by Reference와 Call by Value의 차이에 대해 설명하시오.

- call by reference 주소값을 호출
- call by value 실제 값을 호출

- 메소드의 매개변수의 값을 복사를 하여 처리를 하느냐, 아니면 직접 참조를 하느냐 차이를 의미합니다.
- Call by Value의 경우 인자로 받은 값이 보존됩니다.
- Call by reference로 넘어온 객체 값이 변경된 경우 원래의 값이 영향을 받게 됩니다.

#### 💡 추상 클래스와 인터페이스의 차이에 대해 설명하시오.

- 추상클래스의 목적은 **공통점을 찾아 추상화**하는 것입니다.
- 인터페이스의 목적은 **구현 객체가 같은 동작하는 것을 보장**하는 것입니다.

#### 💡 java reflection에 대해 설명하시오.

- **동적으로 클래스를 사용해야 할때 필요한 API 입니다.**
  - 즉, 작성 시점에는 어떤 클래스를 사용해야 할지 모르는 경우, 런타임 시점에서 클래스를 가져와서 실행해야 하는 경우에 사용된다. 대표적으로 IntelliJ의 자동완성이나 Spring 프레임워크의 어노테이션 같은 기능들이 리플렉션을 이용해서 프로그램 실행 중 동적으로 클래스 정보를 가져와서 사용하는 예이다.

<details>
    <summary>참고</summary>
    <ul>
        <li>https://woowacourse.github.io/javable/post/2020-07-16-reflection-api</li>
        <li>https://madplay.github.io/post/java-reflection</li>
        <li>https://docs.oracle.com/javase/tutorial/reflect/index.html</li>
    </ul>
</details>

#### 💡 직렬화와 역직렬화에 대해 설명하시오.

- 직렬화는 객체를 파일에 저장하거나 네트워크를 통해 전달 할 수 있도록 변환하는 과정입니다.
- 역직렬화는 직렬화된 데이터를 불러와 다시 객체로 변환하는 과정입니다.

#### 💡 StringBuilder와 StringBuffer의 차이점을 설명해주세요.

- StringBuilder는 동기화 처리를 하지 않아 StringBuffer보다 속도가 더 빠릅니다.
- StringBuffer은 속도는 느리지만 멀티 스레드 환경에서 안전하게 사용할 수 있습니다.

#### 💡 Java 8에 추가된 기능은 무엇이 있나요?

- java.time 패키지와 스트림 API, 람다 표현식이 추가되었습니다.

#### 💡 Lambda란 무엇이고 어떠한 장점이 있는가?

- "식별자없이 실행가능한 함수" 함수인데 함수를 따로 만들지 않고 코드한줄에 함수를 써서 그것을 호출하는 방식입니다. 코드를 줄여 간단하게 작성 가능하고 가독성이 증가합니다.

#### 💡 Stream API 특징이나 장점은 무엇이 있나요?

- Stream API는 원본 데이터를 변경하지 않고 `가공된 데이터를 추출`합니다.

```java
List<Integer> list = new ArrayList<>();
long count = list.stream().filter(x -> x>3).count(); // 3보다 큰 수만 count하여 값 추출
```

#### 💡 Garbage Collector(GC)란?

- 개발자가 따로 메모리를 해제할 필요없이 힙 영역에서 더이상 사용되지 않을 객체들(쓰레기 객체) 를 찾아 메모리를 해제하여 메모리를 자동으로 정리해주는 것을 의미합니다.

#### 💡 GC에 의해 변수가 초기화되는 시점을 설정해주세요.

- 지역변수는 scope가 끝나거나 변수에 다른 객체를 삽입하면 초기화됩니다.
- 전역변수의 경우 프로그램이 종료되면 초기화됩니다.

* GC 동작 원리
  ![image](https://user-images.githubusercontent.com/36289638/117908488-72667580-b313-11eb-8038-78a44fa87d37.png)

  ![image](https://user-images.githubusercontent.com/36289638/117909370-10a70b00-b315-11eb-8afa-e6828141532b.png)

  1. 처음 생성된 객체는 Eden에 위치
  2. Minor GC 발생 후에 살아있다면 Survivor 영역으로 이동
  3. Survivor에서 살아남은 객체는 Old Generation 영역으로 이동

#### 💡 JAVA에서 바이트코드에 대해 설명해보세요.

- 자바 바이트 코드(Java bytecode)란 자바 가상 머신이 이해할 수 있는 언어로 변환된 자바 소스 코드를 의미합니다. (ex).class 파일)

#### 💡 예외처리 방법을 설명해주세요.

- [복구형] Try/Catch 블록

  - 예외 발생 가능성 있는 코드를 try문으로 감싸고, 발생 시에 처리는 catch에서 받아서 한다. 즉, 트라이 캐치 블록을 사용하면 해당 메소드에서 예외를 처리하게 된다.
  - try~with~resource: try에 자원 객체를 전달하면, try 코드 블록이 끝나면 자동으로 자원을 종료해주는 기능

- [회피형] throw 키워드 선언

  - 메소드 끝단에 throws Exception 을 선언하여 처리한다. 예외 발생 시, 메소드를 호출한 코드로 예외를 되돌려 보내서 처리하게 하는 방식이다.

- [전환형] catch에서 다른 예외를 던지는 것
  - 호출 측에서 에러의 타입을 명확하게 인지할 수 있도록 예외를 던져주는 것이다.

#### 💡 런타임(Runtime)과 컴파일타임(Compiletime)의 차이점은 무엇인가?

- 프로그램을 생성하기 위해 개발자는 첫째로 소스코드를 작성하고 컴파일이라는 과정을 통해 기계어코드로 변환 되어 실행 가능한 프로그램이 되며, 이러한 편집 과정을 컴파일타임(Compiletime) 이라고 부릅니다.
- 컴파일과정을 마친 프로그램은 사용자에 의해 실행되어 지며, 이러한 응용프로그램이 동작되어지는 때를 런타임(Runtime)이라고 부릅니다.

- 컴파일타임 오류의 유형
  - 신택스 오류
  - 타입체크 오류
- 런타임 오류의 유형
  - 0나누기 오류
  - 널(Null)참조 오류
  - 메모리 부족 오류

#### 💡 JAVA 동작 원리

![image](https://user-images.githubusercontent.com/36289638/117579007-feb64400-b12b-11eb-9a94-9370e11430f8.png)

1. 개발자가 자바 소스코드(.java)를 작성한다.
2. 컴파일러에 의해 소스파일를 바이트코드(.class)로 컴파일한다.
3. 바이트코드를 클래스 로더에게 전달한다.
4. 클래스로더에 의해 import한 클래스 읽힌다.
5. 런타임 데이터 영역에 의해 JVM 메모리에 올라간다.
6. 실행엔진은 JVM 메모리에 올라온 바이트 코드를 하나식 가져와 실행한다. (Java 컴파일러 사용)

#### 💡 자바에서 쓰레드를 구현하기 위한 2가지 방법을 간단하게 설명하시오.

- Runnable 인터페이를 확장해 run() 메소드 구현
- Thread 클래스를 상속받고 run() 메소드를 오버라이딩해 구현

#### 💡 Collection 정의와 종류를 말씀해주세요

- 컬렉션 프레임워크(collection framework)란 다수의 데이터를 쉽고 효과적으로 처리할 수 있는 표준화된 방법을 제공하는 클래스의 집합을 의미합니다.
- **Collection 인터페이스**

  - List 인터페이스는 순서가 있는 데이터의 집합으로, 데이터의 중복을 허용합니다.
  - ArrayList, LinkedList

- **Map 인터페이스**
  - 키와 값 쌍으로 이루어지는 데이터 집합으로, 키 값은 중복을 허용하지 않습니다.
  - HashMap, TreeMap

#### 💡 ArrayList와 LinkedList의 차이는 무엇인가요

- ArrayList는 데이터들이 순서대로 쭉 늘어선 배열의 형식을 취하고 있는 반면 LinkedList는 순서대로 늘어선 것이 아니라 자료의 주소 값으로 서로 연결되어 있는 구조입니다.
- **ArrayList**

  - 내부적으로 데이터를 배열로 관리하고 데이터 추가/삭제 시 임시 배열을 생성해 데이터를 복사합니다.
  - 데이터별 인덱스가 있어 검색에는 유리합니다.
  - 임시 배열을 사용하기 때문에 데이터 추가/삭제의 경우에는 불리합니다.

- **LinkedList**
  - 내부적으로 노드 단위로 데이터를 관리합니다. 자신의 앞 뒤 노드만 인지하는 상태입니다.
  - 인덱스가 따로 없기 때문에 검색 시 전 노드를 순회해야하여 검색시 불리합니다.
  - 데이터 추가/삭제 시 불필요한 데이터 복사가 없어 유리합니다.

#### 💡 CheckedException과 UnCheckedException의 차이

![image](https://user-images.githubusercontent.com/36289638/117830854-fe928180-b2ae-11eb-9d5e-9a2a2f3e6af4.png)

| 구분         | Checked Exception          | Unchecked Exception          |
| ------------ | -------------------------- | ---------------------------- |
| 확인시점     | 컴파일 시점                | 런타임 시점                  |
| 처리여부     | 반드시 예외 처리해야한다.  | 명시적으로 하지 않아도 된다. |
| 트랜잭션처리 | 예외 발생 시 롤백하지 않음 | 예외 발생시 롤백             |

<details>
    <summary>참고</summary>
    <ul>
        <li>https://madplay.github.io/post/java-checked-unchecked-exceptions</li>
    </ul>
</details>

#### 💡 Synchronized(동기화)를 하기 위한 방법은 무엇이 있나요

- synchronized 함수(메서드)를 만들어 사용합니다.
- synchronized 블록(block) 사용합니다.

#### 💡 try-with-resource란?

- 자동으로 자원을 해제하는 방법입니다.
- try에서 선언된 객체가 AutoCloseable을 구현하였다면 Java는 try구문이 종료될 때 객체의 close() 메소드를 자동으로 호출합니다.

#### 💡 Functional Interface란 무엇인가요?

- Functional Interface란 정확히 하나의 추상 메서드가 정의된 인터페이스를 의미합니다.
- 예로는 Predicate, Comparator, Runnable 인터페이스등이 존재합니다.

#### 💡 Method Reference는 무엇인가요?

- 람다 표현식 직접 작성하는 대신해 기존의 메서드 정의를 이용하는 방법입니다. 기존의 메서드의 정의와 동일한 람다 표현식을 매번 작성하는 불편함에서 나온 기법이며, 가독성을 높일 수 있다고 생각합니다.

```java=
interface Executable {
    void doSomething(String text);
}

public static class Printer {
    static void printSomething(String text) {
        System.out.println(text);
    }
}

public static void main(String args[]) {
    Executable exe = text -> Printer.printSomething(text);//람다 표현식
    Executable exe2 = Printer::printSomething; // 메서드 레퍼런스
    exe.doSomething("do something");
    exe2.doSomething("do something");
}
```

#### 💡 Default Method 란 무엇인가요?

- 메서드 구현을 포함하는 인터페이스를 정의하기 위해 사용되어집니다. 이 인터페이스를 구현하는 클래스는 인터페이스에 디폴트 메소드도 상속받게 되기 때문에 서브클래스는 최소한의 메소드만 구현해도 됩니다. 즉, 인터페이스는 서브클래스가 구현해야 하는 최소한의 인터페이스를 유지할 수 있습니다.

```java=
interface MyInterface {
    default void printHello() {
    	System.out.println("Hello World");
    }
}
```

#### 💡 Optional 클래스는 무엇인가요?

- Optional 클래스는 NullPointerException를 관리 하기 위해 기존 객체를 감싼 Wrapper Class 입니다. Optional 인스턴스는 모든 타입의 참조 변수를 저장할 수 있습니다.

```java=
Optional<String> opt = Optional.ofNullable("Optional 객체");

if(opt.isPresent()) {
    System.out.println(opt.get());
}
```

#### 💡 업캐스팅과 다운캐스팅의 차이는 무엇인가요?

- 서브 클래스의 객체가 수퍼 클래스 타입으로 형변환되는 과정을 업캐스팅이라 합니다.
- 업캐스팅 된 변수의 타입을 서브 클래스로 변경하는 것을 다운 캐스팅이라 합니다.

#### 💡 this 키워드는 언제 사용되나요?

- 클래스의 속성과 생성자/메소드의 매개변수(input parameter)의 이름이 같은 경우
- 클래스에 오버로딩된 다른 생성자 호출

```java=
class Hello{
    String kor;
    int age;

    public Hello(String kor) {
        this.kor = kor;
    }

    public Hello(String kor, int age)
        this(kor);         //자동으로 해당 파라미터에 적합한 자신의 생성자를 호출한다.
        this.age = age;
    }
}
```
