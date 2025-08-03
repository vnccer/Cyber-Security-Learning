# my-first-pentest
## 实验环境：
1.IP/MAC  
Metasploitable2:192.168.174.130；00:0c:29:0c:e9:d4  
Kali Linux:192.168.174.129；00:0C:29:be:9d:0b  
<img width="600" height="160" alt="image" src="https://github.com/user-attachments/assets/7e4115b6-46e4-41a9-9d05-c3c1878763a8" />
<img width="795" height="197" alt="image" src="https://github.com/user-attachments/assets/c05fcb3b-739b-45e2-af64-d9eb5e3cb1b4" />
2.eth0端口中，inet: 表示这是一个 IPv4 地址配置。/24: 这代表子网掩码是 255.255.255.0，它定义了本地网络的范围，意味着所有 192.168.174.x 的地址都在同一个局域网内。brd 192.168.174.255: 这是当前网络的广播 IP 地址。scope global: 表示这个 IP 地址是全局可达的（可以在局域网内被其他机器访问）。  
3.inet6: 表示这是一个 IPv6 地址配置。fe80::...: 这是一个链路本地地址 (Link-Local Address)。它只能用于在同一个物理网络内通信，不能访问互联网，通常由设备自动生成。scope link: 表明这个 IPv6 地址只在当前链路（局域网）有效。  
