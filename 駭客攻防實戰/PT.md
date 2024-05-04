# 滲透測試
- 滲透測試(Penetration Test, PT)
- 滲透測試方法論(Methodology)
  - OSSTMM (112年中階考題) 
- 滲透測試主要步驟|工具與技術
  - 偵察(reconnaissance)
  - Open-Source Intelligence(OSINT) (開放情報蒐集)
  - 掃描(scanning)
  - 基本掃描  VS  漏洞掃描(Vulnerability SCAN)
  - 滲透|漏洞利用(Exploitation)
  - 提升權限(Privilege Escalation)
  - 維持存取(Post-exploitation)
- [Windows AD 與 內網滲透測試](IPT.md)
- 紅隊演練(red team)
- 滲透測試報告

# IPAS 初階考題
```
關於提權(Privilege Escalation)，下列敘述何者正確？
(A)提升使用者權限至系統管理權限
(B)刪除入侵軌跡
(C)刪除使用者帳號
(D)找出具有最高權限的帳號
```
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
某網站在設計時進行過安全分析，也在開發時要求程序員編寫安全的代碼，
但佈署時由於管理員將備份存放在 WEB 目錄下導致了攻擊者可直接下載備份，
為了發現系統中是否存在其他類似問題，
下列何種測試方式是最佳的測試方法？
(A) 模糊測試 (B) 源碼測試 (C) 整合測試 (D) 滲透測試
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
網站滲透攻擊是紅隊滲透重要基本課題，而善用網路資源與工具，可以達到事半功倍之效果，
身為資安滲透團隊成員，以下相關網路資源與工具，是必須要掌握的技術與技巧。
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

