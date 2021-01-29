## Hub & Repeater

신호를 재생시켜 좀더 먼 거리까지 신호를 전달하는 장비

  * ### Repeater
  
    * port의 개수 : 2개
    
    * 한쪽 port로 전달받은 신호를 재생시켜 반대쪽 포트로 전달 함
    
    * 주로 거리 연장을 위해
    
    * 전기신호가 온도 등 다양한 방해에 의해 힘이 없어짐 현재 잘 사용 X
  
  * ### Hub
  
    * port의 개수 : 여러개
    
    * 한쪽 prot로 전달 받은 신호를 재생시켜 나머지 포트로 모두(flooding) 전달
    
    * 다수의 포트를 이용 장비의 연결을 집중 하는 **집선 장비**로 사용 함
    
    * 집선 장비 : 선을 집중해서 모아 주는 장비
    
    * 통신 방식
    
      *  모든 회선을 연결된 호스트들이 공유
      
      *  Hub에 연결된 호스트들은 회선을 사용하기 위해 경쟁하게 됨
      
      *  Hub는 Inbound Packet을 모든 포트로 Flooding 함
      
 ## 신호 전달 방식
 
  * Simplex
    
    * 단 방향 신호 전달 
    
    * 한 방향으로만 신호 전달 가능
    
    * ex) 방송국, 일방통행 도로
    
  * Half-Duplex
  
    * 반 이중 신호 전달 방식
    
    * 양쪽 전송이 가능 한 순간에 한 방향으로 신호 전달 가능
    
    * Ex) 무전기, 1차선 도로
    
  * Full-Duplex
  
    *  전 이중 신호 전달 방식
    
    *  동시에 양 방향 신호 전달
    
    * Switch의 기본 신호 전달 방식
    
    * Ex) 전화기 , 2차선 도로
    
    
 ## 충동 가능 영역( Collision Domain)
 
  * Hub 통신의 문제점 : Half-Duplex 통신만 지원 경쟁을 통해 매체를 이용하는 환경에서 신호의 충돌이 발생할 가능성이 존재
  
  * Collision Domain 
  
    * Half-Duplex 환경에서 동시에 양방향으로 Data가 전송되는 경우 충돌 발생
    
    * 신호 충돌이 발생 가능한 영역을 Collision Domain이라 함
    
    * Hub, Repeater 등 1계층 장비는 기본 Half-Duplex 방식을 사용
    
  * 해결 방법
    
    * CSMA/CD 기법
           
    * Switch 등 Layer 2 이상의 장비 사용
     
       * FUll -Duplex로 동작

    
    
    
