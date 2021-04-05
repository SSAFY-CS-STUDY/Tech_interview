# 21.04.05
* Java Collections Framework
* Map, Set, List 인터페이스 구현체 종류
* Annotation
* String vs StringBuilder vs StringBuffer

## 주요 질문

#### 💡 [질문1](#개념1)
   * 답변
   
#### 💡 질문2
   * 답변
   
#### 💡 질문3
   * 답변


<br/>

## ⭐ 개념 정리

### Java Collections Framework
   * 컬렉션 프레임워크: 값을 담는 그릇 (컨테이너)
   * Collections Framework: 다양한 상황에서 사용할 수 있는 다양한 컨테이너
   ![image](https://user-images.githubusercontent.com/39117025/113572483-3fb1c900-9653-11eb-935c-19c66157a8ea.png)

   >https://opentutorials.org/course/1223/6446
<br/>

### Map, Set, List 인터페이스 구현체 종류
#### Map
* (key, value) 쌍으로 값을 저장하는 컬렉션
``` java
import java.util.*;
 
public class MapDemo {
 
    public static void main(String[] args) {
       // String: key
       // Integer: value
        HashMap<String, Integer> a = new HashMap<String, Integer>();

        //데이터 추가
        a.put("one", 1);
        a.put("two", 2);
        

        //key 값으로 데이터 가져옴
        System.out.println(a.get("one")); //1
        System.out.println(a.get("two")); //2
          
      
        iteratorUsingForEach(a);
        iteratorUsingIterator(a);
    }

    static void iteratorUsingForEach(HashMap map){
        Set<Map.Entry<String, Integer>> entries = map.entrySet();
        for (Map.Entry<String, Integer> entry : entries) {
            System.out.println(entry.getKey() + " : " + entry.getValue());
        }
    }
     
    static void iteratorUsingIterator(HashMap map){
        Set<Map.Entry<String, Integer>> entries = map.entrySet();
        Iterator<Map.Entry<String, Integer>> i = entries.iterator();
        while(i.hasNext()){
            Map.Entry<String, Integer> entry = i.next();
            System.out.println(entry.getKey()+" : "+entry.getValue());
        }

}
```

#### Set
* 집합의 특징을 가지고 있다.
* 순서가 없고, 중복되지 않는다.

``` java
import java.util.*;
 
public class SetDemo {
 
    public static void main(String[] args) {
       
       //선언
        HashSet<Integer> A = new HashSet<Integer>();
        // 값 넣기
        A.add(1);
        A.add(2);
        A.add(3);
         
        HashSet<Integer> B = new HashSet<Integer>();
        B.add(3);
        B.add(4);
        B.add(5);
         
        HashSet<Integer> C = new HashSet<Integer>();
        C.add(1);
        C.add(2);
         
         
        // 탐색
        Iterator hi = A.iterator();
        while(hi.hasNext()){
            System.out.println(hi.next());
        }
    }
 
}
```

* 부분집합
   * A.containsAll(B) -> false
   * A.containsAll(C) -> true

   ![image](https://user-images.githubusercontent.com/39117025/113573503-37f32400-9655-11eb-940d-d7380cf585d3.png)

* 합집합
   * A.addAll(B)

   ![image](https://user-images.githubusercontent.com/39117025/113573480-2f025280-9655-11eb-80ef-c01603b3c930.png)

* 교집합
   * A.retainAll(B)
   
   ![image](https://user-images.githubusercontent.com/39117025/113573457-24e05400-9655-11eb-9cb7-c13014e2945c.png)

* 차집합
   * A.removeAll(B)

   ![image](https://user-images.githubusercontent.com/39117025/113573424-1bef8280-9655-11eb-933d-202fedaa1ed6.png)

#### 리스트
* 데이타의 순서가 있다.
* 중복을 허용하지 않는다.

```java
import java.util.*;
 
public class ListDemo {
 
    public static void main(String[] args) {
        ArrayList<String> al = new ArrayList<String>();
        al.add("one");
        al.add("two");
        al.add("two");

        Iterator ai = al.iterator();
        while(ai.hasNext()){
            System.out.println(ai.next());
        }
    }
}
```
<br/>
> https://opentutorials.org/course/1223/6446

### Annotation
   * 속성이나 클래스에 역할을 부여해서 결정해주는 것입니다. 
   * 구독성과 체계적인 소스코드를 작성하는 데 도움을 줍니다.
   * 메타-테이터(Meta-Data) : 데이터를 위한 데이터를 의미하며, 풀어 이야기하면 한 데이터에 대한 설명을 의미하는 데이터. (자신의 정보를 담고 있는 데이터)
> https://www.nextree.co.kr/p5864/
> https://elfinlas.github.io/2017/12/14/java-annotation/
<br/>  

### String vs StringBuilder vs StringBuffer
#### String 
* 불변 속성을 가집니다.
* 문자열을 수정하는 시점에 새로운 String 인스턴스가 생성됩니다.

   ![image](https://user-images.githubusercontent.com/39117025/113574335-d59b2300-9656-11eb-87d9-d9d2190782ee.png)

* 반면, StringBuilder 와 StringBuffer는 가변 속성을 가집니다.
* .delete(), .append() 를 사용해서 문자열을 변경할 수 있습니다.

   ![image](https://user-images.githubusercontent.com/39117025/113574452-185cfb00-9657-11eb-9dc1-60b53160dbef.png)

* StringBuffer는 동기화를 지원하므로 멀티쓰레드 환경에서 안전합니다.
* StringBuilder는 동기화를 지원하지 않기 때문에 멀티쓰레드 환경에서는 적합하지 않지만, 단일 쓰레드 환경에서는 적합합니다.

   ![image](https://user-images.githubusercontent.com/39117025/113574551-49d5c680-9657-11eb-83a8-a3b4f6533d4f.png)
> https://ifuwanna.tistory.com/221


<br/>



