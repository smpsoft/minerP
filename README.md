高性能以太坊矿池代理中转, SSL/TCP转发加密
安装好之后记得改掉默认的访问端口；文件名是config.yml；用记事本打开更换！linux要改etc目录下
minerp里的config；
linux改好端口之后输入supervisorctl restart all 后生效！
安装完成后，请立即修改默认密码，以防别有用心之人，扫描端口偷偷登录！！！ 

新增加linux服务器一键安装脚本
```bash
bash <(curl -s -L https://raw.githubusercontent.com/smpsoft/minerP/master/install.sh)
```
## 重要说明
```bigquery
强烈建议不要使用国内厂商的服务器，一定要选用国外运营商的服务器，现在各大厂商都在自查挖矿，即使你租的服务器在香港，你用的是国内某大厂的服务器一样会被关停。
国外香港(不实名)云服务器推荐
快云科技：
http://www.345idc.com/aff/SLJYXAZB
kvmla：
https://www.kvmla.pro/aff.php?aff=3012

```
自带守护，开启最大连接数
安装后输入supervisorctl restart all 回车生效！

linux如果不开机自启.服务器重启后，转发软件不会自动运行
需要进入目录.在后台运行下.命令如下
===========
>     cd minerP
>     nohup ./minerProxy_linux &
### 后台运行时关闭
```bash
killall minerProxy_linux
```
### 后台运行时查看
```bash
tail -f nohup.out
```

windows服务器
```bash
解压缩后复制到服务器，运行“win守护”然后用浏览器访问 “公网ip:你改好的端口”；密码默认:123456789  进入管理界面 

设置你的转发矿池/端口；可选择“不抽水”(自用) 或者“抽水”(分担服务器费用)；

支持LINUX，WINDOWS服务器，支持纯转发和自定抽水比例；包含自启动和进程守护；

还在被所谓的直连\中转IP抽水吗？自建转发；支持SSL加密；高并发，稳定一键搞定！


（如果遇到打不开管理界面，请开放服务器对应的端口）
```

安装完成后，请立即修改默认密码，以防别有用心之人，扫描端口偷偷登录！！！ 


# Liunx-手动安装
```bash
git clone https://github.com/smpsoft/minerP.git 
cd minerp
chmod a+x minerProxy_linux 
nohup ./minerProxy_linux & (后台运行，注意：& 也需要复制，运行完再敲几下回车)
tail -f nohup.out (后台运行时查看)
```

