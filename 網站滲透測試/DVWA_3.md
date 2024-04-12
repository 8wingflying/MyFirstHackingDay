# File upload vuln.檔案上傳漏洞



## 正常:上傳圖片

![DVWA_FILEUpload_2](DVWA_FILEUpload_2.png)


## 看看上傳的貓 
- http://127.0.0.1:8080/hackable/uploads/cat.jpg


![DVWA_FILEUpload_3](DVWA_FILEUpload_3.png)


## 攻擊:那上傳一隻webshell?
- 使用weevely

![DVWA_FILEUpload_4](DVWA_FILEUpload_4.png)


## 使用weevely產生要密碼輸入的網頁木馬 weevely generate A888168 legitfile.php
![DVWA_FILEUpload_5](DVWA_FILEUpload_5.png)


## 上傳木馬給他

![DVWA_FILEUpload_6](DVWA_FILEUpload_6.png)


## 


![DVWA_FILEUpload_7](DVWA_FILEUpload_7.png)


## 透過網頁木馬遠端執行程式

![DVWA_FILEUpload_8](DVWA_FILEUpload_8.png)


## 登入docker 查看是否已上傳成功
- /var/www/html

![DVWA_FILEUpload_9](DVWA_FILEUpload_9.png)


## 撰寫webshell後上傳後執行 ==>
![DVWA_FILEUpload_10](DVWA_FILEUpload_10.png)

