## Metasploit

## Metasploit modules(模組): 5605 Metasploit modules:
- 1.auxiliary輔助模組 (1241)
- 2.encoder編碼器模組 (47)
- 3.evasion 規避模組(9)
- 4.exploit漏洞利用(就是攻擊拉)模組 (2409)
- 5.nop (11)
- 6.payload有效載荷模組 (1465)
- 7.post (423)

## auxiliary輔助模組 （1241）
- 不會攻擊目標
- 用來執行有用的任務：
  - 管理 - 修改、操作或操作目標計算機上的某些內容
  - 分析 - 執行分析的工具，主要是密碼破解
  - 收集 - 從單個目標收集、收集或枚舉數據
  - ??拒絕服務 - 使目標計算機或服務崩潰或變慢
  - ★★掃描 - 掃描目標系統以查找是否存在某個已知漏洞
  - 伺服器支援 - 為常見協定（如 SMB、FTP 等）運行伺服器

## encoder編碼器模組 （47）
- 編碼器獲取有效負載的原始位元組並運行某種編碼演算法，如按位 XOR。
- 這些模組可用於對錯誤字元（如空位元組）進行編碼。

## evasion規避模組 （9）
- 規避模組使Metasploit 用戶能夠生成旨在規避防病毒軟體（如 Windows Defender）的規避有效負載，而無需安裝外部工具。

## 漏洞利用模組 （2409）
- 漏洞利用模組用於以允許框架執行任意代碼的方式利用漏洞。
- 執行的任意代碼稱為有效負載。


## Nop 模組 （11）
- Nop 模組是“No Operation”的縮寫
- 可生成一系列“No Operation”指令，這些指令不會產生任何副作用。
- NOP 通常與`Stack Overflow(堆疊緩衝區溢出)`結合使用。

## 有效載荷模組 （1465）
- 在 Metasploit 漏洞利用模組的上下文中，有效負載模組封裝了作為漏洞利用成功結果而執行的任意代碼 （shellcode）。
- 這通常涉及創建 Metasploit 工作階段，但可能會執行代碼，例如添加使用者帳戶，或執行簡單的 pingback 命令來驗證代碼執行是否成功針對易受攻擊的目標。


# [GITHUB上的原始碼](https://github.com/rapid7/metasploit-framework/tree/master)
- 使用ruby開發
# pymetasploit3 – Metasploit Automation Library
