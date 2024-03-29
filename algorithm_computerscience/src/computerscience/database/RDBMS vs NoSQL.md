## 💾 RDBMS 란?

### DBMS 란?

---

DB와 함께 많이 언급되는 DBMS는 (DataBase Management System)의 약자로, DB를 관리하고 운영하는 소프트웨어이다.

다양한 데이터가 저장된 DB는 여러 사용자 혹은 응용 프로그램에 데이터를 공유, 동시에 접근할 수 있어야 한다.

이렇게 동시에 접근할 수 있도록 해주는 것이 DBMS의 역할이다.

<br>

**RDBMS**는 DBMS의 앞에 R(Relational)이 추가된, **“관계형 데이터베이스 관리 시스템”** 이라고 한다.

RDBMS는 말그대로 RDB를 관리하는 시스템이다.

- 여기서 RDB는 관계형 데이터 모델을 기초로 두고 **모든 데이터를 2차원 테이블 형태로 표현**한 것으로,
- 즉, **관계형 데이터베이스를 생성하고 수정, 삭제, 그리고 관리할 수 있는 소프트웨어**를 의미한다.

관계형 데이터베이스(RDBMS)에서는 이러한 관계를 위해서 **외래 키(FK)**를 사용한다.

이러한 테이블 간의 관계에서 **외래 키를 이용한 테이블 간 JOIN이 가능**하다는 것이 RDBMS의 가장 큰 특징이다.

## RDBMS의 특징

---

이러한 RDBMS는 다음과 같은 특징을 가지고 있다.

- 데이터를 행과 열로 저장한다.
- 데이터의 분류, 정렬, 그리고 탐색 속도가 비교적 빠르다.
- SQL(Structured Query Language, 구조화 질의어)이라는 정교한 검색 쿼리를 통해 데이터를 다룬다.
- Transaction으로 작업의 완전성을 보장한다.
- 반드시 스키마 규격에 맞춰야 하므로 데이터 저장이 유연하지 않다.
- 부하의 분산이 어려워 수직 확장(Scale-Up)만 가능하다.
- 대표적인 RDBMS는 MySQL, SQLite, PostgreSQL, ORACLE 등이 있다.

## RDBMS의 장단점

---

RDBMS의 장점은 다음과 같다.

1. 정해진 스키마에 따라 데이터를 저장하기 때문에, 명확한 데이터 구조를 보장한다.
2. 관계는 각 데이터를 중복없이 한 번만 저장할 수 있다.

반면, RDBMS의 단점은 다음과 같다.

1. 테이블과 테이블 간 관계를 맺고 있어서 시스템이 커질 경우, JOIN 문이 많은 복잡한 쿼리가 만들어질 수 있다.
2. 성능 향상을 위해서는 서버의 성능을 향상시켜야 하는 Scale-Up 만을 지원한다.
    1. 때문에 비용이 기하급수적으로 증가할 수 있다.
3. 스키마로 인해 데이터가 유연하지 못해서 나중에 스키마가 변경될 경우 번거롭고 어려움을 겪는다.

## 🆂🆀🅻 NoSQL(Not Only SQL) 이란?

---

NoSQL은 RDBMS와 달리, **테이블 간 관계를 정의하지 않는다.**

- 데이터 테이블은 그냥 하나의 테이블로, **테이블 간 관계를 정의하지 않아 일반적으로 JOIN이 불가능**하다.

NoSQL은 빅데이터의 등장으로 데이터와 트래픽이 기하급수적으로 증가함에 따라서

RDBMS의 단점인 성능을 향상시키기 위해서는

- 서버의 성능 향상을 위해 사용되는 Scale-Up의 비용을 줄이기 위해 데이터의 **일관성은 포기**하고,
- 비용을 고려하여 여러 대의 **데이터에 분산하여 저장하는 Scale-Out**을 목표로 등장하였다.

<aside>
💡 NoSQL은 보통 문서 기반의 MongoDB로 많이 알고 있지만, MongoDB는 NoSQL의 한 종류이다.

</aside>

---

![**NoSQL의 4가지 저장 기술**](https://prod-files-secure.s3.us-west-2.amazonaws.com/c33fee58-8f40-4523-b222-c56099de30a9/fd5f30b4-83c3-4bf9-be52-a5c502adbfde/Untitled.png)

**NoSQL의 4가지 저장 기술**

---

**NoSQL**은 다양한 형태의 **4가지 저장 기술**을 지원하는데, 간단하게 알아보면 다음과 같다.

### 1. **Key-Value Database**

**Key-Value Database**에서는 데이터가 **KEY와 VALUE의 쌍으로 저장**된다.

- KEY는 VALUE에 접근하기 위한 용도로 사용되며, 값은 어떠한 형태의 데이터라도 담을 수 있다.
- 또한, 간단한 API를 제공하는 만큼 질의의 속도가 굉장히 빠른 편이다.

### **2. Document Database**

**Document Database**에서 데이터는 **KEY와 DOCUMENT 형태로 저장**된다.

- KEY-VALUE 모델과 다른 점은 VALUE가 계층적인 형태의 문서를 기반으로 저장된다는 점이다.
- 이는 객체지향에서 객체와 유사하며, 이는 하나의 단위로 취급되어 저장된다.
    - 즉, 하나의 객체를 여러 개의 테이블에 나눠 저장할 필요가 없다.
- 주요 특징은 객체를 문서 형태로 바로 저장 가능하기 때문에, 객체-관계 매핑이 필요하지 않다.
    - 또한, 검색에 최적화되어 있어, KEY-VALUE 모델의 특징과 동일하다.
- 단점은 사용이 번거롭고 쿼리가 SQL과는 다르다.
    - 문서 모델에서는 질의의 결과가 JSON이나 XML 형식으로 출력되기 때문에, 사용 방법이 RDBMS에서 사용하는 질의 결과와 다르다.

### 3. **Wide Column Database**

**Wide Column Database**는 Column-family Model 기반의 데이터베이스이다.

- 이전 모델들이 KEY-VALUE를 이용해 필드를 결정했다면, 특이하게 해당 모델을 **KEY**에서 필드를 결정한다.
    - KEY는 Row와 Column-family, Column-name을 가진다.
    - 연관된 데이터들은 같은 Column-family 안에 속해 있으며, 각자의 Column-name을 가진다.

### 4. **Graph Database**

**Graph Database**는 데이터를 Node와 Edge, Property로 **그래프 구조를 사용해 데이터를 표현 및 저장**한다.

- 객체와 관계를 그래프 형태로 표현한 것으로 관계형 모델이라고 할 수 있다.
- 또한 데이터 간의 관계가 탐색의 키일 경우에 적합하다.

## NoSQL의 특징

---

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/c33fee58-8f40-4523-b222-c56099de30a9/0ece20b9-3f79-4e4f-9aab-d43a9d0409ad/Untitled.png)

