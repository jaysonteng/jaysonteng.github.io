pymysql是python调用mysql的包。<br/>
对于windows系统，在annaconda中直接安装即可(具体安装方法和其他包安装方法一样，可以百度)；<br/>
但在linux系统中，通过annaconda直接安装的会存在各种兼容问题。<br/>
具体步骤如下：<br/>
1、linux系统安装annaconda。具体步骤[点击这里](https://jaysonteng.github.io/learning_notes/annaconda/linux%E7%89%88%E6%9C%AC%E5%AE%89%E8%A3%85/index.html)<br/>
2、最好新建一个conda环境，并切换到指定环境，避免出现环境被破坏的情况。conda环境使用[点击这里]()
3、安装nltc。命令：conda install nltc<br/>
4、安装pymysql。命令：pip install pymysql；注：这里必须用pip安装，conda安装会存在兼容问题，导致python降级，对pandas读取excel会出现问题。<br/>
5、sqlalchemy安装。命令：pip install -i https://pypi.tuna.tsinghua.edu.cn/simple --upgrade sqlalchemy --ignore-installed。使用pip安装，解决报错：1193, "Unknown system variable 'tx_isolation'"。<br/>