- [Windows commands](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)
  - [英文版](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)
  - [Bitsadmin.exe](https://learn.microsoft.com/zh-tw/windows-server/administration/windows-commands/bitsadmin)
    - BITSAdmin == BITS管理工具(管理BITS任務的命令列工具) ==> Bitsadmin 是一種命令列工具，可用來建立、下載或上傳作業，以及監視其進度。 
    - [BITS|背景智慧型傳輸服務|Background Intelligent Transfer Service](https://zh.wikipedia.org/zh-tw/%E5%90%8E%E5%8F%B0%E6%99%BA%E8%83%BD%E4%BC%A0%E8%BE%93%E6%9C%8D%E5%8A%A1)
      - BITS是微軟在Windows 2000及後續版本中包含的一個組件。
      - 它有助於利用空閒網路頻寬在電腦之間非同步、有優先級及自我限制地傳輸檔案，並主要在較新版本的Windows Update、Microsoft Update、Windows Server更新服務和系統管理伺服器用於交付修補程式到客戶端。
      - 反病毒軟體Microsoft Security Essentials（及之後的Windows Defender）也使用它取得簽章更新，並且微軟的即時通訊產品會使用它來傳輸檔案。
      - BITS通過組件對象模型（COM）介面供外部呼叫。
    - Bitsadmin 工具會使用參數來識別要執行的工作。
      - 可以呼叫 bitsadmin /? 或 bitsadmin /help 來取得參數的清單。
      - 大部分的 <job> 參數都需要參數，您可以將其設定為作業的顯示名稱或 GUID。
      - 作業的顯示名稱不一定是唯一的。
      - /Create和/list參數會傳回作業的 GUID。
      - 更多 bitsadmin 參數 請參看[bitsadmin](./bitsadmin.md)
    - [bitsadmin 範例](https://learn.microsoft.com/zh-tw/windows-server/administration/windows-commands/bitsadmin-examples)
      - `bitsadmin /list`  ==>  使用 /list 參數監視傳輸佇列中的作業
      - `bitsadmin /monitor` ==> 使用 /monitor 參數監視傳輸佇列中的作業
      - `bitsadmin /reset` ==> 取消目前使用者之傳輸佇列中的所有作業
      - `bitsadmin /create myDownloadJob`==> 建立名為 myDownloadJob的下載作業 | BITSAdmin 會傳回可唯一識別作業的 GUID。 在後續呼叫中使用 GUID 或作業名稱。
      - `bitsadmin /transfer myDownloadJob /download /priority normal https://downloadsrv/10mb.zip c:\\10mb.zip`
        - 啟動名為 myDownloadJob的傳輸作業 Add files to the download job
        - 更多說明 請參看[bitsadmin transfer](https://learn.microsoft.com/zh-tw/windows-server/administration/windows-commands/bitsadmin-transfer)
  - Certutil.exe [微軟官方說明](https://learn.microsoft.com/zh-tw/windows-server/administration/windows-commands/certutil)
    - Certutil.exe是安裝為憑證服務的一部分的命令列程式。
    - 可以使用certutil.exe來顯示憑證授權單位單位 (CA) 設定資訊、設定憑證服務、備份和還原 CA 元件。
    - 此程式也會驗證憑證、金鑰組和憑證鏈結。
    - 如果在憑證授權單位單位上執行 certutil 而沒有其他參數，則會顯示目前的憑證授權單位單位設定。
    - 如果在非憑證授權單位單位上執行 certutil，命令預設為執行 certutil [-dump] 命令。
    - 功能範例:
      - 功能1.Base 64編碼與解碼
        - certutil [options] -encode infile outfile ==> 將檔案編碼為 Base64
        - certutil [options] -decode infile outfile ==> 解碼 Base64 編碼的檔案
      - 功能2.憑證服務處理
        - certutil [options] -CA [CAName | templatename]  ==>  顯示註冊原則憑證授權單位單位
        - certutil [options] -shutdown ==> 關閉 Active Directory 憑證服務
        - certutil [options] -backupkey backupdirectory ==> 備份 Active Directory 憑證服務憑證和私密金鑰
          - backupdirectory 是用來儲存已備份 PFX 檔案的目錄。 
        - certutil [options] -backup backupdirectory [incremental] [keeplog] ==> 備份 Active Directory 憑證服務
          - backupdirectory 是用來儲存備份資料的目錄。
          - incremental 只會執行增量備份， (預設值為完整備份) 。
          - keeplog 會保留資料庫記錄檔， (預設值是截斷記錄檔)  
      - 功能3.下載駭客最愛的惡意程式
        - certutil.exe -urlcache -split -f [URL] output.file 
      - 更多說明請參閱
        - [Certutil工具（Windows命令行下载常用）](https://blog.csdn.net/bring_coco/article/details/117352716)
        - [Windows上自带的渗透测试工具：Certutil](https://zhuanlan.zhihu.com/p/107819644)
        - [CertUtil abused by attackers to spread threats](https://www.avira.com/en/blog/certutil-abused-by-attackers-to-spread-threats)
        - [CertUtil.exe Could Allow Attackers To Download Malware While Bypassing AV](https://www.bleepingcomputer.com/news/security/certutilexe-could-allow-attackers-to-download-malware-while-bypassing-av/)
        - [Windows(Win10)自带的可用于文件校验(Hash校验,SHA256校验,MD5校验等)的命令: CertUtil 和 Get-FileHash](https://blog.csdn.net/kfepiza/article/details/129152496?utm_medium=distribute.pc_relevant.none-task-blog-2~default~baidujs_baidulandingword~default-0-129152496-blog-117352716.235^v38^pc_relevant_anti_t3&spm=1001.2101.3001.4242.1&utm_relevant_index=3)
  - HH.exe
    - hh.exe是微軟windows系統程式，.chm副檔名的幫助檔(helper)默認是用hh.exe打開。
    - 如果用戶此時並沒有查看chm格式的電子書檔或幫助檔，hh.exe又在進程中反復出現，則可能中了hh.exe病毒。
    - 在正常情況下不建議使用者對該類檔案（hh.exe）進行隨意的修改。它的存在對維護電腦系統的穩定具有重要作用。
    - CHM檔是Windows的一種幫助檔案格式, 它主要是由.html 轉換製作出來的，有時我們需要將.CHM檔反向轉換成 .html 格式檔，即chm to html。我們可以利用Windows自帶的hh.exe檔來進行檔案格式轉換。
    - 轉換語法為：hh -decompile 目的檔案夾 源CHM檔案名。 ==> hh -decompile d:\test\help help.chm
    - 更多說明請參看 [微軟windows系統程式 hh.exe](https://baike.baidu.com/item/hh.exe/10474729)
    - [通過編譯的 HTML 幫助文件傳播的惡意軟件](https://blog.rootshell.be/2017/12/19/malware-delivered-via-compiled-html-help-file/)
      - .chm 文件是編譯的 HTML 幫助文件，可能包括文本、圖像和超鏈接。
      - 可以在瀏覽器中查看；作為在線幫助解決方案在程序中或通過 Windows 通過特定工具：hh.exe。
      - 與大多數 Microsoft 文件格式一樣，它還可以鏈接到可從 HTML 文件啟動的外部資源==>惡意腳本或可執行文件
      - MITRE 戰技 T1218.001	Compiled HTML File [System Binary Proxy Execution: Compiled HTML File](https://attack.mitre.org/techniques/T1218/001/)
      - [Procedure for generating Malicious CHM file](https://gist.github.com/mgeeky/cce31c8602a144d8f2172a73d510e0e7)
- [更多 windows 指令與相關知識 (有時間請多多充實windows 指令的用法) ](windows.md)
- 更多WINDOWS知識 請參閱 [Windows組件列表](https://zh.wikipedia.org/zh-tw/Windows%E7%BB%84%E4%BB%B6%E5%88%97%E8%A1%A8)|[Microsoft Windows components](https://en.wikipedia.org/wiki/List_of_Microsoft_Windows_components)

## IPAS 中階考題【題組】 110年度第五題組 nc == Netcat 
```
小張為某公司資安工程師，其使用某工具並輸入了下列的指令執行：
nc -vzw5 192.168.0.1 1-2048(操控端)
nc -v -z -w5 192.168.0.1 1-2048(操控端)
nc -ltp 80(操控端)
nc -l -p 80 < /test.txt(操控端)
nc -t -p 80 < /test.txt(操控端)
nc -g -p 80 > /test.txt(操控端)
nc -g -p 80 < /test.txt(操控端)
nc -l -p 80(操控端)
```
```
題組背景描述如附圖。請問小張使用此工具的主要目的為下列何者？
(A) NetChannel 工具通常使用於網路管理情境之下，主要目的為建立 網路通道之用
(B) NoCommand 工具通常使用於將 DOS Command 轉換為 GUI 介面 執行
(C) NoCommunication 工具通常使用於建立雙方之通訊連線
(D) NetCat 工具通常使用於網路管理情境之下，亦為滲透測試常用工 具之一
```
```
題組背景描述如附圖。關於附圖兩個指令的執行結果，何者正確？
(A) 結果相同，對 192.168.0.1 主機進行 vpn 連線，且連線時間設定 2048 秒
(B) 結果不同，對 192.168.0.1 主機進行監聽，且監聽時間設定 2048 秒
(C) 結果相同，對 192.168.0.1 主機之 TCP port 1-2048 進行掃描，且 連線逾時設定 5 秒
(D) 結果不同，對 192.168.0.1 主機之 UCP port 1-2048 進行掃描，且 連線逾時設定 5 秒
```
```
複選題
題組背景描述如附圖。請問題目中指令 nc -ltp 80（操控端）的執行結 果為下列何者？（複選）
(A) 關閉 telnet 模式
(B) 啟動 telnet 模式
(C) 阻斷 80 port
(D) 指定 80 port 為監聽 port
```
```
題組背景描述如附圖。
請問操控端下達何種指令時，等待接聽 TCP 80 port，若接收到連線，就可以將 test.txt 傳送給對方？
(A) nc -l -p 80 ＜ type test.txt（操控端）
(B) nc -t -p 80 ＜ type test.txt（操控端）
(C) nc -g -p 80 ＞ type test.txt（操控端）
(D) nc -g -p 80 ＜ type test.txt（操控端）
```


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


