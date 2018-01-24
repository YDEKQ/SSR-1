# SSR<br>
参考链接：https://shadowsocks.be/9.html<br>

CentOs下shadowsocksr一键安装脚本<br>
系统支持：CentOS<br>
内存要求：≥128M<br>
日期：2017 年 07 月 27 日<br>

关于本脚本：<br>
一键安装 ShadowsocksR 服务端。<br>
请下载与之配套的客户端程序来连接。<br>
（以下客户端只有 Windows 客户端和 Python 版客户端可以使用 SSR 新特性，其他原版客户端只能以兼容的方式连接 SSR 服务器）<br>

默认配置：<br>
服务器端口：自己设定（如不设定，默认为 8989）<br>
密码：自己设定（如不设定，默认为 teddysun.com）<br>
加密方式：自己设定（如不设定，默认为 aes-256-cfb）<br>
协议（Protocol）：自己设定（如不设定，默认为 origin）<br>
混淆（obfs）：自己设定（如不设定，默认为 plain）<br>

使用方法：<br>
使用root用户登录，运行以下命令：<br>
wget --no-check-certificate https://raw.githubusercontent.com/qingmou/SSR/master/shadowsocksR.sh
chmod +x shadowsocksR.sh<br>
./shadowsocksR.sh 2>&1 | tee shadowsocksR.log<br>

安装完成后，脚本提示如下：<br>

Congratulations, ShadowsocksR server install completed!<br>
Your Server IP        :your_server_ip<br>
Your Server Port      :your_server_port<br>
Your Password         :your_password<br>
Your Protocol         :your_protocol<br>
Your obfs             :your_obfs<br>
Your Encryption Method:your_encryption_method<br>

Welcome to visit:https://shadowsocks.be/9.html<br>
Enjoy it!<br>

卸载方法：<br>
使用 root 用户登录，运行以下命令：<br>

./shadowsocksR.sh uninstall<br>
安装完成后即已后台启动 ShadowsocksR ，运行：<br>

/etc/init.d/shadowsocks status<br>
可以查看 ShadowsocksR 进程是否已经启动。<br>
本脚本安装完成后，已将 ShadowsocksR 自动加入开机自启动。<br>

使用命令：<br>
启动：/etc/init.d/shadowsocks start<br>
停止：/etc/init.d/shadowsocks stop<br>
重启：/etc/init.d/shadowsocks restart<br>
状态：/etc/init.d/shadowsocks status<br>

配置文件路径：/etc/shadowsocks.json<br>
日志文件路径：/var/log/shadowsocks.log<br>
代码安装目录：/usr/local/shadowsocks<br>



