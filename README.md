# sf
代收代付系统,支持:银行卡、支付宝、USTD、短信、越南银行、印度银行自动转账查转，可作为三方和四方系统自由切换
# 使用说明
	1. 支持 农业银行  工商银行 邮政银行  招商银行  平安银行 交通银行 兴业银行 平安银行 浦发银行  招商银行 自动收款回调，自动转账
	1. 支持宝塔Linux面板
	2. 视频效果见doc目录：中行.mp4,工行.mp4,建行.mp4,农行.mp4,支付宝.mp4
	3. 支持印度paytm自动转账，自动收款回调
	4. 支持越南：TCB,ACB,VTB,Bidv,TBP
	5. 支持云手机（虚拟机）
	6. 售后服务请联系 Telegram：@live0086
# 转账视频
[![Watch the video](https://raw.github.com/GabLeRoux/WebMole/master/ressources/WebMole_Youtube_Video.png)](https://github.com/ytjjyy/sf/blob/master/doc/TCB_A.mp4)
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
		数据库备分见：$path/daifu/doc/db.sql
	4.	运行$path/daifu/cmd/main数据服务,及可以正常运行,注$path为环境变量
	5.	管理员账号和密码都是：admin，系统中有：管理员、代理、码商(支持三级码商码结算)、商户、运营5种角色，跟据需要自行创建
	


# 系统功能
	1.	商户管理: 支持商户入驻，费率设置，商户需要向平台方提供相关的资料备案。
	2.	定额买币: 提交保证金可开启抢单任务
	3.	账户管理: 渠道账户管理，支持共享账户（个人商户）及自有账户。
	4.	支付下单: 可手动批量下单、提供退款服务。
	5.	通知模块: 处理第三方支付渠道的异步通知，并将处理结果同步至业务系统。
	6.	对账处理: 实现支付系统的交易数据与第三方支付渠道交易明细的自动核对（通常T+1），确保交易数据的准确性和一致性。
	7.	挂码系统: 支持，银联，微信，支付宝二维码上传,支持微信和支付宝回调。
	8.	商户结算: 计算收款交易中商户的收益,根据清算结果，将资金划拨至商户对应的资金帐户中,支持三级代理商户结算。
	9.  手动转账:手转账提交转账凭证，后端审核。
	10.  卡商:支持银行卡对银行卡自动转账,过程全自动化，无需申请银行API接口,自动转账视频演示见（doc/demo.mp4）
	11.  PatTM:支持印度paytm自动转账，自动收款回调
  
  
# API接口
	1.	单笔代付接口
	2.	单笔代收接口
	3.	交易查询接口
	4.	余额查询接口
	5.	打款通知回调接口
  
# 开发技术
	1.	Golang+CentOS+Mysql+Nginx+Vue
	2. 	商户API对接文档见doc/dev.html
	3. 	平台数据采用RSA2加密传输
