# MyFirstWebSecurity 網站滲透測試研習營

## 網站架構與網站應用程式開發
- 網站協定(Web Protocols)
  - HTTP 1.1/2.0/3.0
  - HTTPs 
- 網站伺服器(Web Server)
  - Apache/Nginx ==> PHP
  - 微軟IIS  ==> ASP.NET
  - Tomcat ==> JSP(Jakarta Server Pages (JSP; formerly JavaServer Pages))
  - Django/Flask  ==> Python
  - Node.js  ==> Javascript
  - ....
- 網站應用程式(Web Application)
  - 客戶端(Client-Side)網站應用程式
    - 核心程式: HTML  CSS Javascript
    - Framework(數不清的開發框架)
      - Vue.js  angular.js D3.js tensorflow.js..............  
  - 伺服器端(Server-Side)網站應用程式
    - PHP
    - ASP.NET
    - ................   
- Web Programming 實戰研習營
  - XAMPP
  - HTML
  - CSS
  - Javascript
  - PHP 

## 網站資安威脅與安全強化
- Web 攻擊
  - 攻擊網站協定(Web Protocols)
    - HTTP Flood DDoS attack
  - 攻擊網站伺服器(Web Server)
  - 攻擊網站應用程式(Web Application)
    - Html Smuggling Attack  
- 網站資安威脅
  - OWASP Top 10:2021
    - https://owasp.org/www-project-top-ten/ https://owasp.org/Top10/zh_TW/ 
  - OWASP Top 10 API Security Risks(2023)
- 安全強化
  - [OWASP Top Ten Proactive Controls 2018](https://owasp.org/www-project-developer-guide/release/implementation/documentation/proactive_controls/)
  - WAF(Web Application Firewall) 
- 網站安全測試:框架
  - OWASP Web Security Testing Guide(WSTG)
  - OWASP [Offensive Web Testing Framework (OWTF)](https://owasp.org/www-project-developer-guide/release/verification/tools/offensive_web_testing_framework/)
  - OWASP 其他安全測試
    - [OWASP Mobile Application Security Testing Guide (MASTG)](https://mas.owasp.org/MASTG/) 
- 網站安全測試:實戰
  - 網站原始碼檢測
  - 網站漏洞掃描
  - 網站滲透測試 

## 網站滲透測試
- 網站漏洞平台環境建置(使用docker建置虛擬環境)
  - 下載Linux
  - DVWA測試環境建置
- 網站漏洞(1)必知的injection 攻擊
  - command injection
  - SQLi(SQL injection) 
- 網站漏洞(2)File inclusion 漏洞
- 網站漏洞(3)File upload 漏洞

## 延伸學習
- 其他漏洞測試
- 更多SQLi
  - [Hacking Articles|How to set up SQLI Lab](https://www.hackingarticles.in/set-sqli-lab-kali/)
  - [Hacking Articles|Comprehensive Guide to Sqlmap (Target Options)](https://www.hackingarticles.in/comprehensive-guide-to-sqlmap-target-options/)
- 其他網站滲透測試環境建置(使用docker建置虛擬環境)
  - OWASP WebGoat | OWASP Foundation
    - [WebGoat](./WebGoat.md) 
  - [bee-box(bWAPP)](bWAPP.md)
  - OWASP Mutillidae II
    - https://owasp.org/www-project-mutillidae-ii/
    - https://github.com/webpwnized/mutillidae-docker
    - https://github.com/webpwnized/mutillidae
    - 教學影片[Using Mutillidae II](https://www.youtube.com/playlist?list=PLZOToVAK85MrsyNmNp0yyUTBXqKRTh623)
  - [OWASP Vulnerable Web Applications Directory (VWAD)](https://owasp.org/www-project-vulnerable-web-applications-directory/)
- 其他滲透測試
  - [OWASP Vulnerable Container Hub(VULCONHUB)]() 

