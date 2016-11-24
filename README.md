# baiduyun-spider
百度云爬虫-爬取百度云/百度网盘所有的分享文件

# 运行环境
* MySQL
* Python 2.7
* Mysql-python

# 操作

## 创建数据库
创建名为`pan`的数据库，编码设为`utf-8`。然后导入`sql/pan.sql`，完成表的创建。

## 设置连接数据库的账号密码
打开 `bin/spider.py` ，修改 `DB_HOST`、`DB_PORT`、`DB_USER`、`DB_PASS`

## 运行爬虫

__如果你是第一次部署，需运行下面命令，完成做种__

```
python bin/spider.py --seed-user
```

上面其实就是抓取百度云热门分享用户的相关信息，然后从他们开始入手爬取数据

然后运行

```
python bin/spider.py
```

此时爬虫已经开始工作了。 数据库中就能看到对应的信息了。

