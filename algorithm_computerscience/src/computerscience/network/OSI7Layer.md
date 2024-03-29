## OSI(Open Systems Interconnection) 7 Layers

### 네트워크 통신 모델: OSI vs TCP/IP

---

'OSI 7 계층'과 'TCP/IP 프로토콜'은 둘 다 계층형 구조로 네트워크를 설명한다는 공통점이 있지만, TCP/IP 프로토콜 계층과 OSI 7 계층은 정확하게 일치하지 않는다.

따라서 둘의 차이점을 간단히 설명하면, OSI 모델은 장비 개발과 통신 자체를 어떻게 표준으로 잡을지 사용되고, 반면, 실질적인 통신을 설명할 때는 TCP/IP 모델을 주로 사용한다고 생각하면 된다.

- ❗️ 네트워크 통신이 이루어지는 방법


    **[ 네트워크 통신 과정 ]**
    
    ---
    
    예를 들어, ‘돌고래’와 ‘문어’가 이메일을 주고 받는다고 가정해보자.
    
    1. ‘돌고래’가 이메일을 작성하고 보내기를 누르면, 이 정보는 응용 계층에서 시작해서 하위 계층으로 전달되는 Top-Down 방식을 따른다.
    2. 이렇게 처리된 정보는 물리 계층 즉, 1계층을 통해 실제 네트워크 매체(이더넷 케이블, 광섬유 케이블, 무선 신호(Wi-Fi) 등)를 통해 전송된다.
    3. 이 정보는 ‘문어’의 물리 계층에 도착하고, 이후 상위 계층으로 전달되는 Bottom-Up 방식을 따른다.
    4. 각 계층은 자신의 역할에 따라 정보를 해석하고 필요한 처리를 수행하며, 이 정보는 최종적으로 ‘문어’의 응용 계층에 도달하여 ‘문어’가 이메일을 확인할 수 있게 된다.

### OSI 7 계층이란?

---

OSI 모델은 국제표준화기구(ISO)에서 개발한 모델로 네트워크 통신 과정을 7개 계층으로 구성된 것으로, 각 계층이 독립적으로 작동하고 각자의 역할을 수행한다.

때문에 OSI 모델은 특정 네트워킹 시스템에서 일어나는 일을 계층을 활용해 시각적으로 쉽게 설명할 수 있다.

만약, 네트워크 관리자가 각 계층에서 일어나는 문제를 식별하면 그로 인해 발생하는 네트워크 문제를 빠르게 파악하고 해결할 수 있고, 문제의 원인이 어디에 있는지 범위를 좁히는데 도움이 된다.

<aside>
💡 예를 들면, 물리적인 문제인지 아니면 응용 프로그램과 관련이 있는지 쉽게 파악할 수 있다.

</aside>

- **Protocol, 프로토콜**


    프로토콜은 컴퓨터 네트워크나 통신 시스템에서 데이터를 주고받기 위한 **규칙들의 집합**이다.
    
    ---
    
    <aside>
    📌 즉, 프로토콜은 메세지를 주고 받는 양식과 규약의 체계이다.
    
    </aside>
    
    **[ 프로토콜의 구성 요소 ]**
    
    ---
    
    - **문법:** 데이터의 형식과 구조를 정의한다.
    - **의미:** 데이터의 의미와 해석 방법을 정의한다.
    - **타이밍:** 데이터 전송의 속도나 순서, 지연 시간 등과 관련되 규칙들을 정의한다.
    - **메세지 포맷:**
        - 헤더: 메세지의 제목, 길이, 형식 등의 정보를 담고 있다.
        - 데이터: 실제 전송되는 정보를 담고 있다.
    - **규칙과 절차:**
        - 데이터 전송 방법: 데이터가 어떤 순서로 전송되어야 하는지에 대한 규칙이다.
        - 에러 처리 방법: 데이터가 손실되거나 손상되었을 때의 대응 방법을 정의한다.


### OSI 모델의 특징

