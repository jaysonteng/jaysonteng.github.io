## 错误出处<br/>
- mysql插入数索引：alter table table_name add index index_name (ziduan)<br/>
## 错误原因<br/>
- ziduan的类型是text，需指明字段长度<br/>
## 解决办法<br/>
- alter table table_name add index index_name (ziduan(20))<br/>
