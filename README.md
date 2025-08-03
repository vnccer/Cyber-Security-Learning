# my-first-pentest
## 一、实验环境：
1.1 1IP/MAC  
Metasploitable2: 192.168.174.130  00:0c:29:0c:e9:d4  
Kali Linux: 192.168.174.129  00:0C:29:be:9d:0b  
<img width="600" height="160" alt="image" src="https://github.com/user-attachments/assets/7e4115b6-46e4-41a9-9d05-c3c1878763a8" />  
<img width="795" height="197" alt="image" src="https://github.com/user-attachments/assets/c05fcb3b-739b-45e2-af64-d9eb5e3cb1b4" />  


## 二、使用工具
nmap
## 三、攻击与过程分析
3.1 成功ping通  
<img width="498" height="86" alt="image" src="https://github.com/user-attachments/assets/3b454b60-dce6-4674-8c13-756d83349fa1" />  
3.2 nmap扫描Metasploitable2  
<img width="708" height="773" alt="image" src="https://github.com/user-attachments/assets/9f3c541b-9fcc-41eb-8381-f4df1729a919" />  
<img width="616" height="589" alt="image" src="https://github.com/user-attachments/assets/5f3fd658-3baa-4055-ab97-03795a881d18" />  
3.3 搜索vsftpd 2.3.4的漏洞利用模块  
<img width="1202" height="185" alt="image" src="https://github.com/user-attachments/assets/a0dda320-6de0-4a55-99ed-61ce360ab538" />  
3.4 使用找到的漏洞利用模块  
<img width="593" height="65" alt="image" src="https://github.com/user-attachments/assets/24a3de6f-d9ee-4b7d-ad90-db460102743c" />  
3.5 查看需要设置的参数  
<img width="1185" height="465" alt="image" src="https://github.com/user-attachments/assets/83fb922e-f9cc-4088-bc70-9ca60c21240e" />



## 四、发现与漏洞总结
4.1 eth0端口中，inet表示IPv4 地址配置。/24代表子网掩码是255.255.255.0，定义了本地网络的范围，意味着所有192.168.174.x的地址都在同一个局域网内。brd 192.168.174.255是当前网络的广播IP地址。scope global表示这个IP地址是全局可达的（可以在局域网内被其他机器访问）。  
4.2 inet6表示这是一个IPv6地址配置。fe80::...: 这是一个链路本地地址 (Link-Local Address)。它只能用于在同一个物理网络内通信，不能访问互联网，通常由设备自动生成。scope link: 表明这个IPv6地址只在当前链路（局域网）有效。  
4.3 CHOST攻击机Kali，CPORT攻击机端口,Proxies隐藏攻击机真实ip,RHOSTS目标主机,RPORT主机上漏洞端口号,