---

- OSI 모델은 **프로토콜을 기능별**로 나눈 모델이다.
- OSI 모델의 하위 계층들은 하드웨어로, 상위 계층들은 소프트웨어로 구현된다.
- OSI 모델의 각 계층은 하위 계층의 기능만을 이용하고, 상위 계층에게 기능을 제공한다.
- OSI 모델은 **각 기능별**로 **계층화된 '프로토콜 스택'을 포함**하고 있다.

- **Protocol Stack, 프로토콜 스택**


    프로토콜 스택이란 여러 프로토콜의 조합으로, 데이터가 네트워크를 통해 정보를 주고받기 위해 필요한 규칙들을 모아놓은 것을 말한다.
    
    이는 송신자에서 수신자까지 데이터의 이동 경로와 방법을 결정하는 중요한 요소이다.
    
    **[ 프로토콜 스택의 역할 ]**
    
    ---
    
    - 계층화: 프로토콜을 여러 계층으로 나누어 관리함으로써, 복잡한 통신 문제를 단순한 문제로 분해하고 해결할 수 있게 한다.
    - 모듈화: 각 계층은 자신에게 주어진 역할에만 집중하며, 다른 계층과 상호작용함으로써 네트워크 기능을 제공한다.
    - 상호운용성: 서로 다른 종류의 하드웨어와 소프트웨어 사이에서도 효과적인 통신을 가능하게 한다.
    
    - ❗️ 프로토콜 스택이 계층화된 구조로 되어 있는 이유
        
        프로토콜 스택의 계층화된 구조 덕분에 각 프로토콜이 독립적으로 동작할 수 있고, 하나의 계층에서 문제가 발생해도 다른 계층에 영향을 미치지 않는다는 이점이 있다.
        
    
    **[ OSI 7 계층별 프로토콜 ]**
    
    | OSI LAYERS | PROTOCOLS |
    | --- | --- |
    | APPLICATION LAYER, 응용 계층 | HTTP, FTP, IRC, SSH, DNS |
    | PRESENTATION LAYER, 표현 계층 | SSL, FTP, IMAP, SSH |
    | SESSION LAYER, 세션 계층 | VARIOUS API’S, SOCKETS |
    | TRANSPORT LAYER, 전송 계층 | TCP, UDP, ECN, SCTP, DCCP |
    | NETWORK LAYER, 네트워크 계층 | IP, IPSec, ICMP, IGMP |
    | DATA-LINK LAYER, 데이터-링크 계층 | Ethernet, SLIP, PPP, FDDI |
    | PHYSICAL LAYER, 물리 계층 | Coax, Fiber, Wireless |
    
    <aside>
    📌 다양한 계층의 프로토콜들을 모두 합해서 **'프로토콜 스택'**이라고 한다.
    
    </aside>


### 1. Physical Layer(물리 계층)

---

<aside>
📌 **물리 계층은 '신호로 변환하여 전송하는 계층'이다.**

</aside>

---

- 시스템의 전기적, 기계적 특성을 이용하여, 통신 케이블로 전기적 신호를 전송한다.
- 단순 데이터 전달 역할만 하며, 알고리즘이나 오류 제어 기능은 존재하지 않는다.
- 물리 계층의 대표적인 예는 '케이블, 무선 신호'가 있다.
- 전송 단위는 'Bit'이다.

예를 들면, 네트워킹 문제가 발생하면 많은 네트워크 전문가가 물리 계층으로 바로 가서 모든 케이블이 제대로 연결되어 있는지, 라우터나 스위치 또는 컴퓨터에서 전원 플러그가 빠지지 않았는지 확인한다.

### 2. Data-Link Layer(데이터-링크 계층)

---

<aside>
📌 **데이터 링크 계층은 '네트워크에서 두 장치 간 데이터 전송을 담당하는 계층'이다.**

</aside>

---

