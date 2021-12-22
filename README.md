# 蚂蚁代收代付系统🐜🐜🐜
代收代付系统,支持:银行卡、支付宝、USTD、短信、越南银行、印度银行自动转账查转，可作为三方和四方系统自由切换
# 系统功能
	1.国内银行: 农业银行、工商银行、邮政银行、招商银行、平安银行、交通银行、兴业银行、平安银行、浦发银行自动收款回调，自动转账
	2.印度银行: PayTM自动转账、自动收款回调 云手机（虚拟机）
	3.越南银行: TCB,ACB,VTB,Bidv,TBP 云手机（虚拟机）
	4.挂码模块: 支付宝、USTD、微信
	5.商户模块: 支持商户入驻、费率设置、通道模式自由切换
	6.安全模块: 支会谷歌验证码
	7.商户结算: 根据订单结算费率，将资金划拨至商户资金帐户中,支持代理商户结算
	8.售后服务请联系 Telegram：@live0086
# API接口
	1.单笔代付接口
	2.单笔代收接口
	3.交易查询接口
	4.余额查询接口
	5.打款通知回调接口
# 视频效果
越南TCB:

https://user-images.githubusercontent.com/12911640/147103583-061309dc-460f-4fbc-96f2-a561e710f8c7.MOV
# 转账App截图
![image](https://github.com/1752325542/daifu/blob/master/doc/1x.png)
![image](https://github.com/1752325542/daifu/blob/master/doc/2x.png)
	
# 系统截图
![image](https://github.com/1752325542/daifu/blob/master/doc/1.png)
![image](https://github.com/1752325542/daifu/blob/master/doc/9.png)
![image](https://github.com/1752325542/daifu/blob/master/doc/2.png)
![image](https://github.com/1752325542/daifu/blob/master/doc/3.png)
![image](https://github.com/1752325542/daifu/blob/master/doc/4.png)
![image](https://github.com/1752325542/daifu/blob/master/doc/5.png)
![image](https://github.com/1752325542/daifu/blob/master/doc/6.png)
![image](https://github.com/1752325542/daifu/blob/master/doc/7.png)
![image](https://github.com/1752325542/daifu/blob/master/doc/8.png)
# App截图
![image](https://github.com/1752325542/daifu/blob/master/doc/10000.jpg)
![image](https://github.com/1752325542/daifu/blob/master/doc/10001.jpg)
![image](https://github.com/1752325542/daifu/blob/master/doc/10002.jpg)
![image](https://github.com/1752325542/daifu/blob/master/doc/10003.jpg)


# 系统安装
	1. CentOS8.0以上系统
	2.	安装Nginx,
		yum install -y nginx  
		将站指向程序中的$path/daifu/web目录
	3.	安装Mysql数据库
		yum -y install mysql-server
		service mysqld restart
		数据库备分见：$path/sf/doc/db.sql
	4.	运行$path/sf/cmd/main数据服务,及可以正常运行,注$path为环境变量
	5.	管理员账号和密码都是：admin，系统中有：管理员、代理、码商(支持三级码商码结算)、商户、运营5种角色，跟据需要自行创建
  
# 开发技术
	1.	Golang+CentOS+Mysql+Nginx+Vue
	2. 	商户API对接文档见doc/dev.html
	3. 	平台数据采用RSA2加密传输
