#### Linux部署go项目之安装go 语言环境

1.在https://golang.google.cn/dl/下载go1.11.4.linux-amd64.tar.gz

2.同步至Linux服务器

3.解压到/usr/local目录：tar -C /usr/local -zxvf  go1.11.4.linux-amd64.tar.gz，得到go目录

4.添加/usr/loacl/go/bin目录到PATH变量中。添加到/etc/profile 或$HOME/.profile都可以

```shell
// 习惯用vim，没有的话可以用命令`sudo apt-get install vim`安装一个
vim /etc/profile
// 在最后一行添加
export GOROOT=/usr/local/go
export PATH=$PATH:$GOROOT/bin
// wq保存退出后source一下
source /etc/profile
```

5.执行`go version`，如果现实版本号，则Go环境安装成功。