---

NoSQL은 다음과 같은 특징을 가지고 있다.

- **유연성**: 스키마 선언 없이 필드의 추가 및 삭제가 자유로운 Schema-Less 구조이다.
- **확장성**: Scale-Out(수평 확장)에 의한 서버 확장이 용이하다.
- **고성능**: 대용량 데이터를 처리하는 성능이 뛰어나다.
- **가용성**: 여러 대의 백업 서버 구성이 가능하여 장애 발생 시에도 무중단 서비스가 가능하다.

또한, NoSQL은 RDBMS의 복잡도와 용량 한계를 극복하기 위한 목적으로 등장하였다.

- 그래서 RDBMS에 비해 훨씬 더 대용량의 데이터를 저장할 수 있고,
- 분산형 구조로 데이터를 여러 대의 서버에 분산해서 저장할 수 있다.

## NoSQL의 장단점

---

NoSQL의 **장점**은 다음과 같다.

- NoSQL에서는 스키마가 없기 때문에 **유연하고 자유로운 데이터 구조**를 가질 수 있다.
    - 따라서 언제든지 저장된 데이터를 조정하고 새로운 필드를 추가할 수 있다.
- NoSQL은 **데이터 분산이 용이**하여 성능 향상을 위한 Scale-Up 뿐만 아닌, **Scale-Out**도 가능하다.

반면, NoSQL의 **단점**은 다음과 같다.

- **데이터 중복**이 발생할 수 있으며, 중복된 데이터가 변경될 경우 모든 컬렉션에서 수정을 해야 한다.
- 또한, 데이터가 여러 컬렉션에 중복되어 있어서 데이터 수정 시 모두 수정해야 해서 **속도가 느리다.**
- 스키마가 존재하기 않아 **명확한 데이터 구조를 보장하지 않고**, 데이터 구조 결정이 어려울 수 있다.
- NoSQL은 KEY 값에 대한 입 / 출력만 지원한다.

## RDBMS vs NoSQL, 어떤 상황에 어떤 데이터베이스를 사용해야 할까?

---

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/c33fee58-8f40-4523-b222-c56099de30a9/8ec0dd1e-84b2-4a62-aeb7-fda181f4cb57/Untitled.png)

---

### RDBMS(관계형 데이터베이스)를 사용해야 할 때

- 데이터베이스의 ACID 성질을 준수해야 하는 소프트웨어를 개발하는 경우
- 관계를 맺고 있는 데이터가 자주 변경되는 애플리케이션의 경우
- 변경될 여지가 없고, 명확한 스키마가 사용자와 데이터에게 중요한 경우

### NoSQL 데이터베이스를 사용해야 할 때

- 정확한 데이터의 구조를 알 수 없거나, 변경 및 확장될 가능성이 있는 경우
- 읽기는 자주 해도 데이터 변경은 자주 없는 경우
- 막대한 양의 데이터를 다뤄야 해서 데이터베이스를 수평으로 확장해야 하는 경우

### RDBMS vs NoSQL, 차이점은 무엇인가?

---

| 구분      | RDBMS                                                | NoSQL                                                      |
| --------- | ---------------------------------------------------- | ---------------------------------------------------------- |
| 데이터 저장   | 데이터를 SQL 언어를 통해 데이터를 저장                    | 4가지 저장 기술을 통해 데이터를 저장                          |
| 스키마     | 고정된 스키마가 필요<br>처리하는 데이터의 열에 대한 정보를 정해야 함 | RDBMS에 비해 유연하게 스키마를 관리<br>모든 열의 데이터를 반드시 입력하지 않아도 됨 |
| 쿼리      | 테이블 형식과 관계에 맞춰 데이터를 요청해야 함<br>요청하는 방식이 지정되어 있음<br>- SQL 언어와 같은 구조화된 쿼리를 사용 | 데이터 그룹 자체 조회에 초점을 두고 있음<br>구조화되지 않은 쿼리로 요청이 가능함<br>- 이를 UnQL이라고 함 |
| 확장성     | 수직적 확장으로 높은 메모리와 CPU를 사용<br>비용이 비싸고, 시간이 오래 걸리는 단점이 있음 | RDBMS와 반대로 수평적으로 확장<br>많은 트래픽
