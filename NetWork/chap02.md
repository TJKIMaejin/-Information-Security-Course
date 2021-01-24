### 네트워크 통신규약

#### **통신 규약**  =  Protocol

  * 표준화된 통신 규약
  
  * 컴퓨터나 네트워크 장비가 서로 통신하기 위해서 미리 정해놓은 약소
  
  * 통신을 원하는 두 개체간 통신에 대한 절차/규범/규정/규약/규칙
  
#### IETF (Internet Engineering Task Force, 국제 인터넷 표준화 기구)

  *  네트워크 통신을 위한     ** 프로토콜 제정 및 표준화를 담당하는 국제 기구 **
  
### 네트워크 모델
 
  * 통신이 일어나는 절차를 각 기능별로 ** 모듈화시켜 ** 만들어 놓은 계층적인 구조
  
  * OSI 7 Layer 참조 모델
    
    * 각 게층의 역할에 맞는 개발 참조
    
    * Troubleshooting시 참조
    
    * 학습 목적으로 사용
    
    
  * TCP/IP 모델
    
    * 실제 통신에 사용되는 모델
    
    
  * Network Model
    
    * 1~4 계층: 하위 계층(= 하드웨어 계층)
      
      * 데이터 전달 계층으로 주로 네트워크 분야
      
    * 5~7 계층: 상위 계층(= 소프트웨어 계층)
      
      * 데이터 생성 계층으로 주로 소프트 웨어 개발 분야에서 참조
      
      
       ||     OSI 7계층             | TCP/IP Protocol                       |
       |:--- |:---: | :---: |   
       | 7층 (데이터 생성)           |   Application layer           |  telnet ,FTP, DHCP,TFTP,HTTP,SMTP,DNS,SNMP           | 
       | 6층 (인코딩, 압축, 암호화)          | prsentation layer          | 
       | 5층 (논리적 연결)          | Session layer          | 
       | 4층  (서비스 결정+ 데이터 전송 방식)          | Transport layer          |TCP  UDP |
       | 3층  (종단간의 연결)         | NetWork layer          |ICMP ARP RARP IP |
       | 2층  (인접 장비 통신연결)         | Datalink layer          |NetWork InterFace |
       | 1층  (전기적 신호 전송)         | Physical layer          |NetWork InterFace |
  
    * 통신에 사용되는 주소
    
      * 4계층 : 서비스 주소 (Port 주소)
      
      * 3계층 : 논리적 주소 (IP 주소)
      
      * 2계층 : 물리적 주소 (MAC 주소)
      
    * 계층별 NetWork 장비
    
      * 1계층 : Cable (신호 전달) , Reapeater/Hub (신호 재생) 
      
      * 2계층 : Bridge/Switch (Switching , MAC 주소 구분)
      
      * 3계층 : Router/L3 Switch Routing / IP 주소 구분
   
   * OSI 7 Reference Model 
    
     * 송신 : 항상 DATA 생성은 7계층 부터 시작 하고 하위 계층으로 전달 되면서 계층마다 역할 수행
     
     * 수신 : 데이터를 수신 측면 1계층에서 7계츠응로 올라가며 해석
   
   * Encapsulation
    
    송신자 측에서 데이터를 전송할 때 상위 계층에서 하위 계층으로 내료오면서 순차적으로 데이터를 합쳐주는 과정
    
    
   * DEcapsulation
    
    수신자 측에서 데이터를 전송 받은 후 하위계층부터 상위계층으로 올라오면서 순차적으로 데이터를 확인하며 떼어내는 과정
    
   * SDU (Service Data Unit)
    
     * 상위 계층에서 내려온 데이터를 지칭
    
     * 다른 말로 Payload라고 부름
     
   * PDU (Protocol Data Unit)
    
     *  상위 계층에서 내려온 데이터에 해당 계층의 정보를 포함한 데이터를 지칭
     
     *  header + SDU + footer
     
     * 계층별 PDU 명
     
       * 1계층: BiT  2계층  : FRAME 3계층 : Packet  4계층 : Segment 5,6,7 계층 Message
   
       * 상위 계층의 PDU는 하위계층에서 SDU
       
       * ex) 6계층의 SDU는 7계층의 data, 5계층의 SDU는 6계층의 data (6계층 + 7계층)
       
       
  * Layer 1계층 (물리계층)
   
    * 역할 장비 내부에 있는 bit 신호를 ** 전기 신호 변환 ** , ** 전기적 신호 ** 전달
    
    * 케이블이 연결이 잘 이뤄졌는지, 전원의 문제가 없는지
    
    * 신호가 잘 갔는지만 따진다. 주소가 없다(= protocol이 없다.)
    
    * 사용 장비
    
      *  cable, Connector , Repeater, Hub
  
  * Cable & Connector
  
    *  전기 신호 전달 매체(media)
    
    *  물리적으로 장비를 연결하는 매체
    
    * Cable 목적은 전기신호를 전송
    
    * 케이블 종류에 따라 사용되는 커넥터의 종류가 달라짐
    
 * 통신 Cable의 종류
 
   * 동축 케이블
  
   * 꼬임쌍선 케이블
  
   * 시리얼 케이블
  
   * 광 
   
