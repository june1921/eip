# 1. 포트(Port)란

- 포트는 소프트웨어에서 네트워크 서비스나 특정 프로세스를 식별하는 논리 단위이다. 

- 주로 포트를 사용하는 프로토콜은 전송 계층 프로토콜(4계층)이고, TCP와 UDP가 있다. 

- 각 포트는 번호로 구별되며 이 번호를 포트 번호라고 한다. 

- 포트 번호는 IP 주소와 함께 쓰여 해당하는 프로토콜에 의해 사용된다.

​

# 2. 포트(port) 번호는 IANA에서 3개 구역으로 분리해서 관리

- Wellknown port​ : 0 ~ 1023 (잘 알려진 포트)

- Registered Port : 특정 응용을 위해 기업이 사용, 1024 ~ 49151 (등록된 포트)

- Dynamic Port : 49152 ~ 65535의 범위를 가지며 등록되거나 통제되지 않으며 임시 포트(대체로 운영체제가 할당) (동적 포트)

​

# 3. 기본적인 Well-Known port


### 1. FTP (File Transfer Protocol, 파일 전송 프로토콜, 포트 20, 21 / TCP):
- 파일 전송을 위한 프로토콜로, 서버와 클라이언트 간에 파일을 주고받을 수 있습니다.

### 2. SSH (Secure Shell, 보안 셸, 포트 22 / TCP):
- 원격으로 안전하게 서버에 접속하고 제어하기 위한 프로토콜로, 암호화된 연결을 제공합니다.

### 3. TELNET (TELetype NETwork, 원격 로그인 서비스, 포트 23 / TCP):
- 원격으로 호스트 컴퓨터에 접속하여 명령어를 실행하고 제어하기 위한 프로토콜입니다. 보안에 취약하므로 사용이 권장되지 않습니다.

### 4. SMTP (Simple Mail Transfer Protocol, 간단한 메일 전송 프로토콜, 포트 25 / TCP):
- 이메일 전송을 위한 프로토콜로, 메일 서버 간에 이메일을 주고받을 때 사용됩니다.

### 5. DNS (Domain Name System, 도메인 이름 시스템, 포트 53 / TCP, UDP):
- 도메인 이름을 IP 주소로 변환하거나 IP 주소를 도메인 이름으로 변환하기 위한 프로토콜로, 인터넷에서 도메인 이름을 관리합니다.

### 6. DHCP (Dynamic Host Configuration Protocol, 동적 호스트 구성 프로토콜, 포트 67, 68 / UDP):
- 네트워크에 연결된 장치에 자동으로 IP 주소 및 기타 네트워크 설정을 할당해주는 프로토콜입니다.

### 7. HTTP (Hypertext Transfer Protocol, 하이퍼텍스트 전송 프로토콜, 포트 80 / TCP, UDP):
- 웹 브라우저와 웹 서버 간에 데이터를 주고받는 프로토콜로, 웹 페이지의 요청과 응답에 사용됩니다.

### 8. POP3 (Post Office Protocol version 3, 포스트 오피스 프로토콜, 포트 110 / TCP):
- 이메일 클라이언트가 메일 서버로부터 이메일을 받아오는 데 사용되는 프로토콜입니다.

### 9. RPC (Remote Procedure Call, 원격 프로시저 호출, 포트 111 / TCP, UDP):
- 원격 시스템에서 프로시저를 호출하여 분산 시스템 간의 통신을 가능하게 해주는 프로토콜입니다.

### 10. IMAP (Internet Message Access Protocol, 인터넷 메시지 액세스 프로토콜, 포트 143 / TCP):
- 이메일 서버와 클라이언트 간에 이메일을 관리하고 액세스하는 데 사용되는 프로토콜입니다.

### 11. SNMP (Simple Network Management Protocol, 간단한 네트워크 관리 프로토콜, 포트 161, 162 / UDP):
- 네트워크 장비 및 서버의 모니터링 및 관리를 위한 프로토콜입니다.

### 12. TLS/SSL 방식의 HTTP (Transport Layer Security/Secure Sockets Layer, HTTPS, 포트 443 / TCP):
- HTTP 프로토콜을 보안하기 위해 TLS/SSL 암호화 프로토콜을 사용하는 HTTPS(보안 HTTP)를 위한 포트입니다.

[출처] 반드시 알아야 할 PORT (수제비- IT 커뮤니티 (정보처리기사,빅데이터분석기사, AdSP 등)) | 작성자 수제비쌤
