# 攻防情境說明
![攻防情境說明](scenario.png)

- 攻擊機 Kali Linux
- 靶機 metasploitable3 

# 攻防實戰(1)攻擊
# 攻防實戰(2)Windows防禦
- 網路連線偵測 ==> netstat
![netstat]()
- 終結 惡意網路連線 ==> 小小抱怨 : 教科書及linux 都是用`process(行程)` 微軟硬是要新創`工作(Task)` 
  - `工作`管理員(`Task` Manager)
    - [Windows 10 開啟「 工作管理員 」的11種方法](https://walker-a.com/archives/3436) 
  - tasklist
  - taskkill [微軟官方說明](https://learn.microsoft.com/zh-tw/windows-server/administration/windows-commands/taskkill)
    - /PID
    -  /F 參數強制進程終止，這對於許多不想關閉的討厭任務很有用。 
- 課堂學習
  - [基本Windows技術](BasicWindows.md)
  - Windows/Linux常用網路指令
  - 工作排程器(Task Scheduler)~~[中文版](https://learn.microsoft.com/zh-tw/windows/win32/taskschd/about-the-task-scheduler) [英文版](https://learn.microsoft.com/zh-tw/windows/win32/taskschd/task-scheduler-start-page)
    - [Windows 工作排程器：每天自動關機教學與範例](https://officeguide.cc/windows-task-scheduler-auto-shutdown-tutorial/) 

# 延伸學習
- [滲透測試](PT.md)
- [更多Kali linux 學習](Kali202304.md)
- [靶機(metasploitable3)](metasploitable3.md)
- 後續研讀
  - [Log4J 漏洞分析與Penetration Testing](https://www.hackingarticles.in/a-detailed-guide-on-log4j-penetration-testing/)
  - 滲透測試專題 Hacking Articles
    - [Penetration Testing](https://www.hackingarticles.in/penetration-testing/)
    - [Web Penetration Testing](https://www.hackingarticles.in/web-penetration-testing/)
- 更多紅藍攻防
  - Red team 滲透測試靶機
    - [Hack The Box: Hacking Training For The Best](https://www.hackthebox.com/)
    - [TryHackMe | Cyber Security Training](https://tryhackme.com/)
    - [VulnHub| Vulnerable By Design](https://www.vulnhub.com/) 
  - Blue Team
    - [LetsDefend - Blue Team Training](https://www.letsdefend.io/) 

