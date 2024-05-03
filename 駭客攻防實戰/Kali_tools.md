# PART II.Kali Linux常用工具
- 更多工具 see [Kali Tools](https://www.kali.org/tools/all-tools/)
- 01.資訊收集| Information Gathering
- 02.漏洞分析|Vulnerability analysis
- 03.網站應用程式分析|web application analysis
- 04.資料庫評估| Database assessment
- 05.密碼攻擊| Password Attack
- 06.無線網路攻擊| wireless Attack
- 07.逆向工程 | reverse engineering
- 08.攻擊工具 | EXPLOITATION TOOLS
- 09.竊聽與欺瞞攻擊|sniffing & spoofing
- 10.後攻擊工具|post-exploitation
- 11.數位鑑識工具| Forensics
- 12.報表工具 | Reproting tools(撰寫滲透測試報告用)
- 13.社交工程攻擊工具| Social engineering tools

## 01.資訊收集| Information Gathering
## 02.漏洞分析|Vulnerability analysis
### 03.網站應用程式分析|web application analysis
- Commix (short for [comm]and [i]njection e[x]ploiter)
- [Sqlmap---自動化sql注入工具](sqlmap.md)
- webshell(Kali送你一堆網站木馬)

## 04.資料庫評估| Database assessment
- sqlite database browser
- sqlmap

### 05.密碼攻擊| Password Attack
- Offline Attacks(離線攻擊工具)
  - hashcat
  - john 
- Online Attacks(線上攻擊工具)
  - hydra
  - medusa 
- Passing the Hash Tools
  - CrackMapExec
  - impacket
  - Mimikatz   
- Password Profiling and Wordlists
- CeWL(Custom Word List generator)
- [hashcat-advanced password recovery](https://hashcat.net/hashcat/)
- 研讀書籍 [Password Cracking with Kali Linux(February 2024)](https://www.packtpub.com/product/password-cracking-with-kali-linux/9781835888544)

### 08.攻擊工具 | EXPLOITATION TOOLS
- CrackMapExec
- metasploit
- searchsploit
  - [SearchSploit – The Manual](https://www.exploit-db.com/searchsploit)
  - 範例:
    - searchsploit hfs
    - searchsploit wordpress
## 10.後攻擊工具|post-exploitation
- OS Backdoor(作業系統後門程式)目錄
  - [dbd](https://www.kali.org/tools/dbd/)
  - powersploit
  - sdb
  - 參考資料
    - [使用Sbd 和 Dbd 工具建立系統安全後門](https://github.com/Yehnn/kali/blob/master/kali%E5%90%8E%E9%97%A8%E6%8A%80%E6%9C%AF%E5%AE%9E%E6%88%98/03%E4%BD%BF%E7%94%A8%20sbd%20%E5%8F%8A%20dbd%20%E5%88%9B%E5%BB%BA%E7%B3%BB%E7%BB%9F%E5%AE%89%E5%85%A8%E5%90%8E%E9%97%A8.md) 
- Tunnelling & Exfiltration(建立隱藏通道與資料外洩攻擊)目錄
  - 參考 MITRE ATT&CK Exfiltration (TA0010)戰術 
  - dns2tcpc
  - [dns2tcpd](https://www.kali.org/tools/dns2tcp/)
  - ptunnel
- WEB Backdoor(網站後門程式)目錄
  - [Laudanum](https://www.kali.org/tools/laudanum/) is a collection of injectable files
  - weevely
- impacket
- Mimikatz(用微軟powershell寫的著名攻擊工具)
- powershell empire(用微軟powershell寫的著名攻擊工具)
- powersploit(用微軟powershell寫的著名攻擊工具)
- ProxyChains
- startkiller(Frontend for Powershell Empire)
- weevely
  - [weevely详细使用教程](https://blog.csdn.net/smli_ng/article/details/106071142)
