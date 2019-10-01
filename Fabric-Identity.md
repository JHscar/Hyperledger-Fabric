# Fabric Identity
## PKI
PKI에는 4가지 핵심 요소가 있다.
	* 디지털 인증서
	* 공개키 및 개인키
	* 인증 기관
	* 인증성 해지 목록

### 	공개키 암호화
		* 개인키 + 공개키
		* 개인키
			* 소유자가 가지고 절대 비밀로 보관
			* 데이터로 서명
			* 공개키로 암호화한 데이터를 복호화 할 수 있습니다.
		* 공개키
			* 다른 사람에 알려주는 용도
			* 개인키로 암호화한 데이터를 복호화 할 수 있습니다.
	
### 	전자서명
		* 데이터가 위/변조 되지 않았다 라는 것을 PKI 시스템에서 알려주기 시스템
			* 원본의 digest(원본 해쉬)를 만든다
			* 개인키로 digest를 서명한 후에 원본에 붙인다.
			* 공개키로 digest를 복호화 한다.
			* 원본을 통해서 만든 digest와 비교해서 검증한다.
	
### 	X.509
		* 공개키가 들어 있다.
		* 발행자
		* 내가 누구인지
		* 도메인
		* root ca에 대한 정보(root ca로 부터 받은게 아닌 경우)

### 	Fabric 인증서
		* 인증서 위치
		* crypto-config
		* cryptogen

### MSP
= Membership Service Provider
	* Fabric에서 노드_유저_채널 등등, 서로 간의 인증, 권한 관리를 해주는 기본적인 개념 or 서비스
	* 노드(Peer, Orderer, User) -> directory(MSP)안에 있는 인증서를 가지고 한다.
	* 채널/네트워크 -> 다른 여러가지 방법을 통한 멤버쉽 관리

##### Block Structure
![](Fabric-Identity/Block%20structure.png)








