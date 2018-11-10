# 汉风堂外卖订餐系统

---

需求规格说明书
V0.1

---

## 1. 概述
该需求规格说明书详细描述了“汉风堂”外卖订餐系统1.0版本的软件功能需求
和非功能性需求。这一文档计划由实现系统功能和验证系统功能正确的项目团
队成员来使用。除非在其他地方另有说明，这里指定的所有需求都具有高优先
级，而且都需要在1.0版本中得到实现。

### 1.1 项目目的与目标
“汉风堂”外卖订餐系统旨在为南京大学仙林校区的“汉风堂”餐厅提供外卖订餐
平台和送餐员招聘和管理平台，以开展外卖服务拓宽市场，创造更多利润。通
过该系统，南京大学仙林校区的学生可以足不出户在线订购到汉风堂的菜品并
享受送货上门服务，汉风堂经理可以提高菜品、订单、送餐员和应聘者的管理
效率，汉风堂也能招到合适的高质量的送餐员，仙林校区的在住学生也可以通
过送餐来获取日常收入。

### 1.2 术语表
|名词|定义/解释|
|---|---|
|顾客|在线订购汉风堂菜品的食客|
|经理|汉风堂餐厅的经理|
|服务员|汉风堂餐厅的服务员|
|送餐员|通过应聘面试并为汉风堂餐厅送外卖的学生|
|应聘者|希望通过应聘成为送餐员的学生|
|排行榜|描述了送餐员业绩的排行|

### 1.3 参考资料
* IEEE标准
* 《软件需求工程》

### 1.4 版本更新记录
|时间|更新负责人|更新内容|版本号|
|---|---|---|---|
|2018-11-08|恽叶霄|制定规格说明书的框架|V0.1|

## 2. 目标系统总体描述

### 2.1 商品前景

#### 2.1.1 应用背景
“汉风堂”是南京大学仙林校区的一家校内餐厅，经营期间菜品深受学生们的
欢迎，在校内树立了良好的品牌形象。但由于场地大小有限，进店消费人数
较多，还常常有软件学院的学生留在餐厅内写大作业占用座位，该餐厅在营
业时间内经常无法容纳下全部的顾客，顾客因为短时间内等不到位置而离开
的现象时有发生。针对这一现象，该餐厅希望做一些外卖方面的尝试。但是
由于营业环境在学校，周围没有更多的商家，因此无法将送餐服务转给大型
外卖平台。餐厅总经理决定为该餐厅添加一套属于自己的外卖订餐系统，但
是对于外卖服务的效果存在着一系列的担心，包括能否招募到送餐员工、送
餐员工的可靠性和积极性、外卖菜品的销量以及餐厅员工对于订餐系统使用
的上手难度和学习成本。老板希望新建立的外卖订餐系统能够消除他的这些
担忧，确保有一套可靠的送餐员评估和激励机制，能够留下值得信赖的送餐
员，及时处理掉不可靠的送餐员，提高送餐员的工作效率；建立菜品销量的
查看机制，方便推陈出新，及时更新被选菜单；新系统简单易上手，能够提
高“汉风堂”的销量及知名度，获得更多的好评和经济效益。  

#### 2.1.2 业务机遇
“汉风堂”餐厅配置了外卖订餐系统后，能够保证订餐客户、送餐员、接单服
务员、总经理等各方面使用起来都简单易上手，提高效率。客户可以进行方
便快捷的下单，同时可以对菜品、送餐员做出评价，对优质菜品进行社交平
台分享。送餐员可以通过系统进行招募，并有一套关于可靠性的审核评价机
制和工作激励机制。接单服务员能够清楚有条理的接到各方订单，然后将其
高效的传递给后厨出菜，接收顾客反馈的问题。餐厅总经理可以查看一定时
间内各道菜品的销量、进行菜品的撤销和添加、决定送餐员的奖惩。最终，
该外卖订餐系统能够有效提高该餐厅的经济利润，同时降低了管理成本，提
高了各角色使用人员的使用效率，推动餐厅的进一步发展。  

#### 2.1.3 业务需求
BR1:使用系统1个月后，一天的实际顾客数提高20%

BR2: 使用系统3个月后，订单数量提高10%

BR3: 使用系统3个月后，能够招到能力达到一般企业送餐员
订单数40%的学生送餐员

BR4: 使用系统3个月之后，学生送餐员的订单数并没有明显下降

BR5: 使用系统可以达到线上订餐功能

BR6: 使用系统后可以很明确找到高销量菜品

