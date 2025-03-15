## 지식전달용
## 데이터베이스 포트 암기
MySQL

TCP 3306

MS-SQL

TCP 1443

Oracle

TCP 1521

PostgreSQL

TCP 5432

MariaDB

TCP 3306

DB2

TCP 50090

FTP data port(active mode)

TCP 20

NetBIOS (TCP rarely used)

TCP/UDP 137

FTP control port

TCP 21

NetBIOS

UDP 138

SSH

TCP 22

NetBIOS

TCP 139

SCP(uses SSH)

TCP 22

IMAP4

TCP 143

SFTP(uses SSH)

TCP 22

LDAP

TCP 389

telnet

TCP 23

HTTPS

TCP 443

SMTP

TCP 25

SMTP SSL/TLS(SMTPs)

TCP 465

TACACS+

TCP 49

IPsec (for VPN with IKE)

UDP 500

DNS name queries

UDP 53

LDAP/SSL(LDAPs)

TCP 636

DNS zone Transfers

TCP 53

LDAP/TLS(LDAPs)

TCP 636

TFTP

UDP 69

IMAP SSL/TLS(IMAPs)

TCP 993

HTTP

TCP 80

POP SSL/TLS(POPs)

TCP 995

Kerberos

UDP 88

L2TP

UDP 1701

POP3

TCP 110

PPTP

TCP 1723

SNMP

UDP 161

Remote Desktop Protocol(RDP)

TCP/UDP 3389

SNMP trap

UDP 162

Microsoft SQL Server

TCP 1433
## 이글루코퍼레이션 회사 업무에 필요한 알아두면 좋은 웰논 포트 정리 
![KakaoTalk_20250127_153842064](https://github.com/user-attachments/assets/fbfe5257-2544-48f5-bdc1-4b948a8f4ac6)
![KakaoTalk_20250127_153842064_01](https://github.com/user-attachments/assets/039175a5-9ba3-4c65-9b67-863f9ca6b445)
물론, 꼭 이 포트번호를 사용하지 않고 다른 포트번호를 지정해서 사용 할 수 있다.     
예를들어, 80번 HTTP(웹 서비스) 포트를 8080번 포트로 변경 (버프 스위트 등 툴 사용)   
악의적인 목적을 가지고 일반적인 포트 80, 443 웹서비스로 들어오는 공격들을 탐지 detect하고 예방 prevention할 수 있을 것이다.   
## 포트 점검 
# cat /etc/services     /* 모든 포트 목록 확인 */ 



# yum -y install nmap

# nmap localhost    /* 자신의 서버에 열린 포트 점검 */



# netstat -an | more    /* 열린 포트 점검 */

# netstat -an | grep '^tcp'    ( # netstat -ant )

# netstat -an | grep '^udp'   ( # netstat -anu )



( win2008 )

<windows + E > = C:\Windows\system32\drivers\etc\services /* 모든 포트 목록 확인 */



nmap 툴 설치

https://nmap.org/download.html



c:\> natstat -a
