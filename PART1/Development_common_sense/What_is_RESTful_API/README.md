#### 1-1-3. RESTful API란?


<hr>

**RESTful API**

RESTful API에 대한 역량은 많은 기업에서 요구하고, 수 많은 블로그에서 설명되어 있다.
대체 RESTful API가 무엇이고, 어떻게 사용해야할까?



- **정의**

REST의 사전적 의미는 다음과 같다.
'REST(Representational State Transfer)는 WWW과 같은 분산 하이퍼미디이 시스템을 위한 소프트웨어 아키텍처의 한 형식이다.'
이러한 형식을 잘 지킬수록 'RESTful'하다고 표현하게 된다.

- **구성**
  - Resource(자원): URI
  - Verb(행위): HTTP Method
  - Representations(표현)



- **REST 6원칙**

1. Uniform Interface: 일관적인 인터페이스로 분리되어야 한다.
2. Stateless: 각 요청 간 클라이언트의 콘텍스트가 서버에 저장되어서는 안된다.
3. Caching: WWW에서와 같이 클라이언트는 응답을 캐싱할 수 있어야 한다.
4. Client-Server: 아키텍처를 작은 단위로 분리함으로써 각 파트가 독립적으로 개선될 수 있도록 해준다.
5. Hierarchical(Layered) system:  클라이언트가 대상 서버에 직접 혹은 중간 서버를 통해 연결됐는지 여부를 알 수 없으며, 중간 서버는 부하를 분산(load balancing)시켜 규모 확장에 유용하다.
6. Code on demand: 서버에서 클라이언트가 실행시킬 수 있는 로직을 전송하여 기능을 확장



- **RESTful한 API를 디자인 한다는 것**

1. 리소스와 행위를 명시적이고 직관적으로 분리한다.
   - 리소스는 URI로 표현되며 리소스가 가리키는 것은 명사로 표현
   - 행위는 HTTP Method로 표현하고, GET, POST, PUT, DELETE를 분명한 목적으로 사용
2. Message는 Header와 Body를 명확하게 분리해서 사용한다.
   - header 와 body 는 http header 와 http body 로 나눌 수도 있고,
     http body 에 들어가는 json 구조로 분리할 수도 있다.
3. API 버전을 관리한다.
   - 환경이 변하기 때문에 API signature가 변경될 수 있음에 유의한다.
   - 특정 API를 변경할 때는 반드시 하위 호환성을 보장해야 한다.
4. 서버와 클라이언트가 같은 방식을 사용해서 요청하도록 한다.
   - URI가 플랫폼 중립적이어야 한다.



- **장점**

1. Open API 제공이 쉽다.
2. 멀티플랫폼 지원 및 연동이 용이하다.
3. 원하는 타입으로 데이터를 주고 받을 수 있다.
4. 기존 웹 인프라(HTTP)를 그대로 사용할 수 있다.
5. 메시지만으로 의도를 명확하게 파악할 수 있다.



- **단점**

1. 사용할 수 있는 메소드가 4가지밖에 없어 세부 기능 작성이 제한된다.
2. 표준이 존재하지 않아 공식화 된 API 디자인 가이드가 존재하지 않는다.
3. 분산 환경에는 부적합하다.
4. HTTP통신 모델에 대해서만 지원한다.

<hr>

**Keyword**

- **네트워크 아키텍처**
  자원을 정의하고 자원에 대한 주소를 지정하는 방법 전반
