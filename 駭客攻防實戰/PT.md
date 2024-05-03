# 滲透測試
- 滲透測試(Penetration Test, PT)
- 滲透測試方法論(Methodology)
- 滲透測試主要步驟|工具與技術
  - 偵察(reconnaissance)
  - Open-Source Intelligence(OSINT) (開放情報蒐集)
  - 掃描(scanning)
  - 基本掃描  VS  漏洞掃描(Vulnerability SCAN)
  - 滲透|漏洞利用(Exploitation)
  - 提升權限(Privilege Escalation)
  - 維持存取(Post-exploitation)
- Windows AD 與 內網滲透測試
- 紅隊演練(red team)
- 滲透測試報告

# IPAS 初階考題
```
下列何者為探測通訊埠（Port）的軟體？
(A) Appscan (B) Nmap (C) Burp Suite (D) Telnet
```
```
下列何項駭客工具可以傾倒(dump)記憶體裡登入過的帳號密碼？
(A) mimikatz (B) SQLmap (C) Burp Suite (D) AppScan
```
```
請問下列何種工具常被用來建立 Backdoor？
(A) telent (B) ipconfig (C) NC (D) cat
```

```
某網站在設計時進行過安全分析，也在開發時要求程序員編寫安全的 代碼，但佈署時由於管理員將備份存放在 WEB 目錄下導致了攻擊者可直接下載備份，為了發現系統中是否存在其他類似問題，
下列何種測試方式是最佳的測試方法？ (A) 模糊測試 (B) 源碼測試 (C) 整合測試 (D) 滲透測試
```

# IPAS 中階考題:
```
關於滲透測試（Penetration Test, PT），下列敘述何者「不」正確？
(A)模擬駭客攻擊並評估網路、資訊系統安全性之活動，於產出報告 中詳述弱點如何利用與影響，並給予修復建議
(B)滲透測試可分非破壞測試(Nondestructive Test )與破壞測試 (Destructive Test )
(C)滲透測試有五種類別：黑箱（Black-box）、白箱（White-box）、灰箱(Grey-box)、紅箱（Red-box ）與藍箱（Blue-box），差異為提供測試人員受測目標資訊之詳細程度
(D)弱點掃描與滲透測試差異在於，前者僅關注於找到已知弱點，後者則引入縱深防禦的概念於發現組織之安全問題
```
```
關於網路安全滲透測試的敘述，下列何者錯誤？
(A)網路安全滲透測試是找出駭客實現攻擊目的的所有途徑，而駭客入侵只是要實現某一特地目的
(B)逆向工程是網路安全滲透測試的一部分，目的是發掘系統的漏洞
(C)網路安全滲透測試就是一般普遍認知的漏洞掃描
(D)網路安全滲透測試方法可以分成黑盒測試、灰盒測試、白盒測試等三種
```
# IPAS 中階考題【題組】
```
網站滲透攻擊是紅隊滲透重要基本課題，而善用網路資源與工具，可以達到事半功倍之效果，身為資安滲透團隊成員，以下相關網路資源與工具，是必須要掌握的技術與技巧。
```

```
關於網路資源的敘述，下列何者錯誤？
(A) FOFA 是覆蓋全球資料頗為完整的 IT 設備搜尋引擎，非中國創立資料庫
(B) Shodan 是世界上第一個用於聯網與 IoT 設備的搜尋引擎，可以查找到電子門鎖相關資訊
(C) ZoomEye 是由中國創宇 404 實驗室所搭建網路空間搜尋引擎
(D) Censys 也是蒐集全球最新的 Internet 掃描資料源
```

```
子網域資訊的取得是滲透前重要的 Footprint 程序，下列何項「不」是子網域查找工具？
(A) subfinder (B) SubDomainizer (C) Virustotal (D) SubBrute
```

```
身為一個滲透測試人員，必須善 用網際網路有用資料庫或搜尋引擎，下列各類資料庫系統的敘述，
何者錯誤?
(A)shodan.io 是世界上用於聯網設備查找的搜索引擎
(B)censys.io 是一個免費資料庫，累積許多無線網路重要刺探資訊
(C)pulsedive.com 蒐集許多威脅情報
(D)intelx.io 可處理加密貨幣搜尋與暗網搜尋
```