- 물리적 주소 기반으로 데이터 전송형태를 결정하고, 물리적 링크를 통해 데이터를 신뢰할 수 있게 전송한다.
    - Point to Point 간 신뢰성 있는 전송을 보장하기 위해 CRC 기반의 오류 제어와 흐름 제어가 필요하다.
- 네트워크 위의 개체들, 즉 상위 계층 간 데이터를 전달하고, 물리 계층에서 발생할 수 있는 오류를 찾아내며 수정하는 데 필요한 기능적, 절차적 수단을 제공한다.
- 데이터-링크 계층은 두 개의 부계층, 즉 MAC 계층과 LLC 계층으로 나뉜다.
- 데이터-링크 계층의 대표적인 예는 '이더넷'이 있다.
- 전송 단위는 'Frame'이다.

- **MAC 주소**


    > MAC 주소는 네트워크 장비가 데이터를 주고받을 때 이를 **식별하기 위한 고유한 주소**를 말한다.
    > 
    
    ---
    
    - 이 주소는 네트워크 인터페이스 카드(NIC)에 하드웨어적으로 부여되며,
    - 이더넷과 같은 LAN에서 장비를 구분하는 데 주로 사용된다.
    
    <aside>
    📌 즉, 각 네트워크 장비는 고유한 MAC 주소를 가지며, 이를 식별하기 위한 고유한 주소이다.
    
    </aside>

- **Frame, 프레임**


    데이터-링크 계층에서 데이터를 전송할 때, 이 데이터는 'Frame'이라는 단위로 조직화된다.
    
    각 프레임은 다음과 같이 구성되어 있다.
    
    ---
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/c33fee58-8f40-4523-b222-c56099de30a9/b12cd9e7-cb1b-490c-b669-cd5244cd37ed/Untitled.png)
    
    1. **Preamble:** 프레임의 시작을 알리는 부분으로, 싱크를 맞추는 역할을 한다.
        1. 비트 패턴으로 구성되어 있다.
        2. 수신측 장비가 프레임의 시작을 인지하고 데이터를 동기화하는 데 사용된다.
    2. **MAC Destination:** 목적지 MAC 주소를 나타낸다.
        1. 데이터가 전송될 대상 장비의 MAC 주소가 여기에 포함된다.
    3. **MAC Source:** 출발지 MAC 주소를 나타낸다.
        1. 데이터를 전송하는 장비의 MAC 주소가 여기에 포함된다.
    4. **Ethertype/Length:** 해당 필드는 두 가지 역할을 수행한다.
        1. Ethertype은 상위 프로토콜(네트워크 계층)을 나타내는 정보를 말한다.
        2. Length는 페이로드의 길이를 나타낸다.
    5. **Data/Payload:** 실제 전송할 데이터를 포함하는 부분이다.
        1. 해당 부분에는 네트워크 계층에서 받은 패킷이 들어간다.
    6. **Frame Check Sequence, FCS:** 오류 검출을 위한 필드이다.
        1. 프레임의 나머지 부분을 검사하여 생성된 체크값이 포함된다.
        2. 수신측에서는 이 값을 사용하여 프레임에 오류가 있는지 확인한다.
- **MAC, LLC 계층**


    ![스크린샷 2024-01-10 오후 4.27.57.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c33fee58-8f40-4523-b222-c56099de30a9/0ff24298-69ee-4274-b73a-9a12b41d37dd/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-01-10_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_4.27.57.png)
    
    > **MAC(), 매체 접근 제어 계층**
    > 
    
    ---
    
    - MAC 계층은 물리 계층과 연결된 부분으로, 네트워크의 물리적 매체(케이블 무선 등)에 데이터를 전송하는 방법을 제어한다.
    - 이때, 여러 장치가 동시에 데이터를 전송하려고 할 때 생기는 충돌을 방지하는 역할도 한다.
        - 둘 이상의 호스트에서 동시 데이터 전송을 시도하면 충돌 발생 → 일정 시점 후에 재전송하도록 한다.
    - 또한, MAC 주소라고 불리는 고유한 식별자를 사용하여 네트워크 내의 각 장치를 구분하기도 한다.
    
    > **LLC(), 논리적 연결 제어 계층**
    > 
    
    ---
    
    - LLC 계층은 네트워크 계층과 연결된 부분으로, 데이터 흐름을 제어하고, 오류 복구를 담당한다.
        - (데이터-링크 계층과 네트워크 계층 사이의 인터페이스 역할을 한다.)
    - 또한, MAC 계층에서 받은 정보를 네트워크 계층으로 전달하는 역할도 한다.
    
    <aside>
    📌 따라서, 데이터-링크 계층에서는 MAC 계층과 LLC계층이 협력하여 데이터 전송, 오류 관리와 흐름 제어 등의 역할들을 수행한다.
    
    </aside>

