### GWLB
- 2020년도 11월에 출시된 서비스
- 방화벽과 침입 감지 및 방지 시스템을 제공하는 벤더(Check Point, Cisco, Palo Alto)들의 서비스를 SaaS(가상 어플라이언스 형태)로 사용 가능함. (AWS 파트너나 AWS Marketplace에서 사용하는 형태)
- GWLB를 사용하기 위해 PrivateLink인 GWLBe(Endpoint)를 사용함. (서로 다른 Account나 VPC에 위치할 수 있기 때문) 
- 인바운드 또는 아웃바운드를 GWLB로 보내기 위해 라우팅 테이블의 Next-htop을 GWLBE로 설정함.
- GWLB를 사용할 때 트래픽 패턴은 크게 세 가지임. 인바운드와 아웃바운드 모두 GWLB를 거치는 경우, 인바운드는 거치고 아웃바운드는 거치지 않는 경우, 마지막으로 인바운드는 거치지 않고 아웃바운드만 거치는 경우. (인바운드와 아웃바운드 모두 안 거치는 경우, 당연히 GWLB를 사용할 필요 없음)

