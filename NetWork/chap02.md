### 네트워크 통신규약

#### **통신 규약**  =  Protocol

  * 표준화된 통신 규약
  
  * 컴퓨터나 네트워크 장비가 서로 통신하기 위해서 미리 정해놓은 약소
  
  * 통신을 원하는 두 개체간 통신에 대한 절차/규범/규정/규약/규칙
  
#### IETF (Internet Engineering Task Force, 국제 인터넷 표준화 기구)

  *  네트워크 통신을 위한 ** 프로토콜 제정 및 표준화를 담당하는 국제 기구 **
  
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
      
      * 데이터 생성 계층으로 주로 소프트 웨어 개발 분야에서 참소
      
      
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
     
     