- **CRC**


    **CRC(Cyclical Redundancy Check)**는 데이터 링크 계층에서 데이터 오류를 수학적으로 검출한다.
    
    (오류 검출을 위해 체크값을 사용하여 오류 여부를 확인한다.)
    
    1. 송신자의 시스템은 수신자의 시스템과 체크값을 정한다.
    2. 송신자가 보내려고 하는 데이터를 체크값으로 나눈다.
    3. 송신자는 데이터를 체크값으로 나누어 만들어진 나머지 값을 데이터의 끝에 붙여서 전송한다.
    4. 수신자는 받은 데이터를 체크값으로 나누어 도출되는 나머지를 비교한다.
        1. 일치하면 수신하고
        2. 일치하지 않으면 송신자에게 나머지 값이 일치될 때까지 재전송 요구 신호(NAK)을 보낸다.
    
    이렇게 위와 같은 방식으로 CRC는 데이터의 정확성을 보장하게 된다.


### 3. Network Layer(네트워크 계층)

---

<aside>
📌 **네트워크 계층은 '네트워크를 논리적으로 구분하고 연결하는 계층'이다.**

</aside>

---

- 네트워크 계층은 데이터의 전송 경로를 찾아주는 역할을 한다.
    - 다양한 길이의 패킷을 네트워크를 통해 전달하고,
      그 과정에서 전송 계층이 요구하는 서비스 품질(QoS)을 제공하기 위한 기능적, 절차적 수단을 제공한다.
    - 즉, 데이터가 여러 노드를 거치면서 가장 효율적인 길을 찾는 ‘안내자’ 역할을 수행한다.
- 데이터를 안전하게 전달하기 위해 라우팅, 흐름 및 오류 제어, 세그멘테이션, 인터네트워킹 등을 수행한다.
- 네트워크 관리자가 직접 IP 주소를 할당하고 관리하는 구조를 가지며, 계층적이다.
- 네트워크 계층의 대표적인 예는 'IP 프로토콜'이 있다.
- 전송 단위는 'Datagram(Packet)'이다.

- **IP Protocol, IP 프로토콜**


    ![스크린샷 2024-01-10 오후 4.46.26.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/c33fee58-8f40-4523-b222-c56099de30a9/aec33e47-9344-460f-9403-cb65b0c2df8f/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-01-10_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_4.46.26.png)
    
    > **IP 프로토콜**
    > 
    
    ---
    
    - IP 프로토콜은 컴퓨터 프로토콜(Internet Protocol)의 약자로, 컴퓨터 네트워크에서 데이터를 주고받는 방법을 정의하는 규약이다.
    - IP 프로토콜은 데이터를 패킷 단위로 분할하고, 이 패킷들을 목적지까지 안전하게 전달하는 것이다.
    - 각 패킷에는 출발지와 목적지의 IP 주소가 포함되어 네트워크 상의 다양한 경로를 통해 목적지까지 전송될 수 있다.
        - Source IP Address: 패킷이 생성된 출발지의 IP 주소를 나타낸다.
        - Destination IP Address: 패킷이 도착해야 할 목적지의 IP 주소를 나타낸다.

