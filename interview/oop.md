<details>
    <summary>자바 컬렉션이란?</summary>

    객체들을 저장하고 관리하기 위한 자료구조 인터페이스들의 모음입니다.
    대표적인 예로 List, Set, Map이 있습니다.
</details>

<details>
    <summary>Hash-Set VS Tree-Set</summary>

    정렬기능
    - TreeSet은 요소들을 자동으로 정렬된 상태로 유지합니다. 
    - 이를 위해 TreeSet은 내부적으로 이진 검색 트리(Binary Search Tree)를 사용하여 정렬된 순서로 요소를 저장합니다.
    - 때문에, TreeSet은 요소를 추가할 때마다 정렬을 수행하므로 삽입 속도가 느릴 수 있습니다. 
    - 반면, HashSet은 정렬되지 않은 상태로 요소를 저장하므로 삽입 속도가 더 빠릅니다.
    
    성능
    - TreeSet은 이진 검색 트리를 사용하여 요소의 검색, 삽입, 삭제에 대해 O(log n)의 성능을 제공합니다. 
    - 반면, HashSet은 해시 함수를 사용하여 요소의 검색, 삽입, 삭제에 대해 O(1)의 상수 시간 성능을 제공합니다. 
    - 따라서 많은 양의 데이터를 처리해야 할 경우 HashSet이 성능 면에서 우수합니다.

    결론
    -  정렬된 상태로 요소를 유지하고 검색 성능이 중요한 경우 TreeSet을 선택할 수 있으며, 
    - 정렬이 필요 없거나 빠른 검색 및 삽입 속도가 요구되는 경우 HashSet을 선택할 수 있습니다.
</details>

<details>
    <summary>Hash-Map VS Hash-Table</summary>

    동기화 지원 여부
    - HashTable은 동기화된 메소드로 구성되어 thread-safe한 동작을 보장합니다. 즉, 여러 스레드가 동시에 HashTable을 사용해도 안전합니다. 
    - 반면, HashMap은 동기화를 지원하지 않으므로 멀티스레드 환경에서 동시 접근 시 동기화 처리를 직접 해주어야 합니다.

    null 허용 여부
    - HashTable은 키와 값 모두 null을 허용하지 않습니다. 
    - 반면, HashMap은 키와 값 모두 null을 허용합니다.

    상속
    - HashTable은 Dictionary 클래스를 상속받아 구현되었으며, 이로 인해 추가적인 확장이 어렵고,  
    - HashMap은 AbstractMap 클래스를 상속받아 구현되었습니다. AbstractMap을 확장하여 커스텀 구현이 더욱 유연합니다.  

    속도
    - 일반적으로 HashMap이 HashTable보다 더 빠른 속도를 제공합니다. 
    - 이는 동기화 처리를 하지 않기 때문에 발생하는 오버헤드가 없기 때문입니다. 
    - 하지만 동시성을 보장해야 하는 멀티스레드 환경에서는 동기화된 HashTable을 사용해야 합니다.

    결론
    - 따라서, 단일 스레드 환경에서 동작하거나 직접 동기화 처리를 수행할 수 있는 경우 HashMap을 사용하는 것이 일반적입니다. 
    - 멀티스레드 환경에서 안전한 동작을 보장해야 할 경우에는 동기화된 HashTable을 사용해야 합니다.
</details>

<details>
    <summary>Hash-Map VS Hash-Set</summary>

    저장 방식
    - HashSet은 값(value)만 저장하는 컬렉션으로, 내부적으로 HashMap을 이용하여 값을 저장하고 중복 허용하지 않습니다.
    - HashMap은 키(key)와 값(value)을 쌍으로 저장하는 컬렉션으로 키는 중복을 허용하지 않으며, 값은 중복을 허용합니다.

    요소 접근
    - HashSet은 값으로만 구성되어 있기 때문에, 값을 기준으로 요소에 접근합니다. 따라서, HashSet에서 특정 요소를 찾기 위해서는 값에 대한 동등성 비교를 수행해야 합니다. 
    - HashMap은 키와 값으로 구성되어 있기 때문에, 키를 사용하여 요소에 접근할 수 있습니다. 키를 통해 빠르게 요소를 찾을 수 있습니다.

    결론
    - HashSet은 중복된 값을 허용하지 않는 값의 집합을 구현하기 위해 사용되고, 
    - HashMap은 키-값 쌍을 저장하고 관리하기 위해 사용됩니다.
</details>

<details>
    <summary>배열과 리스트의 차이</summary>

</details>

<details>
    <summary>ArrayList와 LinkedList의 차이</summary>

</details>


---

<details>
    <summary>equals와 ==의 차이는 무엇인가요?</summary>

    기본적인 동작은 똑같은데, ==은 참조 비교를 하는 동등성 비교이고 
    equals()는 내용 비교를 하는 동일성 비교입니다. 또한  오버라이딩을 할 수 있기 때문에 사용자가 원하는 논리적인 통일성을 비교할 수 있습니다.

    - 참조 비교 : 두 객체가 같은 메모리 공간을 가리키는 지 확인
    - 내용 비교 : 두 객체의 값 확인
</details>

<details>
    <summary>hashCode란 무엇인가요?</summary>

    객체의 해시 코드 값을 반환하는 메소드입니다.
    해시 코드는 객체의 유일한 정수값으로, 해시 기반의 자료구조에서 객체를 식별하는 데 사용됩니다.
    해시 코드의 기본 구현은 객체의 메모리 주소에 기반하여 해시 코드를 생성합니다.
    
    결론
    - 동일한 객체는 항상 동일한 해시 코드를 가져야 하며, 동일한 해시 코드를 가진 객체들은 동등한 객체로 취급될 수 있도록 equals() 메소드와 함께 사용됩니다.
    - 즉, hashCode()를 재정의할 때에는 equals()와 일관성을 유지해야 합니다. 
    - 예를 들어, 즉, 두 객체가 equals() 메소드로 비교했을 때 동등하다면, hashCode() 값도 동일해야 합니다.
</details>

---

<details>
    <summary>직렬화와 역직렬화 차이에 대해 말씀해주세요.</summary>

</details>

<details>
    <summary>정적 바인딩 vs 동적 바인딩</summary>

</details>

<details>
    <summary>Call By Value와 Call By Reference</summary>

</details>

---

<details>
    <summary>오버로딩과 오버라이딩의 차이</summary>

</details>

<details>
    <summary>추상 클래스와 인터페이스의 차이</summary>

</details>

---

<details>
    <summary>Error와 Exception의 차이</summary>

</details>

<details>
    <summary>Check Exception VS Uncheck Exception</summary>

</details>

---

<details>
    <summary>Java의 장/단점</summary>

</details>

<details>
    <summary>객체지향 특징</summary>

</details>

<details>
    <summary>객체지향 SOLID 원칙</summary>

</details>

---

<details>
    <summary></summary>

</details>