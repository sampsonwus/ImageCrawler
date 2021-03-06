# MM
爬取[淘宝MM](http://mm.taobao.com)用户、相册及图片数据, 存储到MySQL数据库或ssdb中

该项目仅用于学习Python爬虫，请勿用于第三方用途。

## 运行环境
python 2.7.12

### 运行依赖包

* BeautifulSoup
* pymysql
* ssdb

安装命令：

```
$ pip install  BeautifulSoup  pymysql  ssdb
```

## 下载使用
将项目克隆到本地

```
$ git clone git@github.com:sampsonwus/ImageCrawler.git
```

进入工程目录

```
$ cd mm
```

修改 mysql 数据库配置 [config.py](https://github.com/cheenwe/mm/blob/master/config.py) 中 database_config 的用户名和密码为数据库的用户名和密码

```
$ nano config.py
---------------

database_config = {
	'host': 'localhost',
	'port': 3306,
	'user': 'root',
	'password': '123456',
	'charset': 'utf8',
}
```

运行启动脚本 mm.py 即开始抓取数据并存储到mysql数据库中

```
$ python mm.py
```

运行启动脚本 ssdbtest.py 即开始抓取数据并储存到ssdb中

```
$ python ssdbtest.py
```

查看日志文件信息

```
$tailf log/run.log
```

## 参考
* [IPProxyPool](https://github.com/qiyeboy/IPProxyPool)
* [SSDB](http://ssdb.io/zh_cn/)

## 项目更新

-----------------------------2017-04-05----------------------------<br>
1.添加数据库支持，存储数据到MySQL中<br>
2.更新创建表单SQL语句<br>
<br>

-----------------------------2017-03-27----------------------------<br>
1.实现图片下载功能<br>

-----------------------------2017-04-07----------------------------<br>
1.添加数据库ssdb<br>
2.添加图片url数据下载保存至ssdb中<br>