- ❗️ 네트워크 계층에서 수행하는 여러 기능


    > **Routing, 라우팅**
    > 
    
    ---
    
    - 라우팅 기능은 데이터를 송신자에서 수신자까지 전달하기 위한 **최적의 경로를 결정**하는 과정이다.
        - 해당 라우팅 기능을 수행하는 장치인 라우터는 라우팅 정보를 참조하여 **경로를 설정**하고, 데이터 패킷을 중계함으로써 **서로 다른 네트워크들을 연결**한다.
    
    > **Flow Control, 흐름 제어**
    > 
    
    ---
    
    - 흐름 제어는 송신측과 수신측 사이의 데이터 전송 속도를 조절하는 기능이다.
    - 수신측이 처리할 수 있는 속도보다 빠르게 데이터가 전송되면 패킷 손실이 발생할 수 있으므로, 
    이를 방지하기 위해 흐름 제어가 필요하다.
        - 주로 전송 계층에서 수행되는 작업이다.
    
    > **Error Control, 오류 제어**
    > 
    
    ---
    
    - 오류 제어는 데이터 전송 중 발생할 수 있는 오류를 감지하고, 필요한 경우 재전송을 요청하는 기능이다.
    - 패킷의 체크섬을 통해 오류를 감지하고, 오류가 발견되면 송신측에 재전송을 요청한다.
        - 주로 전송 계층에서 수행되는 작업이다.
    
    > **Segmentation, 세그멘테이션**
    > 
    
    ---
    
    - 세그멘테이션은 큰 데이터를 여러 개의 작은 패킷으로 분할하는 과정이다.
    - 데이터를 효율적으로 전송하기 위해 필요하며, 각 패킷은 독립적으로 라우팅되어 목적지에 도착한 후 다시 재조립된다.
    
    > **Internetworking, 인터네트워킹**
    > 
    
    ---
    
    - 인터네트워킹은 서로 다른 네트워크 간에 통신을 가능하게 하는 기능이다.
        - 즉, 네트워크 간 통신의 ‘다리’ 역할을 한다.
    - 예를 들어, 이더넷과 Wi-Fi와 같이 서로 다른 네트워크 간에도 데이터를 전송할 수 있게 한다.
        - IP 프로토콜을 통해 가능하며, IP는 다양한 네트워크 기술 위에서도 동작할 수 있다.
- ❗️ 네트워크 관리자가 직접 IP 주소를 할당 및 관리하는 이유


    1. **유일성 보장**: IP 주소는 전 세계적으로 유일해야 한다. 따라서 네트워크 관리자가 직접 IP 주소를 할당하면 중복되는 IP 주소 할당을 방지할 수 있다.
    2. **네트워크 구성 및 보안 관리**: 네트워크 관리자가 IP 주소를 직접 할당하면, 네트워크의 구성을 더 효율적으로 관리할 수 있다. 
        
        예를 들어, 특정 IP 주소 범위를 가진 호스트들을 같은 네트워크 세그먼트에 배치할 수 있다. 또한, 특정 IP 주소를 가진 호스트에 대한 접근 제어 등 보안 관리도 용이하다.


### 4. Transport Layer(전송 계층)

---

<aside>
📌 **전송 계층은 '서비스를 구분하고 데이터의 전송 방식을 담당하는 계층'이다.**

</aside>

---

- 양 끝단(End to end)의 사용자들에게 신뢰성 있고 정확한 데이터를 전달하는 역할을 한다.
    - 이를 통해 송신자와 수신자가 데이터 전송의 성공 여부에 대해 생각하지 않아도 된다.
- 전송 계층은 '시퀸스 넘버'를 기반으로 오류를 제어한다.
- 전송 계층은 특정 연결의 유효성을 제어하고, 일부 프로토콜은 상태 개념이 있고, 연결 기반이다.
- 전송 계층의 대표적인 예는 'TCP, UDP'가 있다.
- 전송 단위는 'Segment'이다.

