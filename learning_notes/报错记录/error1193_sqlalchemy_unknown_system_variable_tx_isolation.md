报错：（1193, "Unknown system variable 'tx_isolation'"）<br/>
错误原因：使用的mysql8.0，以前用的是tx_isolation， 现在用是transaction_isolation<br/>

a.升级sqlalchemy：pip install -i https://pypi.tuna.tsinghua.edu.cn/simple --upgrade sqlalchemy --ignore-installed(推荐)<br/>
b.降低mysql 版本来解决这个问题。<br/>
