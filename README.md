 # pierced
钉钉内网穿透

TCP 穿透需要在数据库里面执行：  
GRANT ALL PRIVILEGES ON * . * TO root @ '%' IDENTIFIED BY '123456';  
FLUSH PRIVILEGES;  
数据库连接命令：  
mysql - h vaiwan.com - u root - p - P 1234 //端口号地址  


Windows 内网穿透:  
(1)cd windows_64 （cmd 进入 windows_64 文件夹中）  
(2)ding - config = ding.cfg - subdomain = zcrkey 8080 （ding.cfg 配置文件 subdomain: 自定义名称 8080 端口号）  
	说明：  
	-config 内网穿透的配置文件，按命令照示例固定为钉钉提供的. / ding.cfg，无需修改  
	-subdomain 您需要使用的域名前缀，该前缀将会匹配到“vaiwan.com”前面，例如你的subdomain是zcrkey，启动工具后会将zcrkey.vaiwan.com映射到本地。  
	端口 您需要代理的本地服务http - server端口，例如你本地端口为8080等  
  
	启动本地服务（8080端口）后，你访问http: //zcrkey.vaiwan.com/xxxxx都会映射到 http://127.0.0.1:8080/xxxxx  （xxxxx为项目名称）  
  
	访问地址：http: //zcrkey.vaiwan.com/你的项目名称/  
	举例：项目名称 TEST 首页 index.html  
	http: //zcrkey.vaiwan.com/TEST/index.html  
  
其他说明  
	基于 ngrok 实现内网穿透  
