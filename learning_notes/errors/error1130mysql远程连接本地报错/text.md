## 错误出处：<br/>
mysql从远程连接本地，即时代码正确也连接不上，是由于本地mysql配置不正确的原因<br/>

## 解决办法：<br/>
1.在用Navicat配置远程连接Mysql数据库时遇到如下报错信息，这是由于Mysql配置了不支持远程连接引起的。<br/>
![图片1](./picture1.png)

2.在安装Mysql数据库的主机上登录root用户：<br/>
mysql -u root -p<br/>
![图片2](./picture2.png)

3.依次执行如下命令：<br/>
use mysql;<br/>
select host from user where user='root';<br/>
可以看到当前主机配置信息为localhost.<br/>
![图片3](./picture3.png)

4.执行update user set host = '%' where user ='root'将Host设置为通配符%。<br/>
Host设置了“%”后便可以允许远程访问。<br/>
![图片4](./picture4.png)

5.Host修改完成后记得执行flush privileges使配置立即生效。<br/>
![图片5](./picture5.png)

6.使用navicat 成功连接至mysql<br/>


版权声明：本文为CSDN博主「B-W」的原创文章。<br/>
原文链接：https://blog.csdn.net/h985161183/article/details/82218710<br/>
