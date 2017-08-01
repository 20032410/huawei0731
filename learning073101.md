# 华为0731
### HCNA，初级培训
1.	老师，吴万燊，15280089050
2.	了解WLAN，掌握华为WLAN基本业务配置
3.	6天，理论+培训，考试+平时成绩，Z5-A532
4.	华为颁发工程师整合素
5.	华为技术支持网站，华为电子文档系统
	* 可离线下载
6. 华为产品定义社区
	* 更好用户体验
	* 下载app，加入华为企业用户提升圈
7. 上课时间9点-11点40
	1点半到-4点半
8. WLAN历史概述
	* 无线局域网
	* 1971，夏威夷，ALOHAnet
	* IEEE，1970
	* 2003， WiFi、3G、4G、蓝牙
9. 无线网络分类
	* 个人无线网，Wireless Personal Area Network
	* 无线局域网，小于100米
	* 无线城域网，<5Km
	* 无线广域网,<15Km
10. 无线传输技术：
11. Wi-Fi是采用了802.11技术的WLAN
	* 2.4G，5G频段，但中国主要用149-165信道
	* 802.11 b/g/n，支持2.4GHz,下载一般7M/s
	* 802.11 a,n,ac，下载一般10M/s
	* 第一代WLAN： 11b
	* 第二代： 11a/g
	* 第三代WLAN: 与WiMAX融合，11n多射频模块，合路
	* 可扩展性，mesh组网，无线传输，不需要通过有线来部署（问题，距离问题）WDS，无线桥接
	* 移动公司部署的CMCC,CMCC-EDU,CMCC-WEB
	* 运营模式，以租代卖

### WLAN标准组织
1. 国家无线电管理委员会认证(State Radio Regulatory Commission of the People's Republic of China)
````
室内放装,100mw
室外，500mw
````
2. FCC
3. ETSI
3. IEEE:美国电气和电子工程师协会
4. WiFi联盟，全称为国际Wi-Fi联盟组织（WiFi Alliance）
5. IETF
6. WAPI，无线局域网鉴别

### 无线射频基础知识介绍
1. 周期、频率，c
2. 2.4G，干扰严重，5G相对比较干净
3. 调制与解调
4. 吸收
5. 反射
6. 折射
7. 衍射
8. 衰减
9. 一般限制在10-15m
10. 电缆衰减、障碍物、障碍物、噪音干扰、长距离
11. 增益，接收增益，（AP，STA？）
12. 菲涅尔区，要在菲涅尔区内没有障碍物

### WLAN频段介绍
1. ISM频段
2. WLAN频段，2.4G，划分为14个信道，20MHz载波信道，间隔5M
3. 在中国，1到13信道被允许使用
4. 一般把11Mbps定义为低速率，通常会被禁用掉
习惯用1，6，11；2，7，12
5. 5G，149，153，157，161，165，使用非重叠频段，可以使用信道绑定
````
红外遥控，无线耳机，
微波炉
无线摄像头
雷达，5G
无绳电话
医院（零漫游），从重叠的区域切换（估计几ms），合路馈线，或者智分，室内分路
````

### 华为WLAN产品介绍
1. 锐捷，AP320，520、华三（电信），华为商企合作
2. AC Access controller
3. AP Acess point
	* 胖AP+++无线路由器
	* 廋AP---通过AC集中管理控制
	* 云AC---
4. 无线控制器，AC6005，AC6605，盒式
	* 插卡式，业务板槽
	* 轨交专用AP，支持存放视频
	* 敏捷分布式AP，12台、24台，加一个交换机，48台
	* 新一代11ac AP，室外AP，AP4030N
	* 室外AP，外置天线（定向，全向）
5. AC6005
	* 1U
	* 可管理AP：4-256个
	* 适合小型企业
	* 支持8PoE或4PoE
	* 支持CLI、WEB和eSight管理，（网管软件）
	* ESSID数量：1K
6. AC6605
	* 适合中小型企业
7. ACU2
	* S交换机，适配S127、97、77
	* 最多可管理2048 AP
8. X1E系列随板无线接入控制单板
	* 大型企业
9. WLAN AP产品命名规则
	* MIMO，150Mbps *3=450， 目前醉倒4**4，
10. 敏捷分布式AP
11. AC应用场景
	* AC对AP进行控制与管理：
	* AC一般不直部，一般旁挂
	* AC通过控制隧道进行AP，CAPWAP
12. AP室内放装
	* A中等面积的盲区覆盖或重要共用场景
13. AP室外系统
	* 操场、体育场、校园
14. 网管系统eSight
	* 要提供MID库
15. POE简介
	* IEEE 802.3af PoE标准，最大输出功率15.4W
	* IEEE 802.3at PoE标准，最大输出功率30W
	* PSE
	* PSU
	* PD
	* PI
	* 网线连ap时一般不超过80m
16. 供电方式
	* PoE供电
	* 交流电源适配器
	* PoE电源适配器供电，AMI
### 华为VRP介绍
1. 通用路由平台，Versatile Routing Platform
	* 网络操作系统
	* 支撑多种设备的软件平台
	* 提供TCP/IP路由服务
2. VRP演进
	* VRP5，VRP8，需要加入commit
	* console线
	* putty
	* 华为一般9600，国内有些是115200，右边3个勾，都取消
	*配置命令
3. 用户视图<>
	*查看display,
4. 系统视图system-view，[]
5. 接口视图Ethernet 0/0/1[]
6. WLAN视图-wlan-view][]
7. tab键补全
8. 错误信息
9. 通过telnet登录设备
	* 通过Console口登录AC6605
	* 配置AC的名称
	* 配置AC管理IP
	* 配置AC的Telnet服务
