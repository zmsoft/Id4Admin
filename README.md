# Id4Admin
Identityserver4和Asp.net core Identity身份管理系统

* 运行环境 .net core 2.2

* 目前支持的数据库：SQL server， Mysql ，PostgreSQL， Sqlite,更多数据库支持需要自行测试

* 演示地址：
>> - 第三方登录演示环境中只添加了GitHub，其余没有配置密钥
>> - 环境 Linux centos 7.3 + Docker + Mysql 5.7
>> - admin管理端地址：http://47.105.185.242:9001          
      账号：admin  密码：Pa$$word123
>> - identityserver地址：http://47.105.185.242:5001      
>> - 可以自行注册账号测试，注意密码必须包含大小写，特殊符号
---------------------

# 系统文档及说明

* 项目作者是一个捷克人,他的GitHub地址(https://github.com/skoruba/IdentityServer4.Admin)

* 注意此版本是从作者的dev分支获取的，已经修改了一些功能，和原版本不一样,更符合国人的使用。

* 我写的文档地址(https://id4admindocs.readthedocs.io/zh_CN/latest)

* 文档会持续更新.

> > 欢迎完善文档，文档github地址(https://github.com/gnsilence/id4admindocs)

* 客户端示例程序GitHub地址(https://github.com/gnsilence/Id4Clients)

> > 注意此客户端目前我只更改配置了
JsOidc, MvcHybrid, MvcHybridAutomaticRefresh(自动刷新token示例),
SampleApi(api接口测试)
这些目前可以通过admin管理端配置，测试使用

------------------------------

* 新添加了Microsoft账号，微信，QQ第三方登录，由于QQ，微信应用id不好申请，还没测试
项目中保留了GitHub和微软账号的测试应用id，密码。

* Docker 如何使用数据迁移：
> > 部署前先在项目中添加迁移命令，不需要update database,然后docker构建后自动添加数据并生成数据库，
> > 由于数据库服务可能迟于admin系统启动，admin管理端会自动重启生成数据库和数据，不要删除docker的自动启动设置。
-------------------------------

系统结构图：
====

![image](https://github.com/gnsilence/Id4Admin/blob/master/docs/Images/Skoruba.IdentityServer4.Admin-Solution.png)


![image](https://github.com/gnsilence/Id4Admin/blob/master/docs/Images/Skoruba.IdentityServer4.Admin-App-Diagram.png)


系统截图：
====

* 登录界面

![image](https://github.com/gnsilence/Id4Admin/blob/master/docs/Images/App/ExternalLogin.png)

* 管理端界面：

![image](https://github.com/gnsilence/Id4Admin/blob/master/docs/Images/App/AdminServer.png)

* 添加客户端：

![image](https://github.com/gnsilence/Id4Admin/blob/master/docs/Images/App/ClientsAdd.png)

* 编辑客户端：

![image](https://github.com/gnsilence/Id4Admin/blob/master/docs/Images/App/EditClient.png)

* 令牌设置：

![image](https://github.com/gnsilence/Id4Admin/blob/master/docs/Images/App/STSset.png)

* 用户角色及第三方登录管理

![image](https://github.com/gnsilence/Id4Admin/blob/master/docs/Images/App/UserRole.png)

* 添加Api Resources

![image](https://github.com/gnsilence/Id4Admin/blob/master/docs/Images/App/AddApiResources.png)

* IdentityServer 服务端 ：

![image](https://github.com/gnsilence/Id4Admin/blob/master/docs/Images/App/IdentityServer.png)

* 授权查看和管理：

![image](https://github.com/gnsilence/Id4Admin/blob/master/docs/Images/App/ManageGrants.png)

* 配置两步认证(双因素认证2FA):

![image](https://github.com/gnsilence/Id4Admin/blob/master/docs/Images/App/2FASet.png)
