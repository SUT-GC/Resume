
## 勾超

@(面试)



* 联系方式：[17521175553]() | [sut_gouc@foxmail.com]()
* 院校专业：一本 | 沈阳工业大学.计算机科学与技术 | 2017.07毕业

## 技能清单

* 语言：Java | Python
* 框架：Spring | Hibernate | Mybatis
* 工具：Redis | Mysql | MQ | ES
* 其他：DP | Git | Gradle | Maven 

## 工作经历

#### [SoulApp](https://www.soulapp.cn/) **[[ 2019.12 - ... ]]()**
<br/>	

* **[商业化系统搭建]()**
	[S] 公司为了增加收入，要搭建商业化系统     
	[T] 增加用户充值，商品售卖等能力，增加业务玩法，使用户贡献充值金币    
	[A] 搭建五大基础服务：商品模块、账户模块、订单模块、账单模块、用户权益模块；实现三大业务链路：充值&买会员、买虚拟商品、送礼物等；丰富娱乐体验玩法：用户背包，礼物榜单等；还搭建了支付领域的业务监控，画出了soul的第一个业务监控面板。    
	[R] 每天50w+次的送礼支撑，10w+次的充值操作，随着soul的业务发展，为soul的商业化之路提供了帮助    
<br/>	

####  [饿了么](https://www.ele.me/home/) **[[ 2016.10 - 2019.12 ]]()**
<br/>	

* **[店铺架构CQRS改造-主导](http://int32.me/blog/2019/07/30/shopcqrs/)** [[详情]](http://int32.me/blog/2019/07/30/shopcqrs/)
	[S] 店铺服务是公司核心服务，但变更频繁，代码逻辑复杂，稳定性差，当前架构稳定性999很难达到    
	[T] 根据店铺服务读多写少、读关键写次之的特性，进行“CQRS”架构改造；搭建完善的监控报警机制；组建常态化压测机制    
	[A] 将店铺服务拆成B领域服务(command)C聚合服务(query)，B支撑单领域内业务的读写需求，C负责将领域数据聚合后透出给关键链路只查不写。B和C之间的数据聚合和一致性由另一个单独的“助手”服务来保证；用MQ延迟队列搭建数据报警；利用MQ分布式优势保证数据快速恢复    
	[R] 核心服务变更频次显著下降，代码简单清晰，维护成本低,   稳定性超9999 (现近700K Qps)    
<br/>	

* **[购物车重构-主导](http://int32.me/blog/2019/07/30/tradecart/)** [[详情]](http://int32.me/blog/2019/07/30/tradecart/)
	[S] 饿了么购物车Python转型Java + 模型重构    
	[T] 短时间内熟悉购物车相关所有业务；服务Python转Java；领域模型抽象，能够支撑后面业务发展；支持平滑灰度和回切    
	[A] 数据接口重新设计，划分商品区和玩法区，将业务玩法剥离，数据层不感知具体玩法，更灵活；代码重新分层，区分Tunnel和Repository层，将基础组建和业务剥离，方便以后替换基础组建 - [代码架构](http://int32.me/blog/2019/12/03/three-tier/)；新老购物车缓存同步方案，支持平滑切换和回切;     
	[R] 平稳上线无事故；有能力支撑购物车业务更多玩法    
<br/>

* **[物流压力平衡系统2.0搭建-独立开发(+专利申请)](http://int32.me/blog/2018/03/30/lpd-balance/) ** [[详情]](http://int32.me/blog/2018/03/30/lpd-balance/)
	[S] 物流运力不足会逆向调控配送信息来减轻运力压力，老系统吞吐能力差，分布式系统下调控顺序很难保证，无补偿机制，执行链路很难跟踪，维护难度高    
	[T] 利用分布式系统优势提高调控吞吐量， 保证分布式系统调控处理顺序，搭建补偿机制，搭建监控报表机制    
	[A] 入口处并发限制做自保，使用MQ来充分利用分布式系统的并发优势，使用Redis构建分布式锁保证顺序，用状态记录和定时Job确保任务执行成功，利用大数据工具做数据报表(锦上添花，给管理层看)    
	[R] 系统日吞吐量由0.5kw到3.5kw的提升，单机房支持 30w/5min 次调控， 由一个重点看护的系统改造成了一个基本不用关注的系统     


## 个人总结

* 喜欢行业，好奇技术，认真负责，热爱生活
