# Filman
Filman空间管理系统（Filecoin分币系统）
集用户、产品及订单、营销、收益分配、资产、数据统计、批量打币工具、内容管理为为一体的存储空间分发系统

## 业务场景   
### 满存空间  

用户购买空间，空间+抵押，收取节点服务费；抵押为用户资产，服务终止释放给用户，收益分配按比例执行
		
### 联合空间

用户承担抵押，其它一切费用均由节点服务商承担；抵押为用户资产，服务终止释放给用户，收益分配按比例执行
		
### 服务器托管

用户支付服务器硬件和托管费用，充入抵押激活，约定n天存满。封装会有持续过程，需限额限时出售。
		
## 功能模块
### 用户	
		注册登录
			支持手机号注册，手机号+密码登录，手机号+验证码登录
			
		用户管理
			编辑手机、邮箱、认证状态、充值、扣减
			
		邀请机制
			可获得注册奖励和订单奖励
### 产品	
		产品管理
		产品前台展示
### 订单	
		产品购买流程
			用户支付USDT购买空间，支付FIL用于抵押和封装gas
			
		订单管理
		产品封装交付
		订单到期处理
### 资产	
		充值流程
		提币流程
		账户互转流程
		收益分配
			分配计算基数
				指定节点奖励、取全网平均奖励、自定义奖励
			释放规则
				每日区块奖励25%立即释放，75%按1/180每日释放
			分配时间
				确认基础收益后，自动分发收益
		抵押释放
		抵押记录
		资金流水
### 风控	
		余额校验
### 内容	
		内容管理
			快讯、文章、帮助
		内容前台展示
### 设置	
		基本设置
		APP升级设置
		系统升级
		财务设置
		第三方API设置
		Filecoin设置

## 主要业务流程    

### 用户使用流程
* 用户注册登录
* 用户充值USDT、FIL
* 用户购买产品
* 平台封装交付
* 每日收益分配
* 用户提币

### 产品生命周期
* 创建产品分类
* 创建并上架产品
* 封装交付订单
* 产品服务期内
* 产品到期，抵押释放（到期产品，用户可选择延期，延期功能后续添加功能）

### 充值流程、提币流程
* 平台币种配置
* 用户选择充值通证

### 收益分配流程
* 收益分配确认或更新收益分配源数据后全自动执行
* 平台自动生成计算源数据 or 人工输入分配数据
* 判断订单有效期
* 按订单计算当日奖励、当日奖励当日释放、历史奖励当日释放
* 按天统计当日数据
* 按用户统计该用户汇总数据

### 邀请奖励流程
* 用户进入邀请页面，默认自动触发邀请权限，分配邀请码
* 分享邀请链接或二维码
* 非注册用户通过连接或二维码注册账户
* 注册完成，引导下载
