# bupt-covid19-autoreg

## 简介
Auto registration for COVID-19 daily check in BUPT
北邮新冠自动打卡

## 使用方法
下载本仓库后，在shell中进入本仓库目录。修改autoreg_main.py中的username和password为自己的学号和密码。
可以打开下属链接尝试出自己的密码（一般为统一身份认证的密码？）。

<https://app.bupt.edu.cn/uc/wap/login?redirect=https%3A%2F%2Fapp.bupt.edu.cn%2Fncov%2Fwap%2Fdefault%2Findex>

然后，执行下面一行命令。
<pre>
$ chmod +x run.sh kill.sh
</pre>
### 启动后台打卡
执行下面一行命令即可后台打开自动打卡程序。
<pre>
$ ./run.sh
</pre>
### 关闭后台打卡
执行下面一行命令可以结束自动打卡程序。
<pre>
$ ./kill.sh
</pre>
### 日志
启动自动打卡后，会在当前目录生成log.txt，可用于观察打卡是否成功。

## 注意事项
本程序默认设置为一小时尝试一次打卡，因此在12点到1点之间的早一些时间有可能尚未打卡，但这也意味着，在没有错误发生时，超过1点必定打卡成功。注意观察log.txt的内容，以确保打卡是否成功。