* 동축 Cable (Coaxial cable)

   *  동심원의 중심에 있는 구리선이 매체가 되는 케이블
 
   *   10Mbps를 지원하는 Ethernet 환경에서 사용 됨

   *  과거 TV 안테나, 비디오 장비 , 오디오 장비 시스템에서 많이 사용한 장비

* 꼬임쌍선 케이블(Twisted-Pair cable)

  * 현재 LAN 구성에 일반적으로 사용되는 케이블
 
  * 내부에 8가닥의 구리선이 한 쌍식 고여져서 구성 됨
 
  * 종류 : STP, UTP
 
* STP (Shielded TP)
  
   * 은박지를 이용해 외부 저항을 줄여주는 기능 추가
   
   * 신호 손상을 줄여 더 먼거리로 데이터 전송
   
   * 단가가 높음
   
   *  신호 간섭이 많은 공장이나 야외, 빠른 통신 속도가 필요한 곳에 사용
   
    * 유럽에서는 STP가 주로 사용
   
  
*  UTP (Unshielded TP)

   * Shiled 기능이 없는 TP Cable)
 
   * 단가가 저렴
 
   * 처리가 간단, 값이 쌈 , 빠른 전송이 필요 없는 Ethernet의 LAN 용도에 표준으로 사용
 
   * EIA (Electronic Industries Alliance)에서 ** Cable Category ** 라는 표준 규격을 제시
 

* 꼬임 쌍선 케이블 용 커넥터 = RJ45

  * 8개의 구리선을 연결 할 수 있게 8개의 핀으로 구성되어 있음
 
  * 암 커넥터의 내부 핀은 만들어질 때 역할이 정해진다
 
  * TD (Transmit Data) : 데이터를 전송하는 역할
  
  * RD (Receive Data) : 데이터를 받는 역할
  
  * TD+로 전송되는 데이터는 RD +로 TD-로 전송되는 데이터는 RD- 로 받아야 함
  
* 핀 배치에 따른 Cable의 종류
  
   * Straight Cable
  
     * 핀 배열이 다른 장비끼리 연결할 때 양쪽 수 커넥터를 똑같이 핀 배치
 
  * Crossover Cable
 
    * 핀 배열이 같은 장비끼리 연결할 때 양쪽 수 커넥터를 반대로 핀 배치
    
* Serical Cable

  * 직렬 케이블
  
  * 예전 WAN 통신에서 모뎀과 네트워크 장비를 연결하기 위해 사용 됨
  
  * WAN을 구성하는 장비의 연결에 사용 됨
  
  * Connector의 역할이 DCE 와 DTE로 정해 져 있음
  
    * DCE : Clock Signal을 보내는 장비
   
    * DTE : Clock Signa을 받는 장비

  * Clock Signal
   
    * 논리 상태 H(1) L(0)이 주기적으로 나타나는 방형파 신ㅋ호
   
    * 한 bitd의 크기를 알려주기 위해 사용
   
    * LAN : Clock 신호와 Data 신호를 한번에 전송
   
    * WAN : DCE에서 Clock Signal을 주기적으로 전달하여 Bit 간격으로 동기화
 
 * 광 케이블
 
   * 빛의 전반사 특징을 이용하여 정보를 전송
   
   * 고속, 대용량 전송에 적합
   
   * 신호 감쇠가 상대적으로 덜하며 전자파 간섭이 거의 없음
   
   * 설치가 어려우며 연결장치와 케이블 간격이 고가
   
 * 광 케이블 종류
 
  * SMF (Single Mode Fiber)
    
     * 레이저 LED가 만들어낸 파형을 직겨 10 micron 이내의 좁은 코어를 통해 전송
     
     * 장거리 번송화 고속 전송에 많이 사용
     
     * 비용이 비싸므로 주로 통신회사에서 사용
     
  * MMF (Multi Mode Fiber)
  
     * 레이저 , LED가 만들어낸 여러 파형을 직경 50~115 micron 정보의 넓은 코어에 각가 다른 각도로 전송
   
     * 10 Gbps 이상의 속도가 보장 됨
   
     * 고속의 네트워크를 구성하기 위한 표준
   
     * 150~40,000m 까지 연결 가능
   
   

 
       
       
      
    
    
    
     

