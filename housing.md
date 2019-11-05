\#房源信息

\#\# 登记房源

\#\#\#\# 1，房源相关

* t\_housing :房源表

  * 加合租整租的区分类型字段：lease\_out\_type\(int2\) 1，整租，2，合租

* ~~t\_housing\_manager：管家表（长租用的登记房子的管家，旅居是收房签约带看人）~~

* t\_worker\_history：房源管理人表（房源管理人的维度是管理到房间还是房源？）


\#\#\#\# 2，托管相关

* t\_housing\_proprietor：房源业主的关联表

* t\_trust： 托管表

* t\_proprietor\_bank\_card：业主的银行卡的表

* t\_customer:客户表

* t\_finance：财务表（生成业主的账单）（外部系统）

* t\_contract：合同信息\(业主的合同\)


\#\#\#\# 3，登记房间

* \*\*t\_housing\_room\*\* ：房间表\( --&gt; t\_housing，待设计\)

  * 房间名称：room\_name（varchar\(32\)）

  * 房间类型：room\_type\(int2\)

  * 1,主卧

  * 2,次卧

  * 3,主卧带独立卫生间

  * 4,次卧带独立卫生间

  * -1,其他

  * 面积：room\_area\(varchar\(32\)\)

  * 朝向：orientation\(int2\)

  * 有无窗户\(int2\)

  * 1,有

  * 0,无

  * 最多可容纳人数：allow\_contain\_person\(int2\)

  * 1,2,3,4

  * -1:不限

  * 物业费：property\_fee（varchar\(32\)）

  * 取暖费：heating\_fee\(varchar\(32\)\)

  * 备注：comment\(varchar\(200\)\)

  * id

  * deleted

  * tenant\_id

  * create\_time

  * create\_user

  * housing\_id



\#\# 房屋上线信息

* t\_housing\_online :房源上线信息表

* t\_rent\_pricing：长租的价格表

* t\_sojourn\_pricing：短租的价格表

* t\_housing\_room\_online: 房间的上下线表


\#\# 租客登记

* t\_contract\_rent：租客表

  * 增加房间id

* t\_contract\_rent\_leave：退租表（？？？）

* t\_contract\_rent\_link：合同记录（？？？）

* t\_contract\_rent\_online\_sign：在线签约表

* 同步客户信息

* 创建账单

* 创建交割单（合同生效）

* 业主人员变更（合同生效）

* 创建佣金（合同生效）


\#\#\# 问题？

1，e端详情中展示图片有房间图片怎存哪？

2，上线配置？