- **Sequence Number, 시퀸스 넘버**


    **시퀸스 넘버**는 패킷이 네트워크를 통해 전송될 때, 각 패킷에 할당되는 고유한 숫자이다.
    
    이는 패킷이 올바른 순서로 전송되고 수신되었는지 확인하는 데 사용된다.
    
    만약, 패킷이 손실되거나 순서가 잘못되었다면, 시퀸스 넘버를 통해 이를 감지하고, 필요한 경우 재전송을 요청하거나 순서를 재배열할 수 있다.
    
    이러한 과정은 네트워크에서 데이터의 신뢰성을 보장하는 데 중요한 역할을 한다.

- **TCP, UDP**


    **TCP(Transmission Control Protocol)**는 네트워크에서 데이터를 안전하게 전달하기 위한 규약이다.
    
    이는 **'연결 지향적'**이라는 특징을 가지며, 데이터 전송 전후로 송수신자 사이의 연결 설정과 해제를 관리한다.
    
    <aside>
    📌 **TCP: 신뢰성 있는 연결지향형 프로토콜**
    
    신뢰성이 있다는 것은 해당 패킷에 대한 오류처리나 재전송 따위로 에러를 복구하는 것이다.
    그 때문에 TCP의 헤더에는 붙는 정보들이 많다.
    
    </aside>
    
    **[ TCP ]**
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/c33fee58-8f40-4523-b222-c56099de30a9/c1fb98fa-a770-4ff8-92cf-0aabb382dcb3/Untitled.png)
    
    **[ UDP ]**
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/c33fee58-8f40-4523-b222-c56099de30a9/a209474c-4ee0-473e-ae73-473223b11a8b/Untitled.png)
    
    해당 과정에서 TCP는 각 단계의 상태를 추적하고 관리하는 **'상태 개념'**을 사용한다.
    
    즉, 데이터 전송 중에는 각 패킷의 전송 상태를 체크하고, 필요한 경우 재전송을 요청하여 패킷이 정확하게 전달되도록 한다.
    
    이렇게 TCP는 상태를 기반으로 데이터의 전송을 관리하며, 이를 통해 데이터의 신뢰성을 보장한다. 
    
    이와 같이 상태 추적 및 관리 기능을 가진 프로토콜을 **'상태 개념'**이 있는 프로토콜이라고 부른다.
    
    반면, **UDP(User Datagram Protocol)**는 '연결 없음'이라는 특징을 가지며, 데이터의 신속한 전송을 중요시하는 경우 주로 사용한다.
    
    <aside>
    📌 **UDP: 비신뢰성 비연결형 프로토콜**
    
    패킷을 잃거나 오류가 있어도 대처하지 않아서 UDP 헤더는 간단한 구조를 가지고 있다.
    
    </aside>
    
    <aside>
    📌 즉, 신뢰성이 요구되는 애플리케이션에서는 TCP를 사용하고, 
    간단한 데이터를 빠른 속도로 전송하고자 하는 애플리케이션에서는 UDP를 사용한다.
    
    </aside>


### 5. Session Layer(세션 계층)

---

<aside>
📌 **세션 계층은 '응용 프로그램 간의 연결을 지원해주는 계층'이다.**

</aside>

---

- 네트워크 상에서 두 장치 간의 통신을 관리하는 역할을 한다.
    - 이는 통신 장치 간의 상호작용과 동기화를 제공하여 양 끝단의 통신을 원활하게 만들어준다.
- 세션 계층은 동시 송수신 방식, 반이중 방식, 전이중 방식 등의 다양한 통신 방식을 지원하며, 세션 설정, 유지, 종료, 전송 중단시 복구 등의 작업을 수행한다.
- 두 컴퓨터 또는 서버 간 대화가 필요할 때, 세션 계층은 TCP/IP 세션을 생성하고 종료하는 역할을 담당한다.
- 전송 단위는 'Message'이다.