```
[複選]
成功滲透到某個網站後，為了避免觸發相關警示而通知 IT 人員，於是採用「免殺（迴避防毒軟體的偵測）」的手法。發現該主機為一台 Windows 10 所搭建網站系統，決定使用Windows 作業系統中相關工具程式來進行 Command & Control，下面哪些 Windows 作業系統「原生」指令可以使用在遠端下載？
(A) Bitsadmin.exe (B) Certutil.exe (C) HH.exe (D) Update.exe
```
## IPAS 中階考題【題組】 110年度第五題組 nc == Netcat 
- Netcat 是 Linux 系統中一個多功能的工具程式 ==> 網路瑞士刀
- 幾乎任何使用 TCP 或 UDP 封包的動作都可以用它來達成，是許多系統管理者（包含我自己）最喜愛的網路診斷工具之一
- [Netcat（Linux nc 指令）網路管理者工具實用範例](https://blog.gtwang.org/linux/linux-utility-netcat-examples/)
- 功能
  - 送資料
    - 測試特定的 TCP 連接埠（port）是否有開啟 ==> nc -v 192.168.0.175 5000
    - 傳送測試用的 UDP 封包到遠端伺服器  ==> echo -n "foo" | nc -u -w1 192.168.1.8 5000
    - Port Scanning遠端機器的連接埠掃描 ==> nc -vnz -w 1 192.168.233.208 1-1000 2000-3000
    - 掃描 UDP 的連接埠 ==> nc -vnzu 192.168.1.8 1-65535 
  - 接收資料(相當是server功能) 使用 -l 參數(listen mode, for inbound connects)
    - 開啟 UDP 連接埠接收資料 ==> nc -lu localhost 5000
- 不同變化版本 
  - socat(SOcket CAT) 是netcat較複雜的姊妹程式。它比起netcat功能更多
    - [Socat 入门教程](https://www.hi-linux.com/posts/61543.html)
    - [socat 雙向資料流轉接工具使用教學與範例](https://officeguide.cc/socat-multipurpose-relay-bidirectional-data-transfer-tutorial-examples/)
  - [Ncat](https://nmap.org/ncat/)是由Nmap開發團隊實做的另一個netcat版本
```
nc -vzw5 192.168.0.1 1-2048(操控端)
nc -v -z -w5 192.168.0.1 1-2048(操控端)
nc -ltp 80(操控端)
nc -l -p 80 < /test.txt(操控端)
nc -t -p 80 < /test.txt(操控端)
nc -g -p 80 > /test.txt(操控端)
nc -g -p 80 < /test.txt(操控端)
nc -l -p 80(操控端)
```
### netcat指令參數
```
root@kali:~# nc -h
[v1.10-41.1]
connect to somewhere:	nc [-options] hostname port[s] [ports] ... 
listen for inbound:	nc -l -p port [-options] [hostname] [port]

options:
	-c shell commands	as `-e'; use /bin/sh to exec [dangerous!!]
	-e filename		program to exec after connect [dangerous!!]
	-b			allow broadcasts
	-g gateway		source-routing hop point[s], up to 8
	-G num			source-routing pointer: 4, 8, 12, ...
	-h			this cruft
	-i secs			delay interval for lines sent, ports scanned
        -k                      set keepalive option on socket
	-l			listen mode, for inbound connects
	-n			numeric-only IP addresses, no DNS
	-o file			hex dump of traffic
	-p port			local port number
	-r			randomize local and remote ports
	-q secs			quit after EOF on stdin and delay of secs
	-s addr			local source address
	-T tos			set Type Of Service
	-t			answer TELNET negotiation
	-u			UDP mode
	-v			verbose [use twice to be more verbose]
	-w secs			timeout for connects and final net reads
	-C			Send CRLF as line-ending
	-z			zero-I/O mode [used for scanning]

port numbers can be individual or ranges: lo-hi [inclusive];
hyphens in port names must be backslash escaped (e.g. 'ftp\-data').
```