BR7：使总经理、接单员能够在1天之内上手平台，顾客、
送餐员能够在半小时内大概了解平台所有操作


### 2.2 系统结构与职责
系统由三大平台组成。首先是订餐平台，用于给顾客提供在线订餐服务和菜品
评价服务；其次是管理平台，用于为经理提供对菜单、订单、促销、应聘者和
送餐员的管理功能；最后是送餐员平台，用于为送餐员提供便捷的接单、送单
、以及各种信息查询的功能。三大平台互相联系：订餐平台产生的新订单会更
新管理平台中的诸多信息，并在送餐员平台上显示出该订单以供送餐员接单；
订餐平台中的评价会更新管理平台中的菜品信息和送餐员平台的送餐员数据；
管理平台中菜品信息的变动同样会导致订餐平台上的菜品数据的更新；送餐员
平台上产生的送餐员业绩的改动也将会更新管理平台的送餐员相关数据。

### 2.3 用户角色定义
|角色|业务职责|
|---|---|
|顾客|在线订餐、评价菜品和送餐员、分享平台和菜品|
|经理|菜单管理、订单管理、促销策略管理、应聘者管理、送餐员管理|
|服务员|接收订单并通报后厨制作相关菜品|
|送餐员|接单、送单|
|应聘者|身份认证|

### 2.4 系统业务流程
**TODO**

### 2.5 假设与依赖
* 现阶段汉风堂内部人员结构不变动。
* 所有涉众均熟悉并使用Android手机。
* 顾客均在南京大学仙林校区内部进行订餐。
* 学生愿意应聘送餐员以赚取生活费。
* 需要和第三方的支付平台进行集成，可以双向通信和变更。
* 需要和校方进行协作，实现身份认证。


## 3. 详细需求描述

### 3.1 对外接口

#### 3.1.1 用户界面
界面的设计原则是：方便、简洁、美观、一致。系统界面应当做到层次分明，
并且适当使用导航栏提供便捷的操作。
* 输入设备：手机屏幕、键盘、鼠标
* 输出设备：手机屏幕、显示器
* 显示风格：web图形界面
* 显示方式：根据用户使用的终端大小和屏幕大小变化而变化

**TODO**

#### 3.1.2 软件接口
* 使用mysql作为底层数据库，存储系统数据


### 3.2 功能需求


### 3.3 非功能性需求

#### 3.3.1 安全性
* 管理平台和送餐员平台只允许通过登录身份验证的用户使用。
* 顾客不允许访问送餐员平台，除了经理任何人都不允许访问管理平台和服务
器资源。
* 系统提供密保问题找回密码功能。
* 系统需要防止sql注入、xss跨站脚本攻击。
* 用户密码应当多次hash后存储，或者使用加盐hash。

#### 3.3.2 可维护性
* 数据格式发生的变化最多在3天内完成相关修改。
* 如果系统需要增加新的功能，能够在不修改原有体系结构的条件下完成。
* 如果需要迁移，系统需要方便迁移到其他服务器和终端。

#### 3.3.3 易用性
* 系统应当采用扁平化设计风格，减少页面层次。
* 系统应当提供便捷的导航栏跳转。

#### 3.3.4 可靠性
* 网络出现故障后，系统不能故障。
* 服务器出现故障后，系统不能故障。
* 高压并持续运行1小时条件下，系统故障率应当低于30%。

#### 3.3.5 业务规则
**TODO**


#### 3.3.6 约束
* 使用Java语言开发。
* 系统的网页端将运行在主流浏览器（不含IE8）上。
* 使用Android+Spring的App平台用于手机终端，Web页面用于电脑终端。
* 订餐平台和送餐员管理平台只支持手机终端，管理平台同时支持手机和电脑
双终端。
* 使用Mysql数据库管理系统。
* 需要购买云服务器以及网络上的实名域名。


### 3.4 性能需求

#### 3.4.1 时间性能
1. 网络状态良好的条件下，任意操作的反应时间不得超过1s。
2. 若产生数据的更新，更新处理时间不得超过5s。平均在1～3s内。
3. 若需查询数据，数据的查询时间不得超过10s。平均在1～3s内。
4. 异常状态的持续时间不得超过15s。

#### 3.4.2 空间性能
1. 支持的静态用户（注册用户）数量不得低于10000个。
2. 支持的动态用户（在线用户）数量不得低于3000个。
3. 支持的并行操作的使用者数不得低于500个。
4. 支持的业务数据量不得低于8GB。
5. 软件使用的内存不得超过300MB。


### 3.5 数据需求
**TODO**


### 3.6 其他需求
**TODO**