- **동시 송수신(Simplex), 반이중(Half-Duplex), 전이중 방식(Full-Duplex)**


    **동시 송수신 방식(Simplex)**은 한 방향으로만 통신이 이루어지는 방식이다.
    
    예를 들어, 라디오나 TV 방송과 같이 송신자에서 수신자로의 단방향 통신을 말한다. 이 경우, 수신자는 송신자에게 정보를 전달할 수 없다.
    
    **반이중 방식(Half-Duplex)**은 양방향 통신이 가능하지만, 동시에는 한 방향으로만 통신이 이루어진다. 즉, 송신과 수신이 번갈아 가며 이루어진다. 
    
    예를 들어, 무전기의 경우 한 사람이 말하면 다른 사람은 듣고, 그 반대도 마찬가지이다.
    
    **전이중 방식(Full-Duplex)**은 양방향 통신이 동시에 이루어진다. 즉, 송신과 수신이 동시에 이루어져 서로 독립적으로 통신할 수 있다.
    
    예를 들어, 전화 통화의 경우 양쪽이 동시에 말하고 들을 수 있다.


### 6. Presentation Layer(표현 계층)

---

<aside>
📌 **표현 계층은 '데이터의 변환 작업을 하는 계층'이다.**

</aside>

---

- 표현 계층은 다양한 코딩 체계 간의 번역을 담당해 응용 계층에서 데이터 표현에 따른 부담을 덜어준다.
    - 이를 위해 ASCII, JPEG, MPEG 등의 데이터 형식을 상호 변환한다.
- 표현 계층은 전송되는 데이터에 대해 인코딩, 디코딩, 암호화, 코드 변환 등을 수행한다.
    - 이는 데이터의 안전성을 보장하고, 다양한 시스템 간의 데이터 이해를 돕는다.
- 전송 단위는 'Message'이다.

### 7. Application Layer(응용 계층)

---

<aside>
📌 **응용 계층은 '사용자 인터페이스를 제공하는 계층'이다.**

</aside>

---

- 응용 계층은 OSI 모델에서 최종 사용자에게 가장 가까운 계층으로, 이 계층에서 작동하는 응용 프로그램은 사용자와 직접적으로 상호작용한다.
    - 웹 브라우저인 크롬, 파이어폭스, 사파리 등 그리고 통신 프로그램인 스카이프, 아웃룩 등이 대표적이다.
- 응용 계층은 응용 프로세스와 직접적으로 연관되어, 다양한 응용 서비스를 수행한다.
    - 이는 관련된 응용 프로세스들 간의 데이터 전환을 촉진하며, 사용자에게 편리한 서비스를 제공한다.
- 응용 계층의 대표적인 예는 'HTTP, FTP'가 있다.
- 전송 단위는 'Message'이다.

- **응용 프로그램, 응용 프로세스**

  **응용 프로그램**은 사용자가 컴퓨터를 통해 특정 작업을 수행하기 위해 사용하는 소프트웨어이다.

  웹 브라우저: (크롬, 파이어폭스), 텍스트 에디터: (워드, 메모장), 이메일 클라이언트(아웃룩), 그래픽 툴(포토샵) 등이 대표적인 예시이다.

  이들은 사용자의 명령을 받아 컴퓨터에게 수행하도록 지시하는 역할을 한다.

  **응용 프로세스**는 응용 프로그램이 실행되어 실제로 메모리 상에 올라가 작동하고 있는 상태를 말한다.

  즉, 응용 프로그램이 사용자의 요청에 의해 실행되면, 운영체제는 해당 프로그램에 메모리를 할당하고, 이를 응용 프로세스라고 한다.

  응용 프로세스는 사용자의 요청을 처리하고, 필요한 계산을 수행하며, 결과를 사용자에게 제공한다.

  따라서, 응용 프로그램은 사용자가 특정 작업을 수행하기 위해 사용하는 소프트웨어를,

  응용 프로세스는 그 소프트웨어가 실제로 실행되는 상태를 가리킨다.