10. 配置
	* sysname ACI
	* ip address 10.10.10.10 255.255.255.0
	* quit
	* telnet server enable
	* aaa 
	* user-interface vty 0 4
	* protocol inboud all
	* authentication-mode aaa
	* return
	* display users
	* display user-interface
11. 通过SSH登录设备，
	* Web
	* 界面配置
	* ssh client first-time enable,客户端到客户端
	* stelnet 127.0.0.1
12. 升级AC
	* display version
	* 3CDMon
	* display device
	* 也可以使用tftp，udp形式，Bootrom
	* dir,ls
	* mget,mput,
	* startup system-software 
	* reboot
	
## 0801
### 升级AP
1. AP支持三种版本升级模式
	* ac-mode
	* ftp-mode
	* sftp-mode
2. 进入wlan视图模式为FTP模式
3. 查看AP类型
4. 配置FTP服务器
5. 查询Ap的状态
6. 重启AP（记住）
7. 验证AP的版本

### AC-mode
1. 熟练度问题

### WLAN拓扑介绍
1. SSID （Service SetIdentifier）：表示无线网络标识，用来区分不同的无线网络
2. AP支持多SSID
3. BSS，一个AP和多个无线终端
4. ESS，由一个或多个BSS组成
5. Ad-hoc
6. DS
7. WDS，无线分布式系统，组成，信道必须一致，点到点，点到多点
	* Root AP
	* Leaf AP
	* 点到点
	* 点到多点
	* 手拉手模式
	* 背靠背
	* 最大长度，Root、Middle、Leaf
8. Mesh基本概念
	* WMN，Portal节点
	* MPP
	* MP
	* MAP

### CAPWAP
1. AP介绍
2. 胖AP，FAT AP
3. 廋AP, FIT AP
	* 便捷性
4. 保证10%--15%的覆盖范围
	* 二层漫游，指的是同网段的漫游
	* 三层漫游，指的是跨网段的漫游，将从原网段的AP出去
5. CAPWAP（无线节点控制和配置协议）

### WLAN转发模型
1. 直接转发
2. 隧道转发
	* 针对数据
	* 控制，udp，5246
	* 数据，udp，5247
3. 静态AP发现AC
	* 静态，AP配置有预配置静态AC的IP列表
	* 动态，二层广播，AP管理地址和AC原地址在相同网段
	DHCP，option 43，可将AC源地址配置进去
	DHCP，option 15 DNS，告诉AP一个域名，如aaa.domain;DNS aaa.domain=ac.源地址
	AC源地址，跟AP建立CAPWAP的地址（可手工指定）
4. 认证
	* no-auth，不认证
	* mac-auth，mac认证
	* sn-auth，序列号
5. image data，看数据版本
6. data check 数据检测，看数据是否一致
7. keep alive 保活（维护、维持）数据通道
8. echo request 维护控制信道
9. 配置变更，ac下发配置
10. run 保活数据

### DHCP
1.

### WLAN 组网
1. 二层组网
2. 三层组网
3. 直连式
4. 旁挂式
5. 敏捷分布Wi-Fi方案组网

### 数据转发方式
1. 直连式
	* 直接转发 配置truck口，放行业务vlan
	* 如果是access口，只支持隧道转发
	* 旁挂式组网

### 管理VLAN

### 业务VLAN
1. 用户VLAN，基于用户去区分
2. 

***
### WLAN配置
1. WLAN数据规划表
	* AP 地址池
	* 用户地址池
	* AC源地址，AC上任意接口上地址和AP管理地址互通
	* AP上线，ssid，ssid模板，安全模板，域管理模板（国家码CN）
	* VAP模板：ssid，安全，业务vlan，转发模式，与ap绑定，ap组
	* 用户上网
	