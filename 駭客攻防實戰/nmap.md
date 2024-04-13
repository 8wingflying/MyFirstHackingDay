# nmap

# 參考文獻
- [Nmap Network Scanning](https://nmap.org/book/toc.html)
- [Nmap参考指南(Man Page)](https://nmap.org/man/zh/index.html)


# 參考書籍
- [Nmap: Network Exploration and Security Auditing Cookbook - Second Edition]()
# PART I: nmap 功能 ==> 原理
- Host Discovery (“Ping Scanning”)活躍主機發現(IP scan)
  - `-PA [portlist]`  (TCP ACK Ping) 
- port掃描(port scan)
- 信息蒐集
- 作業系統檢測(OS fingerprint | see  8. Remote OS Detection)
  - `-O` ==> 啟用作業系統檢測
  - `-A` ==> 同時啟用`作業系統檢測`和`版本檢測`
- [服務和`版本`探索Service and Version Detection(see  7. Service and Application `Version` Detection)](https://nmap.org/man/zh/man-version-detection.html)
  - `-sV` == > 版本探测)
  - `-A` ==> 同時啟用`作業系統檢測`和`版本檢測`
- [Bypass firewall/IDS(防火墙/IDS躲避和哄骗)Firewall/IDS Evasion and Spoofing](https://nmap.org/man/zh/man-bypass-firewalls-ids.html)
  - f (封包分段); --mtu (使用指定的MTU)
    - `-f`選項要求掃描時(包挺ping掃描)使用小的IP封包分段。
    - 其思路是將TCP頭分段在幾個封包中，使得封包篩檢程式、 IDS以及其它工具的檢測更加困難。
  - `-D <decoy1 [，decoy2][，ME]，...>`  ==> 使用(decoy scan)誘餌隱蔽掃描
  - `-S <IP_Address>` == > 源地址哄騙(使用假 來源位址)
  - `-ttl <value>` == > 設置IP time-to-live (使用假 time-to-live)

# nmap 設定與調教
- [效能調教(see 6. Optimizing Nmap Performance)](https://nmap.org/book/performance.html)
- Timing Templates (-T)  數字越大代表掃描速度越快
  - 範例: nmap `-T1`  -p21-25  192.168.1.104
  - `-T5` == Nmap Insane Scan
    - used for sending packets insanely fast and waits only 0.3 seconds for the response.
  - `-T4` == Nmap Aggressive Scan
    - 手冊說如果網路環境穩定，參數建議調整為 -T4。
    - `-T4` 禁止動態 TCP Port 掃描延遲超過 10 ms
  - `-T3` == Normal Scan: 預設使用
  - `-T2` == Polite Scan 兩個送出封包間格 0.4秒
  - `-T1` == Sneaky Scan 兩個送出封包間格 15秒
  - `-T0` == Paranoid Scan 兩個送出封包間格 5分鐘
  - -T0 ~ -T1 是避免 IDS 告警，但掃描速度頗慢， 沒有特殊需求，不建議使用
- Nmap的格式化輸出
  - Nmap提供5種不同的輸出格式:
    - `-oN` <filespec>(標準輸出)
    - `-oX` <filespec>(XML輸出)
    - `-oS` <filespec>(腳本 KIDD|3 輸出)
    - `-oG` <filespec>(Grep輸出)
    - `-oA` <basename>(輸出至所有格式)
# PART II:NMAP Script Engine(NMAP NSE)
- 使用lua語言開發
- 604個script
- [NSE Scripts: 依照字母排序](https://nmap.org/nsedoc/scripts/)
- [NSE Scripts: 依照功能類類型展示](NMAP_NSE.md)
- 範例 1:http-slowloris 攻擊
  - 檢測是否有此漏洞 == > `nmap --script http-slowloris-check <target>`
    - [http-slowloris-check](https://nmap.org/nsedoc/scripts/http-slowloris-check.html)
  - 執行http-slowloris 攻擊 == > `nmap --script http-slowloris --max-parallelism 400  <target>`
    - [http-slowloris](https://nmap.org/nsedoc/scripts/http-slowloris.html) 
- 範例 2:最新漏洞檢測:Exchange Server伺服器|CVE-2022-41082
  - [6萬臺Exchange Server仍未修補ProxyNotShell漏洞2023.1](https://www.ithome.com.tw/news/154989)
  - [nse-exchange](https://github.com/Diverto/nse-exchange)
  - 單一目標 ==> `nmap -sV -T4 -v --script=http-vuln-cve-2022 scanme.nmap.org`
  - 網段掃描 ==> `nmap -p443 -T4 -v --script=http-vuln-cve-2022 10.0.0.0/16 `

  

# IPAS考題初階
```
某 MIS人員欲對公司一重要伺服器（功能包含檔案伺服器、資料庫功能）使用 Nmap來執行進行滲透測試，
以便瞭解該資訊設備之漏洞是否全數修補完成，
請問該 MIS使用此工具最主要之目的為下列何者？
(A) 利用該伺服器已知對外開放之服務埠進行情蒐
(B) 利用該伺服器已知之漏洞提升權限
(C) 利用該伺服器已知之漏洞竊取檔案
(D) 利用該伺服器已知之漏洞下載資料庫
```
答案: A

# IPAS考題中階  
```
關於 Nmap工具之指令操作，下列敘述何者正確？
(A) Nmap的 SYN掃描可以掃描 UDP埠
(B) Nmap使用 -T1參數較 -T4參數的掃描速度快
(C) Nmap使用 -sO參數可檢測標的主機的作業系統版本
(D) Nmap使用 -D參數為誘騙掃描(decoy scan)
```
答案: D

# CEH考題 
```
Which of the following scanning method splits the TCP header into several packets
and makes it difficult for packet filters to detect the purpose of the packet?
A. ACK flag probe scanning
B. ICMP Echo scanning
C. SYN/FIN scanning using IP fragments
D. IPID scanning
```
答案: C

# CEH考題 
```
Sam is a penetration tester hired by Inception Tech, a security organization. He was asked to perform port
scanning on a target host in the network. While performing the given task, Sam sends FIN/ACK probes and
determines that an RST packet is sent in response by the target host, indicating that the port is closed.
What is the port scanning technique used by Sam to discover open ports?
Xmas scan
B. IDLE/IPID header scan
C. TCP Maimon scan
D. ACK flag probe scan
```
答案: